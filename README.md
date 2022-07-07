# EraseNet

This repository is the implementation of EraseNet, a neural network for end-to-end scene text removal.


## Data preparation

The data preparation can be refer to ./examples/. You can download our datatset at [SCUT-EnsText](https://github.com/HCIILAB/SCUT-EnsText) or synthetic dataset [SCUT-Syn](https://github.com/HCIILAB/Scene-Text-Removal) for training and testing. 

SCUT-EnsText needs decompression password, you can send me at [liuchongyu1996@gmail.com](mailto:liuchongyu1996@gmail.com) for it.

## Environment

Anaconda is recommended to establish a virtual environment to run our code. My environment can be refered as follows:
```
python = 3.7
pytorch = 1.3.1
torchvision = 0.4.2
```

## Demo

We provide our retrain model for quick inference for SCUT-EnsText. [Model Link](https://drive.google.com/file/d/1scrtQ2GFvKjjoGEqbKxpOMn37mJmXsFd/view)

## Training

Once the data is well prepared, you can begin training:
```
python train_STE.py --batchSize 4 \
  --dataRoot 'your path' \
  --modelsSavePath 'your path' \
  --logPath 'your path'  \
```

## Testing and evaluation

If you want to predict the results, run:

```
python test_image_STE.py --dataRoot 'your path'  \
            --batchSize 1 \
            --pretrain 'your path' \
            --savePath 'your path'
```

To evaluate the results:
```
python evaluatuion.py --target_path 'results_path' --gt_path 'labels_path'
```



## Acknowledge

The repository is benefit a lot from [LBAM](https://github.com/Vious/LBAM_Pytorch) and [GatedConv](https://github.com/avalonstrel/GatedConvolution_pytorch). Thanks a lot for their excellent work.

## Citation
If you find our method or dataset useful for your reserach, please cite:
```
@ARTICLE{Erase2020Liu,
  author     ={Liu, Chongyu and Liu, Yuliang and Jin, lianwen and Zhang, Shuaitao and Luo, Canjie and Wang, Yongpan},
  journal    ={IEEE Transactions on Image Processing},
  title      ={EraseNet: End-to-End Text Removal in the Wild},
  year       ={2020},
  volume     ={29},
  pages      ={8760-8775},}

@article{zhang2019EnsNet,
    title     = {EnsNet: Ensconce Text in the Wild},
    author    = {Shuaitao Zhang∗, Yuliang Liu∗, Lianwen Jin†, Yaoxiong Huang, Songxuan Lai
    joural    = {AAAI}
    year      = {2019}
  }
```

## Feedback
Suggestions and opinions of our work (both positive and negative) are greatly welcome. Please contact the authors by sending email to Chongyu Liu([liuchongyu1996@gmail.com](mailto:liuchongyu1996@gmail.com)). For commercial usage, please contact Prof. Lianwen Jin via ([eelwjin@scut.edu.cn](mailto:eelwjin@scut.edu.cn)).
