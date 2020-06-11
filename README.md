# Deep Negative Volume Segmentation

> 📋Optional: include a graphic explaining your approach/main result, bibtex entry, link to demos, blog posts and tutorials

## Requirements

To install requirements:

```setup
pip install -r requirements.txt
```
## Training

To train the models used in the paper, run this command:

```train
python train.py --input-data <path_to_data> --alpha 10 --beta 20
```

## Evaluation

To evaluate models, run:

```eval
python eval.py --model-file mymodel.pth 
```


## Pre-trained Models

You can download pretrained models here:

- 3D U-Net and V-Net trained on spherical negative volumes https://drive.google.com/mymodel.pth 
- 3D U-Net,3D U-Net with attention gates, and V-Net trained with different loss function on mandibular condyle https://drive.google.com/mymodel.pth 
- 3D U-Net,3D U-Net with attention gates, and V-Net trained with different loss function on temporal bone https://drive.google.com/mymodel.pth 

## Results

Our model achieves the following performance on :

### [Image Classification on ImageNet](https://paperswithcode.com/sota/image-classification-on-imagenet)

| Model name         | Top 1 Accuracy  | Top 5 Accuracy |
| ------------------ |---------------- | -------------- |
| My awesome model   |     85%         |      95%       |

\begin{table}[]
    \centering
    \caption{Mandibular condyle (MC), temporal bone (TB) and negative volume (NV) segmentation results. Notice that the whole-object 3D segmentation of the manually annotated ``balls'' from Fig.1 need more data to work properly, justifying the development of our automated pipeline which just needs MC and TB masks.}
    \small
    \begin{tabular}{ccccccc} \toprule
    % \multicolumn{2}{c}{Item} \\ \cmidrule(r){1-2}
    Obj. & Score & 3D U-Net & 3D U-Net+Att.  &  V-Net CE & V-Net D & V-Net D+CE \\ \midrule
    \multirow{3}{*}{MC}
    %   \multirow{3}{*}{MC}
     & DICE & $91.4 \pm 5.3$ & $89.8 \pm 8.2$ 
     & $90.9 \pm 4.5$ & $90.9 \pm 6.3$  & $\mathbf{91.4} \pm 4.8$ \\ % VNet 
     & CE & $0.320 \pm 0.003$ & $0.320 \pm 0.005$ 
     & $0.201 \pm 0.075$ & $0.175 \pm 0.024$ & $\mathbf{0.154} \pm 0.053$ \\ % VNet  
     & HD & $14.7 \pm 20.8$ & $15.2 \pm 21.6$ 
     & $11.9 \pm 15.7$ & $11.5 \pm 20.1$  & $\mathbf{10.5} \pm 21.2$  \\ \cline{1-7} % VNet 
       
    \multirow{3}{*}{TB}
     & DICE & $75.5 \pm 8.8$ & $75.8 \pm 8.4$ 
     & $75.9 \pm 6.9$ & $\mathbf{76.7} \pm 6.8$  & $76.3 \pm 7.2$ \\ % VNet 
     & CE & $0.463 \pm 0.043$ & $0.462 \pm 0.035$ 
     & $\mathbf{0.383} \pm 0.088$ & $0.396 \pm 0.093$ & $0.416 \pm 0.100$ \\ % VNet  
     & HD & $29.8 \pm 11.5$ & $29.9 \pm 11.3$
     & $27.9 \pm 11.5$ & $ 28.3 \pm 10.7$ & $ \mathbf{27.6} \pm 10.9$ \\ \cline{1-7} % VNet 
     
    \multirow{3}{*}{NV}
     & DICE & $78.0 \pm 10.6$ & - & - & - & $77.7 \pm 7.7$\\ %\cline{2-7} 
     & CE & $0.344 \pm 0.016$ & - & - & - & $0.406 \pm 0.022$ \\ %\cline{2-7} 
     & HD & $15.8 \pm 18.8$ & - & - & - & $18.7 \pm 17.8$ \\ \bottomrule
    \end{tabular}
     {\small \raggedright \textbf{Note:} Here \textit{CE}, \textit{D} are Cross-Entropy and Dice loss, respectively. \textit{DICE} (measured in $\%$) and \textit{HD} are Dice score and Hausdorff distance. \textit{Att.} stands for the attention-gate architecture.  \par}
    \label{tab:table_segmentation}
\end{table}

> 📋Include a table of results from your paper, and link back to the leaderboard for clarity and context. If your main result is a figure, include that figure and link to the command or notebook to reproduce it. 


## Contributing

> 📋Pick a licence and describe how to contribute to your code repository. 
