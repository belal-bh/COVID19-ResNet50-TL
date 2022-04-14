# Colaboratory Notebooks

We conduct our research experiment on the [Google Colaboratory](https://colab.research.google.com/) runtime environment. We utilize the free GPU runtime of google colaboratory. Because of the daily free GPU limit, we conduct our experiments in different colaboratory notebooks. We create ten different notebooks for ten different Transfer Learning (TL) models. Most of the code same except for the checkpoint sections of the corresponding TL model.

In this section, we shortly described the different TL models and the corresponding colaboratory notebooks. For details information please see our research paper [Transfer learning with fine-tuned deep CNN ResNet50 model for classifying COVID-19 from chest X-ray images](https://www.sciencedirect.com/science/article/pii/S235291482200065X).

**Note:** All these pre-trained ResNet50 model weights are used to initialize our ResNet50 TL models. After initializing these pre-trained weights, we trained our models on the COVID-19 Radiography dataset.

## ChestX-ray14

This pre-trained weight is an in-domain ResNet50 model trained on the ChestX-ray14 dataset consisting of 112K frontal-view chest X-ray images of 30K unique patients.

Notebook: [covid19v2-ResNet50-(ChestX-ray14)-TL-binary.ipynb](<./covid19v2-ResNet50-(ChestX-ray14)-TL-binary.ipynb>)

## ChexPert

This pre-trained weight is an in-domain ResNet50 model trained on a large-scale publicly available ChexPert dataset consisting of 224K chest X-ray images of 65K patients.

Notebook: [covid19v2-ResNet50-(ChexPert)-TL-binary.ipynb](<./covid19v2-ResNet50-(ChexPert)-TL-binary.ipynb>) and [covid19v2-ResNet50-(ChexPert (from-40ep))-TL-binary.ipynb](<./covid19v2-ResNet50-(ChexPert%20(from-40ep))-TL-binary.ipynb>)

## ImageNet

This pre-trained weight is the ResNet50 model trained on a well-known ImageNet dataset. These pre-trained weights are loaded from the PyTorch framework’s pre-trained models collection.

Notebook: [covid19v2-ResNet50-(imagenet)-TL-binary.ipynb](<./covid19v2-ResNet50-(imagenet)-TL-binary.ipynb>)

## ImageNet_ChestX-ray14

A domain-adapted pre-trained ResNet50 model’s weight. This model was trained on two different datasets. Firstly, the model was initialized with pre-trained ImageNet weight and then again trained on the ChestX-ray14 dataset.

Notebook: [covid19v2-ResNet50-(ImageNet_ChestX-ray14)-TL-binary.ipynb](<./covid19v2-ResNet50-(ImageNet_ChestX-ray14)-TL-binary.ipynb>)

## ImageNet_ChexPert

This is also a domain-adapted pre-trained ResNet50 model’s weight trained on two different datasets. The model was initialized with pre-trained ImageNet weight and then again trained on the ChexPert dataset.

Notebook: [covid19v2-ResNet50-(ImageNet_ChexPert)-TL-binary.ipynb](<./covid19v2-ResNet50-(ImageNet_ChexPert)-TL-binary.ipynb>)

## iNat2021_Supervised

The iNat2021 is a large-scale natural world dataset consisting of 2.7M images of 10K different species. This pre-trained supervised ResNet50 model’s weight was collected. This pre-trained weight was downloaded manually from the given source on that paper and the wight file name was `inat2021_supervised_large.pth.tar`. The model was initialized with pre-trained ImageNet weight and then trained on the iNat2021 dataset.

Notebook: [covid19v2-ResNet50-(inat2021_supervised_large)-TL-binary.ipynb](<./covid19v2-ResNet50-(inat2021_supervised_large)-TL-binary.ipynb>)

## iNat2021_Supervised_From_Scratch

This pre-trained supervised ResNet50 model’s weight was also collected from the same source as _iNat2021_Supervised_. But this model only trained on the iNat2021 dataset instead of initializing with pre-trained ImageNet weight. `inat2021_supervised_large_from_scratch.pth.tar` was the name of the pre-trained weight file.

Notebook: [covid19v2-ResNet50-(inat2021_supervised_large_from_scratch)-TL-binary.ipynb](<./covid19v2-ResNet50-(inat2021_supervised_large_from_scratch)-TL-binary.ipynb>)

## iNat2021_Mini_SwAV_1k

The iNat2021 Mini is a smaller (500K images) version of the iNat2021 dataset that contains 50 training images per species. This pre-trained ResNet50 model utilized a self-supervised SwAV algorithm while training on the iNat2021 Mini dataset. The pre-trained weight is collected from the same source paper as _iNat2021_Supervised_ and _iNat2021_Supervised_From_Scratch_. The file name of the pre-trained weight was `inat2021_swav_mini_1000_ep.pth`.

Notebook: [covid19v2-ResNet50-(inat2021_swav_mini_1000_ep)-TL-binary.ipynb](<./covid19v2-ResNet50-(inat2021_swav_mini_1000_ep)-TL-binary.ipynb>)

## MoCo_v1

One of the self-supervised learning (SSL) methods is MoCo (Momentum Contrast) v1. This is a contrastive learning method. The pre-trained ResNet50 model’s weight which is trained on the ImageNet dataset utilizing MoCo v1 was collected. This weight was trained over 200 epochs.

Notebook: [covid19v2-ResNet50-(moco-v1)-TL-binary.ipynb](<./covid19v2-ResNet50-(moco-v1)-TL-binary.ipynb>)

## MoCo_v2

The SSL method `MoCo_v2` is the improved version of `MoCo_v1`. The pre-trained ResNet50 TL model’s weight which is trained on the ImageNet dataset utilizing `MoCo_v2`. This weight was trained over 800 epochs.

Notebook: [covid19v2-ResNet50-(moco-v2)-TL-binary.ipynb](<./covid19v2-ResNet50-(moco-v2)-TL-binary.ipynb>)

## Other notebooks

Tere is a separate colaboratory notbook, [covid19v2-ResNet50-Evaluation(available_best_validation_checkpoints)-TL-binary.ipynb](<./covid19v2-ResNet50-Evaluation(available_best_validation_checkpoints)-TL-binary.ipynb>) which is basically run evaluation program on the saved model checkpoints. Also generate some evaluation summary about 10 different models.

## Important Consideration

These colaboratory notebooks have some dependency and special environment requiremnets. So, be carefull if you want to run these notebooks, it may not work properly. I used google drive to store some files and secret information like kaggle API credential. If you understand the code you can set these environment properly with right credentials and run on google colaboratory GPU runtime. Also you can ping me if you need more information.

Extra dependencies:

- Google acount
- Google Drive account access
- Kaggle API credentials for dounloading Dataset
- Manually configure Google Drive paths that required in the program
- Google colaboratory GPU runtime environment

## Welcome

If this reserch experiments help in any of your research please cite this paper.

Thank you.

**Cite**:

```BibTex
@article{HOSSAIN2022100916,
title = {Transfer learning with fine-tuned deep CNN ResNet50 model for classifying COVID-19 from chest X-ray images},
journal = {Informatics in Medicine Unlocked},
volume = {30},
pages = {100916},
year = {2022},
issn = {2352-9148},
doi = {https://doi.org/10.1016/j.imu.2022.100916},
url = {https://www.sciencedirect.com/science/article/pii/S235291482200065X},
author = {Md. Belal Hossain and S.M. Hasan Sazzad Iqbal and Md. Monirul Islam and Md. Nasim Akhtar and Iqbal H. Sarker},
keywords = {Deep learning, Transfer learning, ResNet50, COVID-19}
}
```
