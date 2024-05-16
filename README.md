# PartFormer-Partial-Transformer-for-Lightweight-Image-Restoration

## Installation
This implementation based on BasicSR which is a open source toolbox for image/video restoration tasks.

```
python 3.9.5
pytorch 1.11.0
cuda 11.3
```

```
cd Image Restoration
pip install -r requirements.txt
python setup.py develop --no_cuda_ext
```
## Quick Start
Image Super-Resolution
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/PartFomrer/test_partformer_x2.yml --launcher pytorch 
```
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/PartFomrer/test_partformer_x3.yml --launcher pytorch 
```
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/PartFomrer/test_partformer_x4.yml --launcher pytorch 
```
Image Denoising
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/Gauss_noisy/PartFormer15_color.yml --launcher pytorch 
```
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/Gauss_noisy/PartFormer25_color.yml --launcher pytorch 
```
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/Gauss_noisy/PartFormer50_color.yml --launcher pytorch 
```
Image Deraining
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/Rain/PartFormer-Rain.yml --launcher pytorch 
```
Low-light enhancement
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/LOL/Partformer-LOL.yml --launcher pytorch 
```
```
PYTHONPATH="./:${PYTHONPATH}" CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node=1 --use_env  --master_port=4321 basicsr/test.py -opt options/test/LOL/Partformer-LOLv2.yml --launcher pytorch 
```
## Pre-trained Models
Pre-trained models can be found in [the relased file](https://github.com/charonf/PartFormer-Partial-Transformer-for-Lightweight-Image-Restoration/releases/tag/pre-trained_model).
