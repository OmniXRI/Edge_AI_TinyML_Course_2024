# OmniXRI's Edge AI & TinyML 小學堂 【第7講】微型機器學習簡介
作者：許哲豪(Jack Hsu), 2024/4/16

**完整課程簡報：20240416_Course_07_OmniXRI_Jack.pdf**  

**Youtube直播：https://youtu.be/5ln7UT5pzFs**  

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 7.1.嵌入式系統與微控制器
- 微型機器學習與生成智慧 
- 嵌入式人工智慧定位
- 嵌入式系統架構 
- 單晶片架構與指令集 
    - [MCU主要分類方式](https://omnixri.blogspot.com/2021/09/aiottinymlmcu.html)
    - [Arm Cortex-M指令集對照表](https://omnixri.blogspot.com/2024/01/vmaker-edge-ai-13-npuai.html)
    - [全國十大MCU供應商（Q3 2023）](https://36kr.com/p/2528780809938432)
    - [STM32 MCUs 32bit Arm Cortex-M系列](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html)
    - [台灣通用型MCU主要供應商 (2021/9)](https://omnixri.blogspot.com/2021/09/aiottinymlmcu.html)
    - [Arm Based MCU + NPU解決方案](https://omnixri.blogspot.com/2024/02/vmaker-edge-ai-14-ces-2024-edge-aitinyml.html)
    - 智慧單晶片（MCU+NPU）

## 7.2.TinyML技術現況
- 何謂微型機器學習 (TinyML)
    - [tinyML基金會2023主要贊助商](https://www.tinyml.org/)
- TinyML應用限制
- TinyML加速運算
    - [硬體增速](https://omnixri.blogspot.com/2022/10/20221021ai.html)
    - [Arm Cortex-M 指令集與加速計算比較](https://omnixri.blogspot.com/2024/01/vmaker-edge-ai-13-npuai.html)
    - [模型優化 (AutoML)](https://edge-impulse.gitbook.io/docs/edge-impulse-studio/eon-tuner)
- TinyML效能評比
    - [MLPerf Tiny](https://mlcommons.org/benchmarks/inference-tiny/)
    - [MLPerf Tiny v1.1 評比結果 （2023/6）](https://omnixri.blogspot.com/2023/07/vmaker-edge-ai-07tinyml-mcu-ai.html)

## 7.3.TinyML開發平台 
- [開發流程簡介](https://omnixri.blogspot.com/2021/09/aiottinymlmcu.html)
- [軟體堆疊架構](https://omnixri.blogspot.com/2022/07/20220731coscupaimcutinyml.html)
- 常見開發工具
    - NCU專屬式工具
    - MCU硬體廠收購TinyML軟體開發商
    - [Edge Impulse TinyML雲端開發平台](https://edgeimpulse.com/)
- 常見開發板
    - [Arduino PRO 系列](https://www.arduino.cc/pro/platform-hardware/)
    - [Seeed Xiao 系列](https://wiki.seeedstudio.com/cn/SeeedStudio_XIAO_Series_Introduction/)
    - [具攝影機](https://omnixri.blogspot.com/2022/12/tinymlmcu.html)

## 7.4.TinyML主要應用
- [聲音感測](https://hackmd.io/HrRb2hthRkOC1_K6IDGn5w#1-%E8%81%B2%E9%9F%B3%E6%84%9F%E6%B8%AC8)
- [運動感測](https://hackmd.io/HrRb2hthRkOC1_K6IDGn5w#2-%E9%81%8B%E5%8B%95%E6%84%9F%E6%B8%AC7)
- [環境感測](https://hackmd.io/HrRb2hthRkOC1_K6IDGn5w#3-%E7%92%B0%E5%A2%83%E6%84%9F%E6%B8%AC5)
- [視覺感測](https://hackmd.io/HrRb2hthRkOC1_K6IDGn5w#4-%E8%A6%96%E8%A6%BA%E6%84%9F%E6%B8%AC10)
- [時序預測](https://www.hackster.io/mjrobot/temperature-prediction-using-a-tinyml-lstm-model-264029)

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務  
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] 許哲豪，當智慧物聯網(AIoT)遇上微型機器學習(tinyML)是否會成為台灣單晶片(MCU)供應鏈下一個新商機！？  
https://omnixri.blogspot.com/2021/09/aiottinymlmcu.html

[3] 許哲豪， MCU攜手NPU讓tinyML邁向新里程碑  
https://omnixri.blogspot.com/2022/10/mcunputinyml.html

[4] 許哲豪，有了TinyML加持MCU也能開始玩電腦視覺了  
https://omnixri.blogspot.com/2022/12/tinymlmcu.html

[5] 許哲豪，TinyML應用大全（30組案例分享）  
https://hackmd.io/@OmniXRI-Jack/tinyML_30_projects

## 延伸閱讀

[A] Wevolver, 2024 State of Edge AI Report  
https://www.wevolver.com/article/2024-state-of-edge-ai-report/introduction

[B] 許哲豪，【vMaker Edge AI專欄 #14】 從CES 2024 看Edge AI及TinyML最新發展趨勢  
https://omnixri.blogspot.com/2024/02/vmaker-edge-ai-14-ces-2024-edge-aitinyml.html

[C] 許哲豪，【vMaker Edge AI專欄 #13】 誰說單晶片沒有神經網路加速器NPU就不能玩微型AI應用？  
https://omnixri.blogspot.com/2024/01/vmaker-edge-ai-13-npuai.html

[D] 許哲豪，【vMaker Edge AI專欄 #07】TinyML (MCU AI) 運行效能誰說了算？  
https://omnixri.blogspot.com/2023/07/vmaker-edge-ai-07tinyml-mcu-ai.html

[E] 許哲豪， 【心得筆記】Edge Impulse EON Tuner AutoML工具介紹  
https://omnixri.blogspot.com/2022/05/edge-impulse-eon-tuner-automl.html

[F] 許哲豪，TinyML相關學術論文  
https://hackmd.io/@OmniXRI-Jack/tinyML_papers

## 教學資源：

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。
