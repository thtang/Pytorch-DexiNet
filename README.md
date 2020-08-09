# DexiNed-PyTorch


This repo is an official unofficial version of DexiNed in Pytorch. The first official version of [DexiNed is in Tensorflow](https://github.com/xavysp/DexiNed).

## Requerements

* Python 3.7
* Pytorch   1.0.1
* OpenCV
* Torchgeometry
## Training Settings
To train DexiNed in Pytorch is similar to training in Tensorflow. For more details see [DexiNed](https://github.com/xavysp/DexiNed/blob/master/README.md).

To summarize: firstly you should download and unzip the BIPED dataset hosted in [Kaggle](https://www.kaggle.com/xavysp/biped). Secondly, augment the dataset with [this ripo](https://github.com/xavysp/MBIPED). Once the BIPED is augmented set the base dir and set the model for training in main.py:

```
python main.py
```
Then, just train.

## Testing Settings
In dexi_utils.py we have added the popular datasets used in edge, contour, and boundary detection. So you should choose the dataset in main():
```
DATASET_NAME= ['BIPED','BSDS','BSDS300','CID','DCD','MULTICUE',
                    'PASCAL','NYUD','CLASSIC'] # 8
TEST_DATA = DATASET_NAME[0]
```
And set for testing the following lines:
```
python main.py --is_testing=True --use_prev_trained True --checkpoint_data 24/24_model.pth
```
Colab [[link]](https://colab.research.google.com/drive/1zeOKkz3f-0vp-WuY-nGgaK50pPegFXpy?usp=sharing)
```
- The whole of input image are sized with the same image width and height if you could help us setting with individual image size we will thank you :)

```

### Dataset

After setting up you just need to run and that's it


### Single Image
 Before testing in the single image please make sure that the images used for testing in [data directory](https://github.com/xavysp/DexiNed-Pytorch/tree/master/data) have the same size. Otherwise, the data will be resized with the default values in dexi_utils.py.  
 
 # Citation
Please cite the paper if you find helpful,
```
@InProceedings{soria2020dexined,
    title={Dense Extreme Inception Network: Towards a Robust CNN Model for Edge Detection},
    author={Xavier Soria and Edgar Riba and Angel Sappa},
    booktitle={The IEEE Winter Conference on Applications of Computer Vision (WACV '20)},
    year={2020}
}
```
```diff
+ If you find some typos or you think we can improve the code, we will appreciate your contribution

```
