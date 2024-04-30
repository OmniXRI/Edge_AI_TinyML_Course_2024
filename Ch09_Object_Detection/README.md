# OmniXRI's Edge AI & TinyML 小學堂 【第9講】實作案例 ─ 物件偵測
作者：許哲豪(Jack Hsu), 2024/04/30

**完整課程簡報：20240430_Course_09_OmniXRI_Jack.pdf**

**完整直播影片：https://youtu.be/HHAaZRIIoCg**

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**
  
## 9.1.物件偵測簡介
- 物件偵測演進史
- 二階式 vs. 一階式 物件偵測
- 候選區域(Region Proposals)
- YOLO vs. YOLO
- YOLO 物件偵測模型發展歷程
- YOLOv7 / v8 / v9 功能擴增
- Yolo-World 基本概念   

## 9.2.物件偵測模型
- 常見物件偵測模型
- [OpenVINO Open Model Zoo 範例](https://docs.openvino.ai/2024/omz_models_group_public.html#object-detection-models)
- [Open Model Zoo – ssd_mobilenet_v1_coco](https://docs.openvino.ai/2024/omz_models_model_ssd_mobilenet_v1_coco.html)
- [OpenVINO Notebooks 範例](https://openvinotoolkit.github.io/openvino_notebooks/)

## 9.3.物件偵測評量 
- Accuracy / Precision / Recall / F1 Score / mAP
- IoU

## 9.4.物件偵測實作
- [實作範例1 ─ YOLOv8物件偵測 (Colab)](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/yolov8-optimization/yolov8-object-detection.ipynb)
- [實作範例2 ─ YOLOv8 OBB (Colab)](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/yolov8-optimization/yolov8-obb.ipynb)
    - [DOTA Dataset](https://captain-whu.github.io/DOTA/)
- [實作範例3 ─ 即時影像辨識 (Colab)](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/object-detection-webcam/object-detection.ipynb)

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務  
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] pyimagesearch - Introduction to the YOLO Family  
https://pyimagesearch.com/2022/04/04/introduction-to-the-yolo-family/

[3] 許哲豪，【vMaker Edge AI專欄 #16】AIPC開箱實測 ─ Yolov8斜物件偵測  
https://omnixri.blogspot.com/2024/04/vmaker-edge-ai-16aipc-yolov8.html

## 延伸閱讀

[A] 許哲豪，如何以Google Colab及Yolov4-tiny來訓練自定義資料集─以狗臉、貓臉、人臉偵測為例  
https://omnixri.blogspot.com/2021/05/google-colabyolov4-tiny.html

[2] 李謦伊，謦伊的閱讀筆記（YOLO）  
https://medium.com/ching-i/tagged/yolo

## 教學資源：

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。
