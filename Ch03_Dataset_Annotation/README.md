# OmniXRI's Edge AI & TinyML 小學堂 【第3講】資料集建置與標註
作者：許哲豪(Jack Hsu), 2024/03/19

**完整簡報： 20240319_Course_03_OmniXRI_Jack.pdf**
**YOUTUBE直播： https://youtu.be/d655nS-0XmM**

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 3.1.資料集建置
- 工作流程
- 資料類型
    - 應用情境
    - 資料結構
    - 感測器
- 資料取得
- 資料擴增
    - 影像處理式
    - 影像拼貼式
    - 影像生成式
    - 時序資料

## 3.2.公開資料集
- 常見影像資料集
    - MNIST 
    - CIFAR-10
    - [Pascal VOC](http://host.robots.ox.ac.uk/pascal/VOC/)
    - [ImageNet](http://image-net.org/)
    - [Microsoft COCO](https://cocodataset.org/)
- 常見聲音資料集
    - [Google Speech Command](https://www.tensorflow.org/datasets/catalog/speech_commands)
    - [ESC-50](https://github.com/karolpiczak/ESC-50)
    - [Google AudioSet](https://research.google.com/audioset/index.html)
- 其它公開資料集
    - [TensorFlow](https://www.tensorflow.org/datasets?hl=zh-tw)
    - [PyTorch](https://pytorch.org/vision/main/datasets.html)
    - [Kaggle](https://www.kaggle.com/datasets)
    - [Papers with Code](https://paperswithcode.com/datasets)
    - [Hugging Face](https://huggingface.co/datasets)
    - 台灣相關
        - [國網中心資料集平台](https://scidm.nchc.org.tw/)
        - [政府資料開放平台](https://data.gov.tw/)
        - [AI Cup 教育部全國大專校院人工智慧競賽](https://www.aicup.tw/)

## 3.3.資料集標註 
- 影像標註類型
    - 依工作內容
    - 依標註外形
    - 依時序內插
- 影像標註格式
    - Pascal VOC (xml)
    - MS COCO (json)
    - YOLO (txt)
    - 旋轉物件標註 (xml) 
- 影像標註工具
    - [LabelImg](https://github.com/tzutalin/labelImg)
    - [Intel CVAT](https://www.cvat.ai/)
    - [Roboflow](https://roboflow.com/)
    - 其它
        - [Segment Anything Model](https://segment-anything.com/)

## 3.4.資料集迷思
- 資料增長
- 標註水準
- 子集不均
- 自動聚類

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] 許哲豪，【AI HUB專欄】如何建立精準標註的電腦視覺資料集
https://omnixri.blogspot.com/2020/10/ai-hub_16.html

[3] 許哲豪，【課程簡報分享】AI萬能？導入AI的八大迷思剖析
https://omnixri.blogspot.com/2019/08/aiai.html

[4] 許哲豪，【vMaker Edge AI專欄 #10】訓練AI模型資料不足怎麼辦？聊聊資料集擴增手法
https://omnixri.blogspot.com/2023/10/vmaker-edge-ai-10-ai.html

## 延伸閱讀

[A] Intel, CVAT Computer Vision Annotation Tool | OpenVINO™ toolkit | Ep. 51 | Intel Software (Youtube)
https://www.youtube.com/watch?v=BKLyHOEACFw

[B] Intel, CVAT Auto Annotation | OpenVINO™ toolkit | Ep. 52 | Intel Software (Youtube)
https://www.youtube.com/watch?v=jbqOa8DX7Jg

[C] MakerPro, 【Roboflow標記工具】新手也能輕鬆上手，打造專業AI資料集的線上指南！
https://makerpro.cc/2024/01/roboflow-marking-tool-is-easy-to-use/

## 教學資源：

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。
