# OmniXRI's Edge AI & TinyML 小學堂 【第10講】實作案例 ─ 影像分割
作者：許哲豪(Jack Hsu), 2024/05/07

**完整課程簡報：20240507_Course_10_OmniXRI_Jack.pdf**  

**Youtbue直播：https://youtu.be/a0fa86d-Irc**  

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 10.1.影像分割簡介  
- 影像分割（像素級分類）類型
    - 語義分割、實例分割、全景分割
- 傳統影像分割技術
    - 尋找邊界、特定封閉區域、特徵區域提取、像素聚類
- OpenCV常用影像分割算法
    - 中心聚類、中心移位、分水嶺、互動式分割、超像素
- 影像分割標註
    - 常見影像分割標註方式
    - 影像分割標註工具
        - [PixelAnnotationTool](https://github.com/abreheret/PixelAnnotationTool)
        - [superpixels-segmentation](https://github.com/Labelbox/superpixels-segmentation)
        - [semantic-segmentation-editor](https://github.com/Hitachi-Automotive-And-Industry-Lab/semantic-segmentation-editor) 
    - VOC語義分割資料格式
    - PNG8 (Indexed, Palette)格式
    - COCO語義分割資料格式

## 10.2.影像分割模型   
- 深度學習影像分割技術演進
- 常見語義分割技術
    - 常見語義分割模型 FCN
    - 常見語義分割模型 U-Net
    - 常見語義分割模型 DeepLabV3+
- 常見實例分割技術
    - 實例分割技術演進
    - 常見實例分割模型 R-CNN 
    - 常見實例分割模型 Yolact & Edge
    - 常見實例分割 YOLO系列
    - 提示式分割 Meat SAM

## 10.3.影像分割評量   
- 像素級
- DICE Coefficient

## 10.4.影像分割實作  
- [Intel OpenVINO Open Model Zoo - Image Segmentation](https://docs.openvino.ai/2024/omz_models_group_public.html#segmentation-models)
- [Intel OpenVINO Notebooks - Image Segmentation](https://openvinotoolkit.github.io/openvino_notebooks/)
- 實作範例
    - [實作範例1 ─ 路況實例分割 (colab)](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/hello-segmentation/hello-segmentation.ipynb)
    - [實作範例2 ─ YOLOv8實例分割 (Colab)](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/yolov8-optimization/yolov8-instance-segmentation.ipynb)
    - [實作範例3 ─物件分割 FastSAM (Colab)](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/fast-segment-anything/fast-segment-anything.ipynb)

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] 許哲豪，【AI HUB專欄】如何建立精準標註的電腦視覺資料集
https://omnixri.blogspot.com/2020/10/ai-hub_16.html

[3] Shervin Minaee etc., Image Segmentation Using Deep Learning: A Survey
https://arxiv.org/abs/2001.05566

[4] Abdul Mueed Hafiz etc., A Survey on Instance Segmentation: State of the art
https://arxiv.org/abs/2007.00047

## 延伸閱讀

[A] 武卓，AI分割一切：用OpenVINO加速Meta SAM大模型
https://makerpro.cc/2023/05/openvino-accelerated-meta-segment-anything-model/

[B] Sunidhi Ashtekar, Dynamic Object Detection and Segmentation with YOLOv9+SAM
https://medium.com/@sunidhi.ashtekar/dynamic-object-detection-and-segmentation-with-yolov9-sam-de258238546f


## 教學資源

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。
