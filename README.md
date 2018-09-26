# Deep Laser Speckle Reduction (DeepLSR)

If you use this code, please cite:

Taylor L. Bobrow, Faisal Mahmood, Miguel Inserni, Nicholas J. Durr, “DeepLSR: Deep learning approach for laser speckle reduction"

<img src="https://github.com/faisalml/DeepLSR/blob/master/imgs/1.gif" width="256"/>    <img src="https://github.com/faisalml/DeepLSR/blob/master/imgs/2.gif" width="256"/>   <img src="https://github.com/faisalml/DeepLSR/blob/master/imgs/3.gif" width="256"/>


## Setup

### Prerequisites

- Linux (Tested on Ubuntu 16.04)
- NVIDIA GPU (Tested on Nvidia P100 using Google Cloud)
- CUDA CuDNN (CPU mode and CUDA without CuDNN may work with minimal modification, but untested)
- Pytorch>=0.4.0
- torchvision>=0.2.1
- dominate>=2.3.1
- visdom>=0.1.8.3
- scipy

### Dataset

All image pairs must be 256x256 and paired together in 512x256 images. '.png' and '.jpg' files are acceptable. Data needs to be arranged in the following order:

```bash
SOMEPATH # Some arbitrary path
└── Datasets # Datasets folder
      └── XYZ_Dataset # Active dataset
            ├── test
            └── train
```

### Training

To train a model:
```
python train.py --dataroot <datapath> --name DeepLSR  --gpu_ids 0 --display_id 0 
--lambda_L1 70 --niter 200 --niter_decay 200 --pool_size 64 --loadSize 256 --fineSize 256
```
- To view training losses and results, run `python -m visdom.server` and click the URL http://localhost:8097. For cloud servers replace localhost with your IP. 
- To view epoch-wise intermediate training results, `./checkpoints/DeepLSR/web/index.html`
- `--niter` number of epochs with constant learning rate `--niter_decay` number of epochs with learly decaying learning rate
- `--lr` adjusts the learning rate, default = 0.002
### Testing

To test the model:
```
python test.py --dataroot <datapath> --name DeepLSR --gpu_ids 0 --display_id 0 
--loadSize 256 --fineSize 256
```
- The test results will be saved to a html file here: `./results/facades_pix2pix/test_latest/index.html`.

### Issues

- Please open new threads or report issues to faisalm@jhu.edu
- Immidiate response to minor issues may not be available.

## License
© [Durr Lab](https://durr.jhu.edu) - This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
- This code is inspired by [pytorch-DCGAN](https://github.com/pytorch/examples/tree/master/dcgan), [pytorch-CycleGAN-and-pix2pix](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) and [SNGAN-Projection](https://github.com/pfnet-research/sngan_projection)
* Subsidized computing resources were provided by Google Cloud.

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
