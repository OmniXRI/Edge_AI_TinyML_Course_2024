# OmniXRI's Edge AI & TinyML 小學堂 【第13講】案例實作─運動辨識
作者：許哲豪(Jack Hsu), 2024/05/28

**完整課程簡報：20240528_Course_13_OmniXRI_Jack.pdf**

**Youtube直播影片：https://youtube.com/live/7vr6FfhaRfs**

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 13.1.運動感測技術簡介
- 實驗器材簡介及開發平台安裝回顧
    - 直播連結：https://youtu.be/y5SOsljxELA
    - 快速指令：https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024/blob/main/Ch12_Keyword_Spoting/Ch12_KWS_Quick_Guide.md
- 何謂運動感測器
- 加速度計 (G Sensor)
- 陀螺儀 (Gyro Sensor)
- 地磁感測器
- 運動感測常見應用
- Edge Impulse 運動感測相關案例
    - [Continuous motion recognition](https://edge-impulse.gitbook.io/docs/tutorials/end-to-end-tutorials/continuous-motion-recognition)
    - [Experts Network Projects](https://docs.edgeimpulse.com/experts#accelerometer-and-activity-projects)
    - [Blog & Projects](https://edgeimpulse.com/blog/)
- Arduino Nano 33 BLE Sense 
    - [Rev1](https://store-usa.arduino.cc/products/arduino-nano-33-ble-sense)
    - [Rev2](https://store-usa.arduino.cc/products/nano-33-ble-sense-rev2)
- [Seeed Xiao nRF52840 Sense](https://wiki.seeedstudio.com/cn/XIAO_BLE/)
- Xiao nRF52840 Sense 模組 ─ 參考電路
- 穿戴式智慧人工智慧裝置 ─ 參考外形

## 13.2.運動感測器取值與輸出
- Xiao nRF52840 Sense 模組 ─ 連接開發板
- [**快速操作指令表（方便快速複製貼上命令）**](https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024/blob/main/Ch13_Motion_Recognition/IMU_Quick_Guide.md)
- 測試程式：運動感測器（IMU）
- 監看運動感測器輸出值

## 13.3.手勢設計與資料上傳
- 設計操作手勢
- Edge Impulse 資料集建置方式

## 13.4.Edge_Impulse_手勢辨識案例
- 建立 Edge Impulse 新專案
- 啟動edge-impulse-data-forwarder 
- 檢查裝置是否已連線
- 從外部裝置取得資料
- 大量收集樣本並分割成獨立可訓練樣本
- 原始資料與自動分割
- 反複收集分割，建立完整資料集
- 選擇模型及設定必要參數
- 提取資料特徵
- 提取特徵結果
- 設定分類訓練相關參數
- 開始進行模型訓練及結果顯示
- 線上測試（從外部裝置取樣）
- 選擇部署種類及設定參數
- 導入 Arduino 函式庫並進行推論測試
- 手勢辨識結果（Arduino部份）
- 使用 Google TensorFlow 完成訓練部署

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] 許哲豪， 【課程簡報】20240509_慈濟醫資_穿戴式人工智慧工作坊_利用TinyML技術快速搭建微型智慧應用
https://omnixri.blogspot.com/2024/05/20240509tinyml12.html

[3] iThome 2021 (13屆) 鐵人賽【arm platforms組】完賽記錄 ─ 爭什麼，把AI和MCU摻在一起做tinyML就對了！ 
https://omnixri.blogspot.com/2021/10/ithome-2021-13-arm-platforms-aimcutinyml.html

[4] 矽递科技(Seeed Studio) Wiki 文档平台 - XIAO nRF52840 (Sense) 开发板  
https://wiki.seeedstudio.com/cn/XIAO_BLE/

[5] Edge Impulse, Developers Document  
https://docs.edgeimpulse.com/

## 延伸閱讀

[A] Yahya Tawil, Towards understanding IMU: Basics of Accelerometer and Gyroscope Sensors and How to Compute Pitch, Roll and Yaw Angles
https://atadiat.com/en/e-towards-understanding-imu-basics-of-accelerometer-and-gyroscope-sensors/

[B] Leonardo Cavagnis, Gesture Recognition with Edge Impulse and Arduino
https://leonardocavagnis.medium.com/gesture-recognition-with-edge-impulse-and-arduino-0da09c0873d5

[C] 【iCShop開箱趣】ep7 Seeed Studio XIAO nRF52840 Sense Review | 把神經網路放到MCU原來這麼簡單？ TinyML Tutorial 範例教學
https://youtu.be/Faka_ahto0o

[D] 林士允(Felix Lin)， 【Maker 玩 AI】 XIAO nRF52840 Sense－入門 TinyML 就靠它！
https://vmaker.tw/archives/65534

## 教學資源

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。
