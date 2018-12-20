# DLHSD

## Dataset

Feature Tensor Extraction Data is already within this repo, original images can be found at http://appsrv.cse.cuhk.edu.hk/~hyyang/files/iccad-official.tgz

## Dependencies

numpy, tensorflow (tested on 1.3 and 1.9), pandas, json, ConfigParser, progress

## Feature Tensor Extraction

```python feature.py str<image_folder> str<output_feature_folder> int<block_size> int<block_dim> int<feature_length>```

## Test

e.g. to test iccad1 of dac17, you need to modify iccad1\_config.ini

set ```model_path=./models/iccad1/bl/model.ckpt```

set ```aug=0``` and

 ```make iccad1_test``` in ```dlhsd``` directory

## Train

e.g. to train iccad1 of dac17, you need to modify iccad1\_config.ini

set ```save_path=./models/iccad1/bl/model.ckpt```

set ```aug=0``` and 

```python train_dac.py iccad1_config.ini <gpu_id>```

use ```train.py``` if you want to see some results of the TCAD extension

## Updates

-20181220: Add script for feature tensor extraction.

-20180827: Add the link of original images of layouts from the  ICCAD benchmark (resolution: 1nm).

-20180705: Fix a bug that learning rate does not decay properly which might cause unstable results.