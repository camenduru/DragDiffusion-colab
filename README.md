🐣 Please follow me for new updates https://twitter.com/camenduru <br />
🔥 Please join our discord server https://discord.gg/k5BwmmvJJU <br />
🥳 Please join my patreon community https://patreon.com/camenduru <br />

## 🦒 Colab

# 🚦 WIP 🚦

| Colab | Info
| --- | --- |
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/camenduru/DragDiffusion-colab/blob/main/DragDiffusion_colab.ipynb) | DragDiffusion_colab (🦒 Colab Pro)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/camenduru/DragDiffusion-colab/blob/main/DragDiffusion_train_colab.ipynb) | DragDiffusion_train_colab (🦒 Colab Free)

## Tutorial
For training please edit `/content/DragDiffusion/lora/train_lora.sh` file
```py
export SAMPLE_DIR="lora/samples/momo"
export OUTPUT_DIR="lora/lora_ckpt/momo"

export MODEL_NAME="runwayml/stable-diffusion-v1-5"
export LORA_RANK=16

accelerate launch lora/train_dreambooth_lora.py \
  --pretrained_model_name_or_path=$MODEL_NAME  \
  --instance_data_dir=$SAMPLE_DIR \
  --output_dir=$OUTPUT_DIR \
  --instance_prompt="a photo of a momo" \
  --resolution=512 \
  --train_batch_size=1 \
  --gradient_accumulation_steps=1 \
  --checkpointing_steps=100 \
  --learning_rate=2e-4 \
  --lr_scheduler="constant" \
  --lr_warmup_steps=0 \
  --max_train_steps=200 \
  --lora_rank=$LORA_RANK \
  --seed="0"
```

## Main Repo
https://github.com/Yujun-Shi/DragDiffusion

## Page
https://yujun-shi.github.io/projects/dragdiffusion.html

## Paper
https://arxiv.org/abs/2306.14435

## Output
![Screenshot 2023-07-10 095249](https://github.com/camenduru/DragDiffusion-colab/assets/54370274/a4ca147a-3fe6-4eee-8192-05ed14890843)
