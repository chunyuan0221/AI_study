### Ultrasound Nerve Segmentation
***
- Porpose:This project want to build a model that can identify nerve structures in a dataset of ultrasound images of the neck. 
- Project process: There are Three files for all process.
  1. Data preprocessing: 
      - We do Data Preprocessing locally because it only takes less time.
      - Save the processed data as a .npy file and upload it to Google Drive.
  2. Creat U-Net Model: 
      - In this project, we use the U-Net architecture to build the model, as shown in the following figure:
        ![alt text](https://drive.google.com/uc?id=1JU4y_mMTNPkax0HhSEhUuzpcGuZQ2jj7)
      - Framework: Keras
      - The Optimizer is **Adam(lr=1e-5)**
      - The loss function is **dice_coef_loss**
      - The metrics is **dice_coef**
  3. Training and Predict
      - Load training and test data(.npy) that we preprocessing.
      - Fit Model and predict testing data.
      - Save the prediction results of each test data as a image file.
  4. Submit the result to Kaggle
      - Save the test data results to the file format requested by Kaggle.

- Result:
  1. On training set: **loss: -0.5608 - dice_coef: 0.5608**
  2. On validation set: **val_loss: -0.3869 - val_dice_coef: 0.3869**
  3. The score on Kaggle:
    ![alt text](https://drive.google.com/uc?id=1nM8_n1NaTY6nfe_gUtzKuNKxH9eJy303)
    
### Referance
1. [Kaggle complete: Ultrasound Nerve Segmentation](https://www.kaggle.com/c/ultrasound-nerve-segmentation/overview)
2. [jocicmarko github](https://github.com/jocicmarko/ultrasound-nerve-segmentation)
