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

## Dataset

All image pairs must be 256x256 and paired together in 512x256 images. '.png' and '.jpg' files are acceptable. Data needs to be arranged in the following order:

```bash
SOMEPATH # Some arbitrary path
├── SUNRGBD # The unzip folder of SUNRGBD.zip
└── SUNRGBDtoolbox # The unzip folder of SUNRGBDtoolbox.zip
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc


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
