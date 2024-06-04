# OmniXRI's Edge AI & TinyML 小學堂 【第14講】實作案例 ─ 異常偵測
作者：許哲豪(Jack Hsu), 2024/06/04

**完整課程簡報：20240604_Course_14_OmniXRI_Jack.pdf**

**Youtube直播影片：https://youtube.com/live/c9q_zik-L8o**

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 14.1.異常偵測技術簡介
- 何謂異常偵測（離群偵測）
- 常見一元異常偵測 
    - 基於支持向量機式(SVM)
    - 基於自動編碼器式(AE)
    - 基於生成對抗網路式(GAN)
- 時序型資料分解
- 常見時序異常偵測 
    - 傳統統計型(AR, VAR, MA, ARIMA)
    - 機器學習型(K-Mean, DBSCAN, LOF, IF)
    - 深度學習型(CNN, LSTM, GRU, AE)
- 影像異常偵測（瑕疵檢測）
    - 深度學習型(影像分類, 物件偵測, 影像分割)
    - 語義分割型（完全卷積網路, 編碼/解碼網路, 分割/決策網路
- 常見資料距離量測
    - 歐幾里德距離, 馬哈拉諾比斯距離, 餘弦距離
- [MLCommons Tiny - Anomaly Detection](https://mlcommons.org/benchmarks/inference-tiny/)

## 14.2.異常偵測開源資源
- [MVTec anomaly detection dataset](https://www.mvtec.com/company/research/datasets/mvtec-ad/)
- [Anomalib](https://github.com/openvinotoolkit/anomalib)
- Edge Impulse 異常偵測開源案例
    - [Experts Network Projects](https://docs.edgeimpulse.com/experts)
    - [Optimize a cloud-based Visual Anomaly Detection Model for Edge Deployments](https://docs.edgeimpulse.com/experts/featured-machine-learning-projects/fomo-ad-in-aws)
    - [Brushless DC Motor Anomaly Detection](https://docs.edgeimpulse.com/experts/predictive-maintenance-and-fault-classification/brushless-dc-motor-anomaly-detection)
    - [Continuous Gait Monitor (Anomaly Detection)-Nordic Thingy:53](https://docs.edgeimpulse.com/experts/accelerometer-and-activity-projects/continuous-gait-monitor-nordic-thingy53)
    - [BrickML Demo Project - 3D Printer Anomaly Detection](https://docs.edgeimpulse.com/experts/predictive-maintenance-and-fault-classification/brickml-3d-printer-anomaly-detection)
- [Edge Impulse Anomaly Detection Block](https://docs.edgeimpulse.com/docs/edge-impulse-studio/learning-blocks)

## 14.3.常見MCU_AI視覺模組
- [2022](https://omnixri.blogspot.com/2022/12/tinymlmcu.html)
- 2024
- [2024 性能比較](https://www.hackster.io/limengdu0117/2024-mcu-ai-vision-boards-performance-comparison-998505)

## 14.4.異常影像偵測案例

### 14.4.1 Edge Impulse FOMO-AD 水五金異常偵測案例
- 範例資源
    - [學習模組─Visual anomaly detection (FOMO-AD)](https://docs.edgeimpulse.com/docs/edge-impulse-studio/learning-blocks/visual-anomaly-detection)
    - [說明文章](https://www.edgeimpulse.com/blog/announcing-visual-anomaly-detection/)
    - [公開範例](https://studio.edgeimpulse.com/public/377568/live)
- Data Acquisition
- Impulse Design
- Model Training
- Live Test

### 14.4.2 Seeed Vision AI Module V2 + Seeed SenseCraft 應用例
- 實驗器材 
    - [Seeed Vision AI Module V2](https://wiki.seeedstudio.com/grove_vision_ai_v2/)
    - [Himax WiseEyes2 HX6538](https://www.himax.com.tw/products/wiseeye-ai-sensing/wiseeye2-ai-processor/)
- 安裝序列埠驅動程式
    - [Windows Driver](https://wiki.seeedstudio.com/grove_vision_ai_v2/)
- Seeed Vision AI Module V2 開發資源
    - [Seeed WIKI ─ Grove – Vision AI V2 (英文版)](https://wiki.seeedstudio.com/grove_vision_ai_v2/)
    - [矽遞科技 WIKI 文檔平台 ─ Grove – Vision AI V2 模塊人工智能(簡中版)](https://wiki.seeedstudio.com/cn/grove_vision_ai_v2/)
    - [Seeed, SenseCraft AI](https://sensecraft.seeed.cc/ai/#/home)
    - [Github, Himax WiseEye Plus – Seeed_Grove_Vision_AI_Module_V2](https://github.com/HimaxWiseEyePlus/Seeed_Grove_Vision_AI_Module_V2)
- [Seeed SenseCraft AI](https://sensecraft.seeed.cc/ai/#/model) 
    - 選擇裝置及模型
    - 模型部署
    - 連接、上傳、測試

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] 許哲豪，有了TinyML加持MCU也能開始玩電腦視覺了
https://omnixri.blogspot.com/2022/12/tinymlmcu.html

[3] Himax, WiseEye2 AI Processor (WE2) (HX6538)
https://www.himax.com.tw/products/wiseeye-ai-sensing/wiseeye2-ai-processor/

[4] Seeed, Grove - Vision AI V2模块人工智能
https://wiki.seeedstudio.com/cn/grove_vision_ai_v2/

[5] Seeed, SenseCraft AI
https://sensecraft.seeed.cc/ai/#/home

[6] Edge Impulse Document – Seeed Grove – Vision AI Module
https://docs.edgeimpulse.com/docs/edge-ai-hardware/mcu-+-ai-accelerators/seeed-grove-vision-ai

## 延伸閱讀

[A] 許哲豪，【AI HUB專欄】導入AI異常偵測技術讓傳產也能邁向智慧製造
https://omnixri.blogspot.com/2020/06/ai-hubai.html

[B] 許哲豪，【AI HUB專欄】如何利用時序型資料異常偵測提昇智慧製造成效
https://omnixri.blogspot.com/2020/06/ai-hub.html

[C] 許哲豪，【AI HUB專欄】導入AI表面瑕疵異常偵測提升智慧製造品質
https://omnixri.blogspot.com/2020/07/ai-hubai.html

[D] 許哲豪，【AI HUB專欄】生成對抗網路不只能變臉也能成為異常偵測好幫手
https://omnixri.blogspot.com/2020/08/ai-hub.html

[E] 許哲豪，【AI HUB專欄】利用深度學習技術讓裂縫無所遁形
https://omnixri.blogspot.com/2020/11/ai-hub_23.html

[F] 許哲豪，【AI HUB專欄】介於有和沒有之間的深度度量學習應用於異常偵測
https://omnixri.blogspot.com/2020/12/ai-hub.html

## 教學資源

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。

