# OmniXRI's Edge AI & TinyML 小學堂 【第5講】開源模型推論工具
作者：許哲豪(Jack Hsu), 2024/4/2建立

**完整簡報： 20240402_Course_05_OmniXRI_Jack.pdf**  
**Youtube直播： https://youtu.be/6By3GXuEpFc**  

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

## 5.1.常見邊緣推論工具簡介

- 常見邊緣推論硬體  
- 邊緣硬體推論限制  
- 常見邊緣推論優化工具  
    - [Google TensorFlow Lite](https://www.tensorflow.org/lite?hl=zh-tw)  
    - [Nvidia TensorRT](https://developer.nvidia.com/tensorrt)  
    - [Intel OpenVINO](https://docs.openvino.ai)  
    - [Edge Impulse Studio](https://edge-impulse.gitbook.io/docs)  
    - [Arm CMSIS-NN](https://www.arm.com/zh-TW/technologies/cmsis)  

## 5.2.Intel-OpenVINO簡介

- 演進歷史  
- 架構簡介  
- 工作流程  
- 重大革新  
- [文件說明](https://docs.openvino.ai)  
- [下載安裝](https://www.intel.com/content/www/us/en/developer/tools/openvino-toolkit/download.html)  
- 範例來源  
    - [Interactive Tutorials(Python) 【Notebooks】](https://docs.openvino.ai/2024/learn-openvino/interactive-tutorials-python.html)
    - [Sample Applications(Python & C++)](https://docs.openvino.ai/2024/learn-openvino/openvino-samples.html)
    - [Open Model Zoo](https://docs.openvino.ai/2024/documentation/legacy-features/model-zoo.html)
        - [Intel's Pre-Trained](https://docs.openvino.ai/2024/omz_models_group_intel.html)
        - [Public Pre-Trained](https://docs.openvino.ai/2024/omz_models_group_public.html)
        - [Demos](https://docs.openvino.ai/2024/omz_demos.html)

## 5.3.OpenVINO-Notebooks簡介 

- 功能簡介
    - [Notebooks Page](https://openvinotoolkit.github.io/openvino_notebooks/)  
- 下載安裝  
    - [Windows](https://github.com/openvinotoolkit/openvino_notebooks/wiki/Windows)  
    - [Ubuntu](https://github.com/openvinotoolkit/openvino_notebooks/wiki/Ubuntu)  
- 執行畫面  
- 範例練習  
    - [Hello Image Classification](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/hello-world/hello-world.ipynb)
    - [免本機安裝, Colab範例](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/hello-world/hello-world.ipynb#scrollTo=bf29578c)

## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務  
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] 許哲豪，OpenVINO 2022大改版讓Edge AI玩出新花樣  
https://omnixri.blogspot.com/2022/08/openvino-2022edge-ai.html  

[3] 許哲豪，在Colab上安裝Python虛擬環境及OpenVINO 2022.1填坑心得  
https://omnixri.blogspot.com/2022/09/colabpythonopenvino-20221.html  

## 延伸閱讀

[A] 許哲豪，歐尼克斯實境互動工作室【系列發文】OpenVINO系列  
https://hackmd.io/@OmniXRI-Jack/series_articles#OpenVINO%E7%B3%BB%E5%88%97  

[B] 許哲豪，如何運行Intel OpenVINO Open Model Zoo（OMZ）範例於Google Colab上  
https://omnixri.blogspot.com/2024/02/intel-openvino-open-model-zooomzgoogle.html  

[C] 許哲豪，TinyML 核心函式庫 Arm CMSIS 6 DSP & NN 更新比較  
https://omnixri.blogspot.com/2024/02/tinyml-arm-cmsis-6-dsp-nn.html  

## 教學資源

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。

