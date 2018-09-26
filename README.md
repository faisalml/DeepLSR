# Deep Laser Speckle Reduction (DeepLSR)

If you use this code, please cite:

Taylor L. Bobrow, Faisal Mahmood, Niguel Inserni, Nicholas J. Durr, “DeepLSR: Deep learning approach for laser specklereduction

## Setup

### Prerequisites

- Linux (Tested on Ubuntu 16.04)
- NVIDIA GPU (Tested on Nvidia P100 using Google Cloud)
- CUDA CuDNN (CPU mode and CUDA without CuDNN may work with minimal modification, but untested)
- Pytorch>=0.4.0
- torchvision>=0.2.1
- dominate>=2.3.1
- visdom>=0.1.8.3

### Dataset

All image pairs must be 256x256 and paired together in 512x256 images. '.png' and '.jpg' files are acceptable. Data needs to be arranged in the following order:

```bash
SOMEPATH # Some arbitrary path
└── Datasets # The unzip folder of SUNRGBD.zip
      └── XYZ_Dataset # The unzip folder of SUNRGBDtoolbox.zip
            ├── test
            └── train
```

### Training

### Test

### Issues

Please open new threads or report issues to faisalm@jhu.edu

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Google Cloud for subsidized computing resources.


## Reference
If you find our work useful in your research please consider citing our paper:
```
@inproceedings{bobrow2018deeplsr,
  title     = {DeepLSR: Deep learning approach for laser speckle reduction},
  author    = {Taylor L. Bobrow, Faisal Mahmood, Niguel Inserni, Nicholas J. Durr},
  booktitle = {arXiv},
  year = {2018}
}
```
