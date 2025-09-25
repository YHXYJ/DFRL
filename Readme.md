## DFRL for Single-Domain Generalization in Infrared Small Target Detection 

This repository contains the test scripts. By running these scripts, you can reproduce the results presented in our paper. The complete training code and model implementation will be made publicly  available upon the completion of the review process.

## Code Structure

code/   
 ├── dataset/                          #This directory contains the datasets for test.   
 ├── model/                            #This directory contains the models of IRSTD.  
 ├── pth/                                 # This directory contains the pretrained weights and corresponding test results.   
 ├── test_xxxx.py                  # testing scripts.         



## Environment

- Python 3.9
- PyTorch 2.6.0
- CUDA 11.8

```bash
conda create -n DFRL python=3.9
conda activate DFRL
```



---

### Dataset Preparation

The IRSTD-1k dataset can be downloaded form https://github.com/RuiZhang97/ISNet/tree/master.

The NUAA-SIRST dataset can be downloaded form https://github.com/YimianDai/sirst.

Datasets should be put as the follow：

dataset/        
 ├── IRSTD-1k/                   

 │   ├── 80_20/                  #Train/val split indices.       
 │   ├── images/                        
 │   ├── masks /      	                    

​	...

## testing

Before running `test_xxxx.py`, please modify the following configurations in `test_xxxx.py`:

- `model_dir`: Modify **line  30**. #path to the trained weights. 

The output will be saved in the same directory as the pth file.