# OmniXRI's Edge AI & TinyML 小學堂 【第12講】實作案例 ─語音辨識（快速指令表）
講師：歐尼克斯實境互動工作室 許哲豪(Jack Hsu)博士
2024/05/21 整理製作

## 12.3 Arduino環境建置  

### 12.3.1 連接開發板

以 USB Type C纜線連接電腦和開發板，檢查「裝置管理員」下「連接埠(COM和LPT)」是否有多一個「USB序列裝置（COMxx）」。xx即為埠號，會隨電腦即插入USB位置每次都會隨機配置。若沒有產生序列裝置，則可快速按開發板「Reset」鍵二次，令其進入模式。

### 12.3.2 安裝 Arduino 開發環境
1. 安裝 Arduino 2.x (Windows Win 10 and newer, 64 bits)
   https://www.arduino.cc/en/software
2. 開啟Arduino 
3. 點選選單 File > Preference ... ，並於 "Additional Boards Manager URLs" 項目填入 **https://files.seeedstudio.com/arduino/package_seeeduino_boards_index.json**
4. 點選選單 Tools > Board > Boards Manager... , 輸入 **nRF52840** 搜尋 Seeed nRF52840 開發板相關函式庫。 安裝下列二個函式庫。版本選最新即可，按下「INSTALL」鍵後開始安裝
   4.1. **Seeed nRF52 Boards (BLE, 低功耗用）**
   4.2. **Seeed nRF52 mbed-enabled Boards （PDM, IMU, ML使用）**
5. 指定好欲工作的開發板名稱及埠號，點選選單 Tools > Board > Seeed nRF52 Boards > Seeed XAIO  nRF52840 Sense 並選擇 Port。可點選 Tools > Get Board Info 來檢查連線是否正確。

### 12.3.3 測試程式編譯及上傳（LED閃爍）

1. 點選選單 File > Examples > 01.Basics > Blink 會自動產生下列程式碼

```c++=
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH); // turn the LED on (HIGH is the voltage level)
  delay(1000); // wait for a second
  digitalWrite(LED_BUILTIN, LOW); // turn the LED off by making the voltage LOW
  delay(1000); // wait for a second
}
```

2. 點選快捷鍵列的**上傳鍵（右箭頭符號）**，此時程式就會開始編譯，完成後會自動上傳到開發板上。如果看到開發板上紅色LED以1秒亮1秒暗，即完成測試。
3. 若無法上傳，快按開發板上RESET鍵二次，再重新選擇開發板及埠號，重新上傳即可。
4. 以上程式 **LED_BUILTIN** (等同於LED_RED)可試著修改成其它顏色LED（紅色LED_RED, 綠色LED_GREEN, 藍色LED_BLUE），或修改延遲時間長度。

## 12.4. Edge Impulse Studio  

### 12.4.1 Edge Impulse 簡介
[Edge Impulse](https://edgeimpulse.com/)  
    - [Product](https://edgeimpulse.com/product)  
    - [Public Projects](https://edgeimpulse.com/projects/overview)  
    - [Blog](https://www.edgeimpulse.com/blog/)
    - [Developer Document](https://docs.edgeimpulse.com/docs)  
    - [Expert network projects](https://edge-impulse.gitbook.io/experts)
     
### 12.4.2 建置工作環境

[完整安裝說明](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli/cli-installation)

- 申請並登入 [Edge Impulse 帳號](https://studio.edgeimpulse.com/login)
- 安裝 [Python 3.x](https://www.python.org/downloads/)
- 安裝 [Node.js (建議安裝v18.20.2 LTS)](https://nodejs.org/en/download)
- **安裝 Node.js 時要注意，記得一定要勾選「Tools for Native Modules」**
- 以 node -v 及 npm -v 檢查安裝好的版本
- 下載並安裝Arduino CLI （命令列界面） <winodws exe 64bit> [【完整說明】](https://arduino.github.io/arduino-cli/0.35/installation/)
- 安裝 Edge Impulse CLI [【完整說明】](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli/cli-installation) 
```npm install -g edge-impulse-cli --force``` 
- 安裝完成後會得到下列工具
     - edge-impulse-daemon
     - edge-impulse-uploader
     - edge-impulse-data-forwarder
     - edge-impulse-run-impulse
     - edge-impulse-blocks
     - himax-flash-tool
- [Edge Impulse 資料集建置方式](https://edge-impulse.gitbook.io/docs/edge-impulse-studio/data-acquisition)
    - 從裝置產生（手機、電腦、開發板）
    - 直接上傳檔案

### 12.4.3 啟動公用專案範例 

[Edge Impulse Inc. / Tutorial: Recognize sounds from audio](https://studio.edgeimpulse.com/public/14301/latest)

點擊左上角「Clone this project」複製到個人專案，才可開始修改測試。

## 12.5 建立 Edge Impulse 專案

Xiao nRF52840 Sense 範例主要參考資料。
- XIAO nRF52840 Sense 上的 PDM 麦克风的使用
https://wiki.seeedstudio.com/cn/XIAO-BLE-Sense-PDM-Usage/
- 基于 Edge Impulse 的语音识别
https://wiki.seeedstudio.com/cn/XIAO-BLE-PDM-EI/
- 基于 TensorFlow Lite 的语音识别
https://wiki.seeedstudio.com/cn/XIAO-BLE-Sense-TFLite-Mic/

**實驗用資料集 on_off_noise_dataset.zip**，包含兩個檔案夾各三個標籤，資料來源 Google speech commands dataset v0.02摘要部份內容。
- train
    - on(500), off(500), noise(4)
- test
    - on(10), off(10), noise(2)

[下載連結](https://drive.google.com/file/d/1awBgM7YAbnhJS3EcWl-vPUpzOgTveA3U/view?usp=sharing)

以下僅提供參考，可以不用下載。
**Google speech commands dataset v0.02**
- [完整說明](https://www.tensorflow.org/datasets/catalog/speech_commands)
- 訓練集原始壓縮檔 2.37GB, 解壓縮後 3.19GB，36 檔案夾，共 105,841 個檔案。[【手動下載】](http://download.tensorflow.org/data/speech_commands_v0.02.tar.gz)
- 測試集原始壓縮檔 110MB, 解壓縮後 149MB，12 檔案夾，共 4,892 個檔案。[【手動下載】](http://download.tensorflow.org/data/speech_commands_test_set_v0.02.tar.gz)

### 12.5.1 建立專案流程

1. 登入帳號，建立新專案，名稱為 Xiao_nRF52840_KWS_Test (名稱可自定)，選擇個人專案「Personal」，設定專案屬性為公用「Public」（公用無數量限制，私人限制2個），按下「Create new project」產生新專案。
2. 不連線實體裝置來取樣。
3. 下載實驗用資料集 [on_off_noise_dataset.zip](https://drive.google.com/file/d/1awBgM7YAbnhJS3EcWl-vPUpzOgTveA3U/view?usp=sharing)，並解壓縮。
4. 按「+ Add data」，再按「upload data」，進入上傳資料模式。
5. 選擇「Select a folder」，選擇資料集路徑下 \train\on，指定分類為「Training」，指定標籤名稱為「on」，按下左下角「Upload data」完成上傳。
6. 接著依上述步驟5，修改標籤名稱，再分別把「off」和「noise」檔案夾內容上傳。
7. 再來指定分類為「Test」，分別完成上傳資料集路徑\test下的「on」、「off」和「noise」。
8. 由於資料集已完成分割，每個樣本為1秒，所以不需再分割。
9. 接著切換到 Create impulse 項目，修改 Window Size 為 500ms, Increase 100ms, 新增 Audio (MFCC) 及 Classification 區塊，參數使用預值即可，最後按「Save Impulse」儲存設定值。
10. 切換到 Spectral features，切換到 Generate features 子分頁，按下「Generate features」產生對應特徵值。
11. 切換到 Classification，設定訓練次數 30，學習率 0.0005，其它先使用預設值，按下「Start training」即可開始訓練。若推論精度及混淆矩陣表現不理想，可再增加訓練次數。
12. 完成訓練後，可切到 Live Classification 頁面，選擇右半部樣本名稱，再按「Load Sample」即可進行線上測試。

### 12.5.2 部署及測試

1. 切換到 Deployment 頁面，選擇 Arduino Library，按下「Build」，即可產生名為「ei-專案名稱-arduino-版本序號.zip」的檔案。
2. 開啟Arduino，點擊選單 Sketch > Include Library > Add .ZIP Library...，將剛才產生的檔案加入。
3. 新增範例檔，點擊選單 File > Examples > ei-專案名稱_inferencing > nano_ble33_sense > nano_ble33_sense_microphone，如下所示。（不包含51-53, 117-134列 新增之程式）
4. 將範例程式直接編譯上傳即可進行推論，此為 No Code 模式。輸出結果以 COM 埠接收文字串。包含推論時間、各標籤置信度。
5. 新增第 51-53 列，定義推論門檻值及LED目前及上一個狀態變數。117-134 列，指定當特定分類置信度高於門檻值時點滅對應的LED。
6. 預設推論時間間隔 2000ms，可自行調整第 86 列程式 delay(n); ， n 為時間間隔。

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

// If your target is limited in memory remove this macro to save 10K RAM
#define EIDSP_QUANTIZE_FILTERBANK   0

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

/* Includes ---------------------------------------------------------------- */
#include <PDM.h>
#include <Xiao_nRF52840_KWS_Test_inferencing.h>

/** Audio buffers, pointers and selectors */
typedef struct {
    int16_t *buffer;
    uint8_t buf_ready;
    uint32_t buf_count;
    uint32_t n_samples;
} inference_t;

static inference_t inference;
static signed short sampleBuffer[2048];
static bool debug_nn = false; // Set this to true to see e.g. features generated from the raw signal

float threshold = 0.50; // 分類置信度門檻值
int LED = 0; // 目前 LED 顯示狀態
int oldLED; // 上一次 LED 顯示狀態

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

    // summary of inferencing settings (from model_metadata.h)
    ei_printf("Inferencing settings:\n");
    ei_printf("\tInterval: %.2f ms.\n", (float)EI_CLASSIFIER_INTERVAL_MS);
    ei_printf("\tFrame size: %d\n", EI_CLASSIFIER_DSP_INPUT_FRAME_SIZE);
    ei_printf("\tSample length: %d ms.\n", EI_CLASSIFIER_RAW_SAMPLE_COUNT / 16);
    ei_printf("\tNo. of classes: %d\n", sizeof(ei_classifier_inferencing_categories) / sizeof(ei_classifier_inferencing_categories[0]));

    if (microphone_inference_start(EI_CLASSIFIER_RAW_SAMPLE_COUNT) == false) {
        ei_printf("ERR: Could not allocate audio buffer (size %d), this could be due to the window length of your model\r\n", EI_CLASSIFIER_RAW_SAMPLE_COUNT);
        return;
    }
}

/**
 * @brief      Arduino main function. Runs the inferencing loop.
 */
void loop()
{
    ei_printf("Starting inferencing in 2 seconds...\n");

    delay(1000); // 調整二次取樣推論間隔時間（ms）

    ei_printf("Recording...\n");

    bool m = microphone_inference_record();
    if (!m) {
        ei_printf("ERR: Failed to record audio...\n");
        return;
    }

    ei_printf("Recording done\n");

    signal_t signal;
    signal.total_length = EI_CLASSIFIER_RAW_SAMPLE_COUNT;
    signal.get_data = &microphone_audio_signal_get_data;
    ei_impulse_result_t result = { 0 };

    EI_IMPULSE_ERROR r = run_classifier(&signal, &result, debug_nn);
    if (r != EI_IMPULSE_OK) {
        ei_printf("ERR: Failed to run classifier (%d)\n", r);
        return;
    }

    // print the predictions
    ei_printf("Predictions ");
    ei_printf("(DSP: %d ms., Classification: %d ms., Anomaly: %d ms.)",
        result.timing.dsp, result.timing.classification, result.timing.anomaly);
    ei_printf(": \n");
    for (size_t ix = 0; ix < EI_CLASSIFIER_LABEL_COUNT; ix++) {
        ei_printf("    %s: %.5f\n", result.classification[ix].label, result.classification[ix].value);

        //lets light up some LEDS
        if (result.classification[ix].value > threshold) {
          //now let's see what label were in
          switch (ix) {
            case 0: LED = 11; break; // RED LED
            case 1: LED = 12; break; // BLUE LED
            case 2: LED = 13; break; // GREEN LED
            default: LED = 0;
          }
          //in Sense, LOW will light up the LED
          if (LED != 0) {
            digitalWrite (oldLED, HIGH); //if we enter a word right next to previous - we turn off the previous LED
            digitalWrite (LED, LOW);            
            oldLED = LED;
          }
          else //turn off LED
            digitalWrite (oldLED, HIGH);
        }
    }
#if EI_CLASSIFIER_HAS_ANOMALY == 1
    ei_printf("    anomaly score: %.3f\n", result.anomaly);
#endif
}

/**
 * @brief      PDM buffer full callback
 *             Get data and call audio thread callback
 */
static void pdm_data_ready_inference_callback(void)
{
    int bytesAvailable = PDM.available();

    // read into the sample buffer
    int bytesRead = PDM.read((char *)&sampleBuffer[0], bytesAvailable);

    if (inference.buf_ready == 0) {
        for(int i = 0; i < bytesRead>>1; i++) {
            inference.buffer[inference.buf_count++] = sampleBuffer[i];

            if(inference.buf_count >= inference.n_samples) {
                inference.buf_count = 0;
                inference.buf_ready = 1;
                break;
            }
        }
    }
}

/**
 * @brief      Init inferencing struct and setup/start PDM
 *
 * @param[in]  n_samples  The n samples
 *
 * @return     { description_of_the_return_value }
 */
static bool microphone_inference_start(uint32_t n_samples)
{
    inference.buffer = (int16_t *)malloc(n_samples * sizeof(int16_t));

    if(inference.buffer == NULL) {
        return false;
    }

    inference.buf_count  = 0;
    inference.n_samples  = n_samples;
    inference.buf_ready  = 0;

    // configure the data receive callback
    PDM.onReceive(&pdm_data_ready_inference_callback);

    PDM.setBufferSize(4096);

    // initialize PDM with:
    // - one channel (mono mode)
    // - a 16 kHz sample rate
    if (!PDM.begin(1, EI_CLASSIFIER_FREQUENCY)) {
        ei_printf("Failed to start PDM!");
        microphone_inference_end();

        return false;
    }

    // set the gain, defaults to 20
    PDM.setGain(127);

    return true;
}

/**
 * @brief      Wait on new data
 *
 * @return     True when finished
 */
static bool microphone_inference_record(void)
{
    inference.buf_ready = 0;
    inference.buf_count = 0;

    while(inference.buf_ready == 0) {
        delay(10);
    }

    return true;
}

/**
 * Get raw audio signal data
 */
static int microphone_audio_signal_get_data(size_t offset, size_t length, float *out_ptr)
{
    numpy::int16_to_float(&inference.buffer[offset], out_ptr, length);

    return 0;
}

/**
 * @brief      Stop PDM and release buffers
 */
static void microphone_inference_end(void)
{
    PDM.end();
    free(inference.buffer);
}

#if !defined(EI_CLASSIFIER_SENSOR) || EI_CLASSIFIER_SENSOR != EI_CLASSIFIER_SENSOR_MICROPHONE
#error "Invalid model for current sensor."
#endif

```
