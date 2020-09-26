# Energy-based Out-of-distribution Detection (Energy OOD)

This repository is the official implementation of [Energy-based Out-of-distribution Detection]

## Pretrained Models

Please download the [pretrained models](https://github.com/hendrycks/outlier-exposure/tree/master/CIFAR/snapshots/baseline) and put them in folder

```
./CIFAR/snapshots/baseline/
```

## Testing and Fine-tuning

run energy score testing for cifar10 WRN
```test
bash run.sh energy 0
```

run energy score testing for cifar100 WRN
```test
bash run.sh energy 1
```

run energy score training and testing for cifar10 WRN
```train
bash run.sh energy_ft 0
```

run energy score training and testing for cifar100 WRN
```train
bash run.sh energy_ft 1
```

## Results

Our model achieves the following performance on :

### [Image Classification on ImageNet](https://paperswithcode.com/sota/image-classification-on-imagenet)

| Model name         |     FPR95       |
| ------------------ |---------------- |
| Softmax score |     51.04%      |
| Energy score  |     33.01%      |
| Softmax score with fine-tune |     8.53%       |
| Energy score with fine-tune|     3.32%       |



## Outlier Datasets

These experiments make use of numerous outlier datasets. Links for less common datasets are as follows, [80 Million Tiny Images](http://horatio.cs.nyu.edu/mit/tiny/data/tiny_images.bin), [Icons-50](https://github.com/hendrycks/robustness),
[Textures](https://www.robots.ox.ac.uk/~vgg/data/dtd/), [Chars74K](http://www.ee.surrey.ac.uk/CVSSP/demos/chars74k/EnglishImg.tgz), and [Places365](http://places2.csail.mit.edu/download.html), [LSUN-C](https://www.dropbox.com/s/fhtsw1m3qxlwj6h/LSUN.tar.gz), [LSUN-R](https://www.dropbox.com/s/moqh2wh8696c3yl/LSUN_resize.tar.gz), [iSUN](https://www.dropbox.com/s/ssz7qxfqae0cca5/iSUN.tar.gz).
