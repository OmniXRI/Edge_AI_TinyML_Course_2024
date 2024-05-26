# OmniXRI's Edge AI & TinyML 小學堂 【第13講】實作案例 ─運動辨識（快速指令表）

講師：歐尼克斯實境互動工作室 許哲豪(Jack Hsu)博士 2024/05/28 整理製作  

## 13.1. 實驗器材及開發平台  
- [Seeed Wiki - Xiao nRF52840 Sense（英文）](https://wiki.seeedstudio.com/XIAO_BLE/)
- [Arduino Software Downloads](https://www.arduino.cc/en/software)
- [Edge Impulse Document](https://docs.edgeimpulse.com)

相關開發環境建置請參考  
[OmniXRI's Edge AI & TinyML 小學堂 【第12講】實作案例 ─語音辨識（快速指令表）](https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024/blob/main/Ch12_Keyword_Spoting/Ch12_KWS_Quick_Guide.md)

## 13.2 運動感測器(IMU)取值與輸出

1. 至 [Seeed Arduino LSM6DS3 Github](https://github.com/Seeed-Studio/Seeed_Arduino_LSM6DS3) 下載函式庫(*.zip)。
2. 開啟 Arduino IDE，點擊選單 Sketch > Include Library > Add .ZIP Library... 新增下載的函式庫。
3. 點擊選單 File > Examples > Seeed Arduino LSM6DS3 > IMU_Capture 開啟範例。
4. 依下列指示修改範例程式，方便後續連續輸出，可搭配 edge-impulse-data-forward 將感測器數值送到雲端。
    - 加入 // 註解掉第 7-9 列
    - 修改第 13 列，將COM埠通訊速度提升到 115,200 bps
    - 加入 // 註解掉第 25-49 列及第 65-69 列，讓程式以最快方式輸出 IMU 加速度計及陀螺儀數值。
5. 編譯並上傳程式到開發板，可點擊選單 Tools > Serial Monitor 或 Serial Plotter 監看 IMU 輸出數值文字串或數值圖形內容。

```c=
#include <LSM6DS3.h>
#include <Wire.h>

//Create a instance of class LSM6DS3
LSM6DS3 myIMU(I2C_MODE, 0x6A);    //I2C device address 0x6A
float aX, aY, aZ, gX, gY, gZ;
// const float accelerationThreshold = 2.5; // threshold of significant in G's
// const int numSamples = 119;
// int samplesRead = numSamples;

void setup() {
  // put your setup code here, to run once:
  Serial.begin(115200);
  while (!Serial);
  //Call .begin() to configure the IMUs
  if (myIMU.begin() != 0) {
    Serial.println("Device error");
  } else {
    Serial.println("aX,aY,aZ,gX,gY,gZ");
  }
}

void loop() {
  // wait for significant motion
//   while (samplesRead == numSamples) {
//     // read the acceleration data
//     aX = myIMU.readFloatAccelX();
//     aY = myIMU.readFloatAccelY();
//     aZ = myIMU.readFloatAccelZ();

//     // sum up the absolutes
//     float aSum = fabs(aX) + fabs(aY) + fabs(aZ);

//     // check if it's above the threshold
//     if (aSum >= accelerationThreshold) {
//       // reset the sample read count
//       samplesRead = 0;
//       break;
//     }
//   }

//   // check if the all the required samples have been read since
//   // the last time the significant motion was detected
//   while (samplesRead < numSamples) {
//     // check if both new acceleration and gyroscope data is
//     // available
//     // read the acceleration and gyroscope data

//     samplesRead++;

    // print the data in CSV format
    Serial.print(myIMU.readFloatAccelX(), 3);
    Serial.print(',');
    Serial.print(myIMU.readFloatAccelY(), 3);
    Serial.print(',');
    Serial.print(myIMU.readFloatAccelZ(), 3);
    Serial.print(',');
    Serial.print(myIMU.readFloatGyroX(), 3);
    Serial.print(',');
    Serial.print(myIMU.readFloatGyroY(), 3);
    Serial.print(',');
    Serial.print(myIMU.readFloatGyroZ(), 3);
    Serial.println();

  //   if (samplesRead == numSamples) {
  //     // add an empty line if it's the last sample
  //     Serial.println();
  //   }
  // }
}
```
## 13.3 手勢設計與資料上傳

## 13.4 建立 Edge Impulse 專案  

Xiao nRF52840 Sense 範例主要參考資料。
- XIAO nRF52840 Sense 上的 6-Axis IMU 的使用
https://wiki.seeedstudio.com/cn/XIAO-BLE-Sense-IMU-Usage/
- XIAO nRF52840 Sense 基于 Edge Impulse 的运动识别
https://wiki.seeedstudio.com/cn/XIAOEI/
- 基于 TensorFlow Lite 的运动识别
https://wiki.seeedstudio.com/cn/XIAO-BLE-Sense-TFLite-Getting-Started/

1. 登入帳號，建立新專案，名稱為 Xiao_nRF52840_IMU_Test (名稱可自定)，選擇個人專案「Personal」，設定專案屬性為公用「Public」（公用無數量限制，私人限制2個），按下「Create new project」產生新專案。
2. 使用開發板連線方式來取樣及測試。開啟命令列模式執行「``` edge-impulse-data-forwarder --clean```」，接著輸入帳號、密碼，按上下鍵選擇對應的專案名稱(Xiao_nRF52840_IMU_Test)，輸入開發板名稱（可自由命名）及資料數量及名稱（用逗號分隔），此時應可順利連接開發板到雲端，可打開 Edge Impulse 專案 Devices 檢查是否綠燈。
3. 進入 Edge Impulse Data acquistion 右半部 Data Collect data，選擇裝置，指定標籤名稱，設定取樣時長(10000ms)，按下「Start sampling」開始取樣。開始依定義手勢重覆執行多次（中間要有間隔），直到時間結束。
4. 點擊新增資料末端三小點符號，選擇「Split Sample」，進入分割資料模式，將每個樣本為1秒。
5. 進入後會自動設定分割位置及數量，如果不滿意，可自行調整，最後按下「Split」即可自動將內容分解成多個樣本。預設全部加入訓練集中。
6. 接著切換到 Create impulse 項目，修改 Window Size 為 500ms, Increase 100ms, 新增 Spectral Analysis，為加速訓練時間可僅勾選三軸加速度計(aX, aY, aZ)即可，再新增 Classifier 區塊，參數使用預值即可，最後按「Save Impulse」儲存設定值。
7. 切換到 Spectral features，切換到 Generate features 子分頁，按下「Generate features」產生對應特徵值。
8. 切換到 Classifier，設定訓練次數 30，學習率 0.0005，其它先使用預設值，按下「Start training」即可開始訓練。若推論精度及混淆矩陣表現不理想，可再增加訓練次數。
9. 若效果仍不理想，可將 Neural network architecture 二層 Dense Layer Neural數量都增加到 40（層數、神經元數可自定），再重新訓練即可。
10. 完成訓練後，可切到 Live Classification 頁面，選擇左半部 Classify new data，再按「Start sampling」即可進行取樣並進行線上測試。11. 

## 13.5 部署及測試  

1. 切換到 Deployment 頁面，選擇 Arduino Library，按下「Build」，即可產生名為「ei-專案名稱-arduino-版本序號.zip」的檔案。
2. 開啟Arduino，點擊選單 Sketch > Include Library > Add .ZIP Library...，將剛才產生的檔案加入。
3. 新增範例檔，點擊選單 File > Examples > ei-專案名稱_inferencing > nano_ble33_sense > nano_ble33_sense_acclerometer，如下所示。（不包含20, 21, 26, 100-102列 新增之程式）
4. 確認開發板設定，點擊選單 Tools > Boards > Seeed nRF52 mbed-enabled Boards > Seeed XIAO BLE Sense - nRF52840 。
5. 由於目前使用的 IMU 為 LSM6DS3 所以需修改程式內容如下。
    - 註解掉第 19 列， //#include <Arduino_LSM9DS1.h>
    - 新增第 20 列， #include <LSM6DS3.h>
    - 新增第 21 列， #include <Wire.h>
    - 新增第 26 列， LSM6DS3 myIMU(I2C_MODE, 0x6A);
    - 修改第 56 列， if (!myIMU.begin()) {
    - 註解掉第 99 列， //        IMU.readAcceleration(buffer[ix], buffer[ix + 1], buffer[ix + 2]);
    - 新增 100-102 列，
        buffer[ix]     = myIMU.readFloatAccelX();
        buffer[ix + 1] = myIMU.readFloatAccelY();
        buffer[ix + 2] = myIMU.readFloatAccelZ();
6. 將程式進行編譯後，第 148 列「#error "Invalid model for current sensor"」會產生「"invalid model for current sensor"」錯誤。主要原因為Edge Impulse打包時是以Sensor_Fusion方式處理而不是Accelerometer方式造成。
7. 點擊選單 File > Preferences 找到 Sketchbook Folder，進到該路徑後，進到 \libraries\專案名稱_inferencing\src\model-parameters\ ，開啟model_metadata.h ，找到 「 #define EI_CLASSIFIER_SENSOR                     EI_CLASSIFIER_SENSOR_FUSION 」，將定義改成「 EI_CLASSIFIER_SENSOR_ACCELEROMETER 」存檔即可。
8. 將範例程式直接編譯上傳即可進行推論，此為 No Code 模式。輸出結果以 COM 埠接收文字串。包含推論時間、各標籤置信度。
9. 預設推論時間間隔 2000ms，可自行調整第 88 列程式 delay(n); ， n 為時間間隔。
10. 如需驅動LED或其它硬體，可於第 140列後加入。

```c=
/* Edge Impulse ingestion SDK
 * Copyright (c) 2022 EdgeImpulse Inc.
 *
 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 * You may obtain a copy of the License at
 * http://www.apache.org/licenses/LICENSE-2.0
 *
 * Unless required by applicable law or agreed to in writing, software
 * distributed under the License is distributed on an "AS IS" BASIS,
 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 * See the License for the specific language governing permissions and
 * limitations under the License.
 *
 */

/* Includes ---------------------------------------------------------------- */
#include <Xiao_nRF52840_IMU_Test_inferencing.h>
//#include <Arduino_LSM9DS1.h> //Click here to get the library: https://www.arduino.cc/reference/en/libraries/arduino_lsm9ds1/
#include <LSM6DS3.h>
#include <Wire.h>
/* Constant defines -------------------------------------------------------- */
#define CONVERT_G_TO_MS2    9.80665f
#define MAX_ACCEPTED_RANGE  2.0f        // starting 03/2022, models are generated setting range to +-2, but this example use Arudino library which set range to +-4g. If you are using an older model, ignore this value and use 4.0f instead

LSM6DS3 myIMU(I2C_MODE, 0x6A);    //I2C device address 0x6A
/*
 ** NOTE: If you run into TFLite arena allocation issue.
 **
 ** This may be due to may dynamic memory fragmentation.
 ** Try defining "-DEI_CLASSIFIER_ALLOCATION_STATIC" in boards.local.txt (create
 ** if it doesn't exist) and copy this file to
 ** `<ARDUINO_CORE_INSTALL_PATH>/arduino/hardware/<mbed_core>/<core_version>/`.
 **
 ** See
 ** (https://support.arduino.cc/hc/en-us/articles/360012076960-Where-are-the-installed-cores-located-)
 ** to find where Arduino installs cores on your machine.
 **
 ** If the problem persists then there's not enough memory for this model and application.
 */

/* Private variables ------------------------------------------------------- */
static bool debug_nn = false; // Set this to true to see e.g. features generated from the raw signal

/**
* @brief      Arduino setup function
*/
void setup()
{
    // put your setup code here, to run once:
    Serial.begin(115200);
    // comment out the below line to cancel the wait for USB connection (needed for native USB)
    while (!Serial);
    Serial.println("Edge Impulse Inferencing Demo");

    if (!myIMU.begin()) {
        ei_printf("Failed to initialize IMU!\r\n");
    }
    else {
        ei_printf("IMU initialized\r\n");
    }

    if (EI_CLASSIFIER_RAW_SAMPLES_PER_FRAME != 3) {
        ei_printf("ERR: EI_CLASSIFIER_RAW_SAMPLES_PER_FRAME should be equal to 3 (the 3 sensor axes)\n");
        return;
    }
}

/**
 * @brief Return the sign of the number
 * 
 * @param number 
 * @return int 1 if positive (or 0) -1 if negative
 */
float ei_get_sign(float number) {
    return (number >= 0.0) ? 1.0 : -1.0;
}

/**
* @brief      Get data and run inferencing
*
* @param[in]  debug  Get debug info if true
*/
void loop()
{
    ei_printf("\nStarting inferencing in 2 seconds...\n");

    delay(1000);

    ei_printf("Sampling...\n");

    // Allocate a buffer here for the values we'll read from the IMU
    float buffer[EI_CLASSIFIER_DSP_INPUT_FRAME_SIZE] = { 0 };

    for (size_t ix = 0; ix < EI_CLASSIFIER_DSP_INPUT_FRAME_SIZE; ix += 3) {
        // Determine the next tick (and then sleep later)
        uint64_t next_tick = micros() + (EI_CLASSIFIER_INTERVAL_MS * 1000);

//        IMU.readAcceleration(buffer[ix], buffer[ix + 1], buffer[ix + 2]);
        buffer[ix]     = myIMU.readFloatAccelX();
        buffer[ix + 1] = myIMU.readFloatAccelY();
        buffer[ix + 2] = myIMU.readFloatAccelZ();

        for (int i = 0; i < 3; i++) {
            if (fabs(buffer[ix + i]) > MAX_ACCEPTED_RANGE) {
                buffer[ix + i] = ei_get_sign(buffer[ix + i]) * MAX_ACCEPTED_RANGE;
            }
        }

        buffer[ix + 0] *= CONVERT_G_TO_MS2;
        buffer[ix + 1] *= CONVERT_G_TO_MS2;
        buffer[ix + 2] *= CONVERT_G_TO_MS2;

        delayMicroseconds(next_tick - micros());
    }

    // Turn the raw buffer in a signal which we can the classify
    signal_t signal;
    int err = numpy::signal_from_buffer(buffer, EI_CLASSIFIER_DSP_INPUT_FRAME_SIZE, &signal);
    if (err != 0) {
        ei_printf("Failed to create signal from buffer (%d)\n", err);
        return;
    }

    // Run the classifier
    ei_impulse_result_t result = { 0 };

    err = run_classifier(&signal, &result, debug_nn);
    if (err != EI_IMPULSE_OK) {
        ei_printf("ERR: Failed to run classifier (%d)\n", err);
        return;
    }

    // print the predictions
    ei_printf("Predictions ");
    ei_printf("(DSP: %d ms., Classification: %d ms., Anomaly: %d ms.)",
        result.timing.dsp, result.timing.classification, result.timing.anomaly);
    ei_printf(": \n");
    for (size_t ix = 0; ix < EI_CLASSIFIER_LABEL_COUNT; ix++) {
        ei_printf("    %s: %.5f\n", result.classification[ix].label, result.classification[ix].value);
    }
#if EI_CLASSIFIER_HAS_ANOMALY == 1
    ei_printf("    anomaly score: %.3f\n", result.anomaly);
#endif
}

#if !defined(EI_CLASSIFIER_SENSOR) || EI_CLASSIFIER_SENSOR != EI_CLASSIFIER_SENSOR_ACCELEROMETER
#error "Invalid model for current sensor"
#endif
```
