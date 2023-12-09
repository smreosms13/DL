# Learning with Coarse Labels using Grafit and MaskCon

This repository implements Grafit and MaskCon, two techniques for learning with coarse labels in computer vision tasks. The code is modified based on the [MaskCon_CVPR2023 repository](https://github.com/MrChenFeng/MaskCon_CVPR2023).

## Related Papers

- **Grafit: Learning fine-grained image representations with coarse labels**
  - Hugo Touvron, Alexandre Sablayrolles, Matthijs Douze, Matthieu Cord, Hervé Jégou
  - [arXiv:2011.12982](https://arxiv.org/abs/2011.12982)

- **MaskCon: Masked Contrastive Learning for Coarse-Labelled Dataset**
  - Chen Feng, Ioannis Patras
  - [arXiv:2303.12756](https://arxiv.org/abs/2303.12756)

### Bibtex

```bibtex
@misc{touvron2020grafit,
  title={Grafit: Learning fine-grained image representations with coarse labels},
  author={Hugo Touvron and Alexandre Sablayrolles and Matthijs Douze and Matthieu Cord and Hervé Jégou},
  year={2020},
  eprint={2011.12982},
  archivePrefix={arXiv},
  primaryClass={cs.CV}
}

@misc{feng2023maskcon,
  title={MaskCon: Masked Contrastive Learning for Coarse-Labelled Dataset},
  author={Chen Feng and Ioannis Patras},
  year={2023},
  eprint={2303.12756},
  archivePrefix={arXiv},
  primaryClass={cs.CV}
}

```
## Original GitHub Repository
[MaskCon_CVPR2023](https://github.com/MrChenFeng/MaskCon_CVPR2023).

### Updates and Modifications

#### 1. Code Modifications

The code has been modified in the following ways:

- **utils.py Modification & ops.py Creation:** The `utils.py` file has been modified, and a new file `ops.py` has been created. These changes are based on updates from the [AutoAugment PyTorch repository](https://github.com/DeepVoltaire/AutoAugment).

#### 2. Target Data and Label Type Correction

Due to errors, changes have been made to the target data and target label types.

#### 3. Typo Correction in utils.py

A typo in `utils.py` has been corrected.

## Preparation
- Python: 3.11.5
- Anaconda: 23.10.0
- PyTorch: 2.0.1
- CUDA: 11.7.0
- torchvision: 0.15.2
- wandb: 0.15.12

## Usage
Example runs on CIFAR100/CIFARToy dataset:

- MaskCon & CIFAR100:
  ```bash
  python main.py --dataset cifar100 --wandb_id [wandb_id] --w 1.0 --t 0.05
  ```
- Grafit & CIFARToy :
- ```bash
  python main.py --dataset cifartoy_good --mode grafit --wandb_id [wandb_id] --w 0.8 --t0 0.1
  ```
