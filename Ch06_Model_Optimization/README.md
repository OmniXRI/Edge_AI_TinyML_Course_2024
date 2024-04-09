# OmniXRI's Edge AI & TinyML 小學堂 【第6講】模型優化與佈署
作者：許哲豪(Jack Hsu), 2024/4/9建立

**完整課程簡報： 20240409_Course_06_OmniXRI_Jack.pdf**  

**Youtube直播： https://youtu.be/vzJqu8OAu9U**

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 6.1.模型訓練優化
- 數值擬合
- 輸出型式
    - 序數(Ordinal Encoding)
    - 獨熱(One-Hot Encoding)
    - 歸一化指數函數(Softmax)
- 損失函數
    - 平均絕對誤差(MAE)
    - 均方誤差(MSE)
    - 均方根誤差(RMSE)
    - 交叉熵(Cross-Entropy)
- 反向傳播
- 梯度下降 
    - 極值、梯度
    - 學習率
    - 常見優化器調整方式
    - BGD / SGD / MBGD
    - Adagrad
    - RMSProp
- 慣性動量
    - Momentum
    - Adam
    - 實驗比較
- 隨機丟棄

## 6.2.加速訓練方式
- 低複雜度模型
- 遷移式學習
    - [Microsoft Lobe.ai](https://www.lobe.ai/)
    - [Google Teachable Machine](https://teachablemachine.withgoogle.com/)
- 自動學習
- 分散式學習
    - 並行學習
    - 聯邦學習

## 6.3.模型推論優化
- 數值量化
- 模型剪枝
- 模型壓縮
    - 權重共享
    - 低秩逼近
    - 標準卷積
    - 快速卷積
- 知識蒸餾

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務
https://omnixri.blogspot.com/p/ntust-edge-ai.html

## 延伸閱讀

[A] 陽明交通大學電子工程學系張添烜老師，「深度學習的模型壓縮與加速」(YouTube)
https://www.youtube.com/watch?v=LlJQ_agQJyM&list=PLj6E8qlqmkFv3cCjjX2SA1D4FJ9fadDij

[B] MIT Han Lab (韓松）,「TinyML and Efficient Deep Learning Computing | MIT 6.S965 Fall 2022」(Youtube)
https://www.youtube.com/watch?v=5HpLyZd1h0Q&list=PL80kAHvQbh-ocildRaxjjBy6MR1ZsNCU7

## 教學資源：

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。
