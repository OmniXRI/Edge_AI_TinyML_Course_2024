# OmniXRI's Edge AI & TinyML 小學堂 【第16講】實作案例 ─ 影像音樂生成
作者：許哲豪(Jack Hsu), 2024/06/18

**完整課程簡報：20240618_Course_16_OmniXRI_Jack.pdf**  

**Youtube直播影片：https://youtu.be/K3MreTE7EKI**  

**<font color="#f00">本課程完全免費，請勿移作商業用途！更多課程內容請參考文末教學資源連結。歡迎追蹤、留言、訂閱、點讚、轉發，讓更多需要的朋友也能一起學習。</font>**

- [Intel OpenVINO & Notebooks 回顧](https://youtu.be/6By3GXuEpFc)
- [Intel OpenVINO Notebooks Windows安裝](https://github.com/openvinotoolkit/openvino_notebooks/wiki/Windows)
- [Intel OpenVINO Notebooks 範例程式網頁](https://openvinotoolkit.github.io/openvino_notebooks/)

## 16.1.常見影像生成應用
- GAN & Transformer
    - [MyEdit](https://myedit.online/tw/photo-editor/ai-image-generator), [Midjourney](https://www.midjourney.com/home), [DALL·E3](https://openai.com/index/dall-e-3/), [Stable Diffusion](https://stability.ai/), [NovelAI](https://novelai.net/), [Stableboost](https://serp.ai/tools/stableboost/), [Fotor](https://www.fotor.com/tw/), [Adobe Firefly](https://www.adobe.com/tw/products/firefly/features/ai-painting-generator.html), [Leonardo AI](https://leonardo.ai/), [Craiyon](https://www.craiyon.com/), [DreamStudio](https://beta.dreamstudio.ai/generate), [Canva](https://www.canva.com/)
- 影像生成 ─ 生成對抗網路(GAN)
- 影像生成 ─ Stable Diffusion
- 影像生成 ─ U-Net & VAE
- Meteor Lake運行影像生成效能比較
- OpenVINO Notebooks Device 設定

## 16.2.影像生成應用實例
- 影像生成應用實例 ─ Tiny SD 文生圖
- 影像生成應用實例 ─ Tiny SD 圖生圖
- 影像生成應用實例 ─ Tiny SD 互動介面
- 範例1： [Image Generation with Tiny-SD and OpenVINO(Colab)](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/tiny-sd-image-generation/tiny-sd-image-generation.ipynb)
- 影像生成應用實例 ─ ControlNet 圖生圖
- 影像生成應用實例 ─ ControlNet 結果
- 影像生成應用實例 ─ ControlNet 互動介面
- 範例2： [Text-to-Image Generation with ControlNet Conditioning(Local)](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/controlnet-stable-diffusion/controlnet-stable-diffusion.ipynb)
- 影像生成應用實例 ─ Infinite Zoom
- 影像生成應用實例 ─ Infinite Zoom 工作流程
- 影像生成應用實例 ─ Infinite Zoom 互動介面
- 範例3： [Infinite Zoom Stable Diffusion v2 and OpenVINO(Loacal)](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/stable-diffusion-v2/stable-diffusion-v2-infinite-zoom.ipynb
)

## 16.3.常見音樂生成應用
- 常見音樂生成應用
    - [MyEdit](https://myedit.online/tw/audio-editor/ai-sound-effect-generator), [Stable Audio](https://www.stableaudio.com/), [Suno AI](https://suno.com/), [Soundraw](https://soundraw.io/), [Boomy](https://boomy.com/), [Riffusion](https://www.riffusion.com/), [Voicemod](https://www.voicemod.net/zh/), [Loudly](https://www.loudly.com/), [Covers AI](https://covers.ai/)

## 16.4.音樂生成應用實例
- 音樂生成應用實例 ─ MusicGen 字生樂
- 音樂生成應用實例 ─ MusicGen 互動介面

- 更多 Intel OpenVINO AIGC 範例


## 參考文獻

[1] 許哲豪，NTUST Edge AI 人工智慧與邊緣運算實務
https://omnixri.blogspot.com/p/ntust-edge-ai.html

[2] 許哲豪， 【課程簡報】20231209_DevFest Taichung_如何結合Google Colab及Intel OpenVINO來玩轉AIGC  
https://omnixri.blogspot.com/2023/12/20231209devfest-taichunggoogle.html  

## 延伸閱讀

[A] Intel OpenVINO DevCon （Youtube 中文講座）  
https://www.youtube.com/watch?v=jnYNJVvghgE&list=PLJhgRo1wc4K9LRAUUgG-48BxJVqXEXhhH  

[B] Intel OpenVINO™ 生成式 AI 系列 (Bilibili 教學影片)  
https://space.bilibili.com/38566875/channel/collectiondetail?sid=2301246  

## 教學資源

OmniXRI 系列文章：  
https://omnixri.blogspot.com/p/blog-page_19.html

OmniXRI Youtube 教學影片頻道：  
https://www.youtube.com/@omnixri1784/videos  

OmniXRI Github 課程簡報及相關範例：  
https://github.com/OmniXRI/Edge_AI_TinyML_Course_2024

---
註：本課程非學校正式課程，現僅有老師一人，沒有教學助理可幫忙，如操作上有相關問題，請於Youtube, FB Group, Blogger, Medium, Hackmd, Github 各討論區中留言，老師會儘量協助，如有服務不週之處尚請見諒。
