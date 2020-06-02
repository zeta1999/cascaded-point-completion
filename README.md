## Cascaded Refinement Network for Point Cloud Completion

This is the TensorFlow implementation for the paper "Cascaded Refinement Network for Point Cloud Completion"

## Getting Started
python version: python-3.5;  cuda version: cuda-10;  TensorFlow version: tensorflow-1.13

## Datasets
[Our dataset](https://drive.google.com/file/d/1MzVZLhXOgfaLZjn1jDrwuiCB-XCfaB-w/view?usp=sharing)

PCN's dataset: Please download it from [PCN](https://github.com/wentaoyuan/pcn)
    
## Train the model
To train the models: python train.py  
    --loss_type: CD_T or CD_P;  
    --h5_train: the training data;  
    --h5_val: the validation data;  
    --num_gt_points: the resolution of ground truth point clouds;  
    --step_ratio: 2, 4, 8, 16 for different output resolutions;   
    --log_dir: output directory to save models and training log;   
    --augment: whether to use data augmentation during training.
    

## Evaluate the models
Our pre-trained models can be downloaded here: [Models](https://drive.google.com/file/d/1egNorG-u98SWUueBsZquw02l4cHU8xBD/view?usp=sharing), unzip and put them in the root directory.  
To evaluate models in different cases: python test.py  
    --loss_type: CD_T or CD_P;  
    --data_dir: the test data from different cases;   
    --checkpoint: the pre-trained models;   
    --num_gt_points: the resolution of ground truth point clouds;    
    --step_ratio: 2, 4, 8, 16 for different output resolutions.
    
## Citation
@inproceedings{wang2020cascaded,  
&nbsp;&nbsp;&nbsp;&nbsp;      author    = {Wang, Xiaogang and Ang Jr, Marcelo H and Lee, Gim Hee},  
&nbsp;&nbsp;&nbsp;&nbsp;      title     = {Cascaded Refinement Network for Point Cloud Completion},  
&nbsp;&nbsp;&nbsp;&nbsp;      booktitle = {Conference on Computer Vision and Pattern Recognition (CVPR)},  
&nbsp;&nbsp;&nbsp;&nbsp;      year      = {2020},  
}

## Acknowledgements 
Our implementations use the code from the following repository:  
[PCN](https://github.com/wentaoyuan/pcn)    
[PointNet++](https://github.com/charlesq34/pointnet2)
