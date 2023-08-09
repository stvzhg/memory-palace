---
feed: show
title: What is Stable Diffusion
date: 08-08-2023
---

# What is [Stable Diffusion](https://en.wikipedia.org/wiki/Stable_Diffusion)

**Stable Diffusion** is a [deep learning](https://en.wikipedia.org/wiki/Deep_learning "Deep learning"), [text-to-image model](https://en.wikipedia.org/wiki/Text-to-image_model "Text-to-image model") released in 2022 based on diffusion techniques. It is primarily used to generate detailed images conditioned on text descriptions, though it can also be applied to other tasks such as [inpainting](https://en.wikipedia.org/wiki/Inpainting "Inpainting"), outpainting, and generating image-to-image translations guided by a [text prompt](https://en.wikipedia.org/wiki/Prompt_engineering "Prompt engineering").[[3]](https://en.wikipedia.org/wiki/Stable_Diffusion#cite_note-:0-3) It was developed by researchers from the CompVis Group at [Ludwig Maximilian University of Munich](https://en.wikipedia.org/wiki/Ludwig_Maximilian_University_of_Munich "Ludwig Maximilian University of Munich") and Runway with a compute donation by Stability AI and training data from non-profit organizations.

# Installation guide (with webui)

## Install dependencies

```
sudo apt-get update
sudo apt-get install wget git python3 python3-venv ffmpeg libsm6 libxext6
```

## Download and execute installation script

```
bash <(wget -qO- https://raw.githubusercontent.com/AUTOMATIC1111/stable-diffusion-webui/master/webui.sh)
```

### Reference

https://github.com/AUTOMATIC1111/stable-diffusion-webui

# Use [[LoRA]] model

### Install sd-webui-additional-networks support

1. Open "Extensions" tab.
2. Open "Install from URL" tab in the tab.
3. Enter [URL](https://github.com/kohya-ss/sd-webui-additional-networks) of this repo to "URL for extension's git repository".
4. Press "Install" button.
5. Restart Web UI.

### Use model

1. Place LoRA models inside `extensions/sd-webui-additional-networks/models/LoRA` folder
2. Open **"Additional Networks"** panel from the left bottom of Web UI.
3. Press **"Refresh models"** to update the models list.
4. Select **"LoRA"** for **"Network module 1"**.
5. Choose **the name of the LoRA model file** in **"Model 1"**.
6. Set **the weight** of the model (negative weight might be working but unexpected.)
7. Repeat them for the module/model/weight 2 to 5 if you have other models. Models are applied in the order of 1 to 5.
8. You can generate images with the model with these additional networks.

### Reference

https://github.com/kohya-ss/sd-webui-additional-networks

# Use pre-trained model

1. Place pre-trained checkpoint inside `models/Stable-diffusion` folder
2. Click refresh button on the top left of the page or restart webui to use the new model
3. (Optional) some model need [[VAE]] for better performance. Place them in `models/VAE` folder and enable it in setting

# Useful website

* https://civitai.com/