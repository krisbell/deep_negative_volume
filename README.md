# Deep Negative Volume Segmentation

<p align="center">
<img src="./img/pipeline.png" alt>

</p>
<p align="center">
<em>Sample caption</em>
</p>

## Requirements

To install requirements:

```setup
pip install -r requirements.txt
```
## Training

To train the models used in the paper, run this command:

```train
python train.py --config <path_to_config_file>
```

## Evaluation

To evaluate models, run:

```eval
python train.py --config <path_to_config_file>
```

## Pre-trained Models

You can download pretrained models here:

- 3D U-Net and V-Net trained on spherical negative volumes https://drive.google.com/mymodel.pth 
- 3D U-Net,3D U-Net with attention gates, and V-Net trained with different loss function on mandibular condyle https://drive.google.com/mymodel.pth 
- 3D U-Net,3D U-Net with attention gates, and V-Net trained with different loss function on temporal bone https://drive.google.com/mymodel.pth 

## Results


