# MCCGAN
[MCCGAN: AN ALL-IN-ONE IMAGE RESTORATION UNDER ADVERSE  CONDITIONS USING MULTIDOMAIN CONTEXTUAL CONDITIONAL GAN] (https://www.worldscientific.com/doi/abs/10.1142/S0219467825500111)

## Prerequisites
- Linux or macOS
- Python 3
- CPU or NVIDIA GPU + CUDA CuDNN

## Getting Started
### Installation
- Clone this repo:
```bash
git clone https://github.com/mariasiddiqua/MCCGAN/
cd mccgan
```

- Install [PyTorch](http://pytorch.org) and other dependencies. For Conda users, you can create a new Conda environment by

```bash
conda env create -f environment.yml
```

and then activate the environment by

```bash
conda activate mccgan
```

- To log training progress and test images to W&B dashboard, set the `--use_wandb` flag with training script
- Train a model:

```bash
python train.py --dataroot ./datasets/yourdataset --name restore --direction AtoB  --use_wandb
```

To see more intermediate results, check out `./checkpoints/restore/web/index.html`.

- Test the model:

```bash
python test.py --dataroot ./datasets/yourdataset --name restore --direction AtoB
```

- The test results will be saved to a html file here: `./results/restore/test_latest/index.html`.


## Citation

If you use this code for your research, please cite our papers.

```
@article{doi:10.1142/S0219467825500111,
author = {Siddiqua, Maria and Akhter, Naeem and Zameer, Aneela and Khurshid, Javaid},
title = {MCCGAN: An All-In-One Image Restoration Under Adverse Conditions Using Multidomain Contextual Conditional GAN},
journal = {International Journal of Image and Graphics},
volume = {25},
number = {02},
pages = {2550011},
year = {2025},
doi = {10.1142/S0219467825500111}
