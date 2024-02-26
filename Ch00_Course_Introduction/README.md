# OmniXRI's Edge AI & TinyML 小學堂 【第0講】課程簡介

**<font color=red>本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 1. 課程源起

2012年深度學習開啟了新的人工智慧浪潮，CNN, RNN, GAN, SNN等技術讓人充份感受到AI的實用性，開始大量引入日常生活中。2022年底OpenAI以ChatGPT帶動了大型語言模型(LLM)及生成式AI（GenAI, AIGC）的重大革新，讓全世界都瘋狂投入。2024年2月台大資工李宏毅老師開設了「生成式AI導論」，一口氣線上加線下來了二千多位同學，不分科系共同參與，其熱門程度不輸明星演唱會。

![NTU_AIGC_course](https://hackmd.io/_uploads/Syblijthp.jpg =400x)

![NTU_AIGC_course02](https://hackmd.io/_uploads/r1jmojt2T.jpg =400x)

台大李宏毅老師「生成式AI導論」上課影像。[[影像來源]](https://www.facebook.com/groups/aigctw/posts/2528159394034624/)

不過在「邊緣智慧裝置」可能就不太受重視了，就像馬路上超跑總是吸引大家的目光，瘋狂追捧，而自行車和機車雖然實用，卻只有少數廠商願意投入，因為有限的硬體算力、運行功耗、產品單價及太過專業跨域的知識、開發工具，加上未來就業市場的影響，自然教育單位就很少老師及學生願意投入。

三年前個人受恩師推薦，有幸在台科大資工系產碩專班連續三年開設[「人工智慧與邊緣運算實務」](https://omnixri.blogspot.com/p/ntust-edge-ai.html)。隨著學程的結束，本來以為應該不會再幫大家上課，但最近受到一百多位網友的「+1」號召，於是起心動念，決定免費開設YOUTUBE直播課程，幫大家建立基礎知識，希望能藉此推廣相關技術，滿足台灣在這個領域不足的地方。

## 2. 課程簡介

智慧物聯網(AIoT)已推動多年，但其AI多半在雲端。隨著半導體技術及軟體工具平台逐漸成熟，因此已有很多微型AI應用已可移至邊緣端。目前「邊緣人工智慧(Edge AI)」主要分為「嵌入式(Embedded AI, TinyML, MCU AI)」、「行動式(Mobile AI)」及最新的人工智慧筆電(AI PC)。本課程將聚焦在使用電池、可斷網獨立推論的硬體、算法，尤其是使用筆電、手機、單板微電腦及單晶片的微型AI應用。

本課程定位為<font color=blue>**初階學習者**</font>，沒有太多AI或程式基礎亦可學習。前半段將依序從基礎深度學習理論、硬體選用、資料集建置、客製化模型訓練、優化到推論環境佈署。後半段則以案例實作為主，帶領大家如何利用各種開源工具來完成邊緣智慧應用，包括OpenCV, Google Colab, TensorFlow Lite, Intel OpenVINO, Nvidia TensorRT, Edge Impulse等。

:::info 
YOUTUBE 課程直播時間： 2024/3/5 ~ 2024/6/18，每週二晚上20：00 ~ 21：00，一小時課程（可視情況彈性延長半小時問答），共16週。
如遇特殊狀況需調整上課時間，會另行公告處理方式。
:::

## 3. 講師簡介

![](https://1.bp.blogspot.com/-ZnmpktLAa2w/X-qQHv8N0XI/AAAAAAAADFA/AfjqWTikyAkMF2KhxDQW9pHN6r9PSCA7QCLcBGAsYHQ/w200-h200/JackHsu.png)

**許哲豪 (Jack Hsu) 博士**

連絡方式： 
- 電子郵件： [omnixri@gmail.com](mailto:omnixri@gmail.com)

個人簡介：
- [歐尼克斯實境互動工作室(OmniXRI Studio)](https://omnixri.blogspot.com/) 創辦人
- Facebook [【Edge AI Taiwan邊緣智能交流區】](https://www.facebook.com/groups/edgeaitw) 社團創辦人
- Intel 創新大使（台灣地區首位, 2023 ~ now）
- [MakerPRO](https://makerpro.cc/jack-hsu-column/), [vMaker](https://vmaker.tw/archives/category/%e5%b0%88%e6%ac%84/jack-omnixri)等單位Edge AI專欄作家
- 多家公司兼任技術/新創顧問

專長：
機電整合、半導體封裝、電腦視覺、立體顯示、實境互動、人工智慧、智財技轉、新創輔導。

經歷：
- 臺灣科技大學 資訊工程系 產碩專班 「人工智慧與邊緣運算實務」 兼任助理教授 (2021/2 ~ 2023/6)
- 開南大學 健康產業管理系 健康產業應用課程 「健康資料處理與分析」、「智慧醫療」 協同計畫主持人暨部份課程教學講師 (2022/9 ~ 2023/6)
- 開源人年會 Coscup 2023 【Open Edge AI & TinyML】 議程召集人 (2023/7)
- 2019 【Intel OpenVINO x Edge AI 創意應用競賽】 課程講師/活動顧問/競賽評審

榮譽：
- iThome 2021(13屆) 鐵人賽【Arm Platforms組】 冠軍
    「爭什麼，把AI和MCU摻在一起做tinyML就對了」 （筆名：史蒂芬周）  

## 4. 課程大綱

本課程大綱主要參考台科大[「人工智慧與邊緣運算實務」](https://omnixri.blogspot.com/p/ntust-edge-ai.html)進行規畫，大家可先作預習。目前大綱為預定內容，僅供參考，實際內容會隨課程展開後進行微調。

所有課程簡報、範例、影片會於課後提供相關連結，並發佈到 FB Group, Blogger, Medium, Hackmd 等媒體，方便大家透過習慣的管道學習。

**註一：** 大部份範例實作課程會使用Google Colab雲端範例，少部份實作課程會使用到特定硬體，會於課前說明，請自行準備。
**註二：** 本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。

- **<font color=blue>2024/03/05</font>** Ch_0 課程簡介 [簡報] [影片]
- **<font color=blue>2024/03/05</font>** Ch_01 邊緣人工智慧簡介 [簡報] [影片]
    1.1 人工智慧
    1.2 機器學習
    1.3 深度學習
    1.4 生成式智慧
- **<font color=blue>2024/03/12</font>** Ch_02 邊緣運算硬體 [簡報] [影片]
    2.1 基本運算原理
    2.2 加速運算晶片
    2.3 開發板類型
    2.4 硬體選用評估
- **<font color=blue>2024/03/19</font>** Ch_03 資料集建置與標註 [簡報] [影片]
    3.1 資料集建置
    3.2 公開資料集
    3.3 資料集標註
    3.4 資料集迷思
- **<font color=blue>2024/03/26</font>** Ch_04 開源模型訓練工具 [簡報] [影片]
    4.1 AI工作流程
    4.2 常見模型算法
    4.3 開源訓練工具
    4.4 影像分類範例
- **<font color=blue>2024/04/02</font>** Ch_05 開源模型推論工具 [簡報] [影片]
    5.1 邊緣推論工具簡介
    5.2 OpenVINO簡介
    5.3 OpenVINO多媒體處理
    5.4 OpenVINO Notebooks
- **<font color=blue>2024/04/09</font>** Ch_06 模型優化與佈署 [簡報] [影片]
    6.1 模型訓練優化
    6.2 加速訓練方式
    6.3 模型推論優化
    6.4 OpenVINO優化工具
- **<font color=blue>2024/04/16</font>** Ch_07 微型機器學習簡介
    7.1 嵌入式系統與微控制器
    7.2 TinyML技術現況
    7.3 TinyML開發平台
    7.4 TinyML主要應用
- **<font color=blue>2024/04/23</font>** Ch_08 實作案例 ─ 影像分類 [簡報] [影片]
- **<font color=blue>2024/04/30</font>** Ch_09 實作案例 ─ 物件偵測 [簡報] [影片]
- **<font color=blue>2024/05/07</font>** Ch_10 實作案例 ─ 影像分割 [簡報] [影片]
- **<font color=blue>2024/05/14</font>** Ch_11 實作案例 ─ 姿態估測 [簡報] [影片]
- **<font color=blue>2024/05/21</font>** Ch_12 實作案例 ─ 語音辨識 [簡報] [影片]
- **<font color=blue>2024/05/28</font>** Ch_13 實作案例 ─ 運動辨識 [簡報] [影片]
- **<font color=blue>2024/06/04</font>** Ch_14 實作案例 ─ 異常偵測 [簡報] [影片]
- **<font color=blue>2024/06/11</font>** Ch_15 實作案例 ─ 文字語音生成 [簡報] [影片]
- **<font color=blue>2024/06/18</font>** Ch_16 實作案例 ─ 影像音樂生成 [簡報] [影片]

## 教學資源

許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務 (2021~2023)  
https://omnixri.blogspot.com/p/ntust-edge-ai.html

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

