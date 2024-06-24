Implementation of Diffusetrace
===

1.Pretraining
---
	python train_pretrain.py --secret_length 48 --steps 10000000 --kl_weight 1 --rec_weight 1 --lr 0.0005 --batchsize 64 --load_path '' --save_path './model48bit.pth'

2.Finetuning
---
	python finetune.py --w_seed 0 --dataset Gustavosta/Stable-Diffusion-Prompts --model_path ../stable-diffusion-2-1-base --secret_length 48 --num_inference_steps 25 --guidancescale 5 --reverse_inference_steps 25 --batchsize 8 --lr 0.0005 --steps 500

