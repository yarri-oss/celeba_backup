# TFDS Manual Loading of Celeb A Dataset

Workaround for failing TFDS library for loading the public dataset, Celeb A.
As of Dec-3 2021, the [TFDS Celeb A](https://www.tensorflow.org/datasets/catalog/celeb_a) dataset gives an `wrong checksum` error
when trying to use `tfds.load("celeb_a")` and this library is a workaround
using a mirror of the `img_align_celeba` dataset on S3.

## Usage

You can use this from within Colab using the following methods:

```
!pip install git+https://github.com/yarri-oss/celeba_backup.git
!pip install tfds_nightly

import tensorflow as tf
tf.__version__    # should be 2.7.0

import tensorflow_datasets as tfds
import celeba_backup
ds = tfds.load('celeba_backup', split='train')
```

