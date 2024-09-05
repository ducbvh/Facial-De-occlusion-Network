# Facial-De-occlusion-Network

Quickstart in Colab [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OrpR9FAfXnJij0ecQkgE6KGWf7kLt3p3?usp=sharing)

##Model Architect
* This approach is an end to end inpainting method that learns to fill in user-specific details.
* No required  3D face to  face reconstruction.
* Easy to train, customize, fine-tuning.
- Model Architecture
  ![image](https://github.com/user-attachments/assets/0b6488f4-a192-4672-9adf-794040f27ee7)
- Encoder and Decoder:
  ![image](https://github.com/user-attachments/assets/66b65b16-8802-4af6-a83f-d5a87a1bba4e)
- Attention Module:
  ![image](https://github.com/user-attachments/assets/cc294063-c891-4ed9-a214-f5c454dbf486)


## Datasets

Link Mask: [Link](https://github.com/cabani/MaskedFace-Net.git)

Link UnMask: [Link](https://github.com/NVlabs/ffhq-dataset.git)

## Structure of Reposity
* `notebook`: contains Jupyter notebook file to train, evaluate and inference the model
    *  `FaceDe_occlusion.ipynb`: Step2step train model Face De-occlusion
* `training_checkpoints`: path to save checkpoints from model
* `weights`: model weight trained with no attention, can use to fine-tuning
* `dataset`: contains dataset splitted into train and test.
   *  `train`: contain train set
       *  `target`: target image
       *  `input`: input image
   *  `test`: contain test set
       * `target`: target image
       *  `input`: input image
       
## Results
* Train Based model (W/O Attention Module) with 100 epoch:
   - The generated image fills the lips and nose quite harmoniously. However, the image quality is blurry, not clear.
![Picture1](https://user-images.githubusercontent.com/45920660/231653665-9d720e4b-edc0-4111-9627-1851c5a64d52.png)



* Train with Attention Mudule with 300 epoch:  
   - The generated image is clear and detailed, but there is a white part of the mouth that cannot be filled.
   ![Picture2](https://user-images.githubusercontent.com/45920660/231653744-c4c967eb-e235-4e1a-be22-dd7018bf8824.png)

* Load Weights of Base model without Attention to Model with Attention and Fine-tune with 150 epoch:  
   => Fixed problem with white part of the mouth.


   ![Picture3](https://user-images.githubusercontent.com/45920660/231653771-7fbf930f-7727-43ed-a4b5-db83b3fa2ff5.png)
