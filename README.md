# TFDS Manual Loading of Celeb A Dataset

Workaround for failing TFDS library for loading the public dataset, Celeb A

## Usage

You can use this from within Colab using the following methods:

```
!pip install git+https...
!pip install tfds_nightly

import tensorflow as tf
tf.__version__    # should be 2.7.0

import tensorflow_datasets as tfds
import celeba_backup
ds = tfds.load('celeba_backup')
```

