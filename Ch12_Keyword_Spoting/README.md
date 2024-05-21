# OmniXRI's Edge AI & TinyML 小學堂 【第12講】實作案例 ─ 語音辨識
作者：許哲豪(Jack Hsu), 2024/05/21

**完整課程簡報：20240521_Course_12_OmniXRI_Jack.pdf**  

**Youtube直播影片：https://youtu.be/y5SOsljxELA**  

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 12.1.智慧物聯網與感測技術
- TinyML 回顧
    - [課程簡報](https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024/tree/main/Ch07_TinyML_Introduction)
    - [直播影片](https://youtu.be/5ln7UT5pzFs)
- 傳統智慧物聯網(AIoT)架構
- 傳統型AIoT vs. 新型態TinyML
- 常見感測技術
- 常見市售感測器實驗模組
    - [Seeed Studio Grove](https://www.seeedstudio.com/category/Grove-c-1003.html)
- 感測器類比/數位信號互換

## 12.2.喚醒詞技術簡介
- 喚醒詞偵測
- 案例分享 ─ 聲控電風扇
    - [正確示範（美女版）](https://www.youtube.com/shorts/X8yJjRj7Uus)
    - [錯誤示範（阿媽版）](https://www.youtube.com/shorts/frDYfeRiz9I)
    - [正確示範（台灣國語）](https://youtu.be/vpZgt0VQf8Y)
- 聲音訊號─取樣、量化
- 常見聲音訊號波形（時間域）
- 時間域、頻率域轉換
- 時域、頻譜、梅爾倒頻譜表示法
- 深度學習模型聲音分類
- 關鍵詞偵測(KWS)程序

## 12.3.TinyML開發流程與環境
- TinyML 開發流程
- TinyML 實驗器材及開發平台
- Seeed Studio Xiao（小）系列
- [Xiao nRF52840 Sense 模組](https://wiki.seeedstudio.com/XIAO_BLE/) 
    - CPU： [Nordic nRF52840](https://www.nordicsemi.com/products/nrf52840?lang=zh-TW)
    - 正面
    - 反面
    - 接腳定義
    - [擴充底板](https://wiki.seeedstudio.com/cn/Seeeduino-XIAO-Expansion-Board/)
    - 參考電路
    - 參考外形
    - 連接開發板

- [**快速操作指令表（方便快速複製貼上命令）**](https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024/blob/main/Ch12_Keyword_Spoting/Ch12_KWS_Quick_Guide.md)
    - Arduino 下載安裝設定測試
    - Edge Impulse 環境設定
    - Edge Impulse 喚醒詞案例

## 12.4.Edge_Impulse喚醒詞案例
- Edge Impulse
    - 簡介
    - 主要功能
    - 公用專案
    - 部落格文章
    - 說明文件
    - Expert network projects
    - 註冊/登入
- 下載及安裝必要工具
    - [Python 3.x](https://www.python.org/downloads/)
    - [Node.js (建議安裝v18.20.2 LTS)](https://nodejs.org/en/download/package-manager)
    - [Arduino CLI](https://arduino.github.io/arduino-cli/0.35/installation/)
- [安裝 Edge Impulse 工作環境](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli/cli-installation)
- 啟動公用專案範例 ─ [水流聲辨識](https://studio.edgeimpulse.com/public/14301/latest)
- 專案工作流程
    - 專案功能表
    - 資料集建置方式
- 喚醒詞案例
    - 建立 Edge Impulse 新專案
    - 檢查裝置是否已連線
    - 開始收集資料
    - 從裝置上傳資料限制
    - 直接上傳資料集
    - 大量收集樣本並分割成獨立可訓練樣本
    - 原始資料與自動分割
    - 反複收集分割，建立完整資料集
    - 選擇模型及設定必要參數
    - 提取資料特徵
    - 提取特徵結果
    - 設定分類訓練相關參數
    - 開始進行模型訓練及結果顯示
    - 線上測試（從內建測試集）
    - 選擇部署種類及設定參數
    - 導入 Arduino 函式庫並進行推論測試
    - 測試結果 (No Code型式)
    - 控制 LED 點滅 (Low Code型式)

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務  
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] 許哲豪， 【課程簡報】20221031_開南健管系_健康資料處理與分析_week08_穿戴式及健康照護感測器  
https://omnixri.blogspot.com/2022/11/20221031week08.html

[3] iThome 2021 (13屆) 鐵人賽【arm platforms組】完賽記錄 ─ 爭什麼，把AI和MCU摻在一起做tinyML就對了！  
https://omnixri.blogspot.com/2021/10/ithome-2021-13-arm-platforms-aimcutinyml.html

[4] 矽递科技(Seeed Studio) Wiki 文档平台 - XIAO nRF52840 (Sense) 开发板  
https://wiki.seeedstudio.com/cn/XIAO_BLE/

[5] Edge Impulse, Developers Document  
https://docs.edgeimpulse.com/

## 延伸閱讀

[A] 許哲豪， 【課程簡報】20240509_慈濟醫資_穿戴式人工智慧工作坊_利用TinyML技術快速搭建微型智慧應用  
https://omnixri.blogspot.com/2024/05/20240509tinyml12.html

[B] 許哲豪，【vMaker Edge AI專欄 #14】 從CES 2024 看Edge AI及TinyML最新發展趨勢  
https://omnixri.blogspot.com/2024/02/vmaker-edge-ai-14-ces-2024-edge-aitinyml.html

[C] 許哲豪，TinyML(MCU AI)系列發文  
https://hackmd.io/@OmniXRI-Jack/series_articles#TinyMLMCU-AI%E7%B3%BB%E5%88%97

[D] Seeed, Learn TinyML using Wio Terminal and Arduino IDE #2 Audio Scene Recognition and Mobile Notifications  
https://www.seeedstudio.com/blog/2021/02/03/learn-tinyml-using-wio-terminal-and-arduino-ide-2-audio-scene-recognition-and-mobile-notifications/

## 教學資源

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。
