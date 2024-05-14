# OmniXRI's Edge AI & TinyML 小學堂 【第11講】實作案例 ─ 姿態估測
作者：許哲豪(Jack Hsu), 2024/05/14

**完整課程簡報：20240514_Course_11_OmniXRI_Jack.pdf**

**Youtube直播影片：https://youtube.com/live/7aGkeYT5LwU**

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 11.1.姿態估測簡介
- 姿態估測
- 姿態估測常見用途
- 姿態估測（人體關鍵點）資料集
- 姿態估測標註比較
- [MS COCO](https://cocodataset.org/#keypoints-2020) 關鍵點資料集
- MS COCO 關鍵點定義
- [OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose
) 基本介紹
- OpenPose 關鍵點定義 
- 姿態關鍵點轉換

## 11.2.姿態估測模型
- 人體姿態估測模型(OpenVINO OMZ)
    - [Intel's Pre-Trained Model](https://docs.openvino.ai/2024/omz_models_group_intel.html#human-pose-estimation-models)
    - [Public Pre-Trained Model](https://docs.openvino.ai/2024/omz_models_group_public.html#human-pose-estimation-models)
- [人體姿態估測模型(OpenVINO Notebooks)](https://openvinotoolkit.github.io/openvino_notebooks/)
    - YOLOv8 [姿態估測模型](https://docs.ultralytics.com/tasks/pose/)及[資料格式](https://docs.ultralytics.com/datasets/pose/
    )
    - [Yolov8 關鍵點定義](https://chtseng.wordpress.com/2023/07/14/yolov8-pose-estimation/) 
- [Google MediaPipe](https://developers.google.com/mediapipe)
    - [Github](https://github.com/google/mediapipe)
    - [Studio Demo](https://mediapipe-studio.webapps.google.com/home)

## 11.3.姿態估測評量
- OKS, AP, MPJPE

## 11.4.姿態估測實作
- [實作範例1 ─ Yolov8 姿態估測 (OpenVINO Colab)](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/yolov8-optimization/yolov8-keypoint-detection.ipynb)
- [實作範例2 ─手部特徵點偵測 (MediaPipe Colab)](https://colab.research.google.com/github/googlesamples/mediapipe/blob/main/examples/hand_landmarker/python/hand_landmarker.ipynb)
- [實作範例3 ─手勢辨識 (MediaPipe Colab)](https://colab.research.google.com/github/googlesamples/mediapipe/blob/main/examples/gesture_recognizer/python/gesture_recognizer.ipynb)
- [實作範例4 ─姿態特徵點偵測 (MediaPipe Colab)](https://colab.research.google.com/github/googlesamples/mediapipe/blob/main/examples/pose_landmarker/python/%5BMediaPipe_Python_Tasks%5D_Pose_Landmarker.ipynb)

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] Haoming Chen etc., 2D Human Pose Estimation: A Survey
https://arxiv.org/abs/2204.07370

[3] Microsoft, COCO Keypoints Dataset 
https://cocodataset.org/#keypoints-2020

[4] OpenPose, Github 
https://github.com/CMU-Perceptual-Computing-Lab/openpose

[5] Ultralytics, Yolov8 Docs – Pose Estimation
- Overview: https://docs.ultralytics.com/tasks/pose/
- Dataset: https://docs.ultralytics.com/datasets/pose/

[6] Google, MediaPipe
- Home: https://developers.google.com/mediapipe
- Demo: https://mediapipe-studio.webapps.google.com/home
- Github: https://github.com/google/mediapipe

## 延伸閱讀

[A] CH.Tseng, YOLOV8 Pose Estimation
https://chtseng.wordpress.com/2023/07/14/yolov8-pose-estimation/

[B] Roboflow, How to Train a Custom Ultralytics YOLOv8 Pose Estimation Model
https://blog.roboflow.com/train-a-custom-yolov8-pose-estimation-model/

[C] 許哲豪， 【vMaker Edge AI專欄 #05】Google MediaPipe快速上手 ─ 浮空手勢也能用來當作簡報播放器 
- https://omnixri.blogspot.com/2023/05/vmaker-edge-ai-05google-mediapipe.html
- https://github.com/OmniXRI/PPT_Gesture_Demo

## 教學資源

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。

