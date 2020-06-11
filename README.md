# Deep Negative Volume Segmentation

<p align="center">
<img src="./img/pipeline.PNG" alt>

</p>
<p >
<em>End-to-end pipeline for Deep Negative Volume Segmentation. As an example, we take the most complex object in a human body - temporomandibular joint (TMJ), consisting of the mandibular condyle (MC) and the temporal bone (TB).
Segmentation of MC and TB are shown as step A and step B, respectively. Step C and step D represent classical image
enhancement of TB and 3D reconstruction of both bones. The “inflation/clipping” block represented by step E.
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


