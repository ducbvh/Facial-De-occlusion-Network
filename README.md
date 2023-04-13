# Facial-De-occlusion-Network
This is an implementation of [Facial De-occlusion Network for Virtual Telepresence Systems](https://arxiv.org/abs/2210.12622)

Try on Colab[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OrpR9FAfXnJij0ecQkgE6KGWf7kLt3p3?usp=sharing)

## Datasets

Link Mask: [Link](https://github.com/cabani/MaskedFace-Net.git)

Link UnMask: [Link](https://github.com/NVlabs/ffhq-dataset.git)

## Structure of Reposity
* `notebook': contains Jupyter notebook file on how to train and evaluate the models
    *  `FaceDeocculusion.ipynb`: Step2step train model Face De-occulusion
* `training_checkpoints`: path to save checkpoints from model
* `weights`: model weight trained with no attention, can use to fine-tuning
* `dataset`: contains dataset splitted into train and test.
   *  `train`: contain train set
     * *  `target`: target image
     * *  `input`: input image
   *  `test`: contain test set
     * * `target`: target image
     * *  `input`: input image
