### Holistically-Nested Edge Detection
***
- Edge Detection method:
  1. Tradition: Canny edge detector
    - The upper and lower hysteresis thresholds must be set manually, and tuning this parameter requires experience.
    - After testing A image, we found that this set of Hysteresis thresholding values has good edge detection, but this set of thresholds may not always have good results when used on B image.
    - Canny edge detector needs several preprocessing steps to obtain the edge map(image features), such as taking gray -> blurring.
  2. New: Holistically-Nested Edge Detection (HED)
    - In this project we use end-to-end network to solve the defects of Canny edge detector.
    - Purpose: Show you how to use Holistically-Nested Edge Detection in your own projects.
    - Model Framework: Cafee
    - Result:  
        Left(Oringinal)、Center(Canny)、Right(HED)
      ![alt text](https://drive.google.com/uc?id=14fSmXGTpGStKYSyW_FkQsZBKJtdvGYqh)
      ![alt text](https://drive.google.com/uc?id=19QpxPtxY6S0JWx_oZCFgmYMCxlGTiylN)
      
- Essential knowledge(When I was working on HED project, I read the following topics):
  1. [Python, argparse, and command line arguments](https://www.pyimagesearch.com/2018/03/12/python-argparse-command-line-arguments/)
  2. [Deep learning: How OpenCV’s blobFromImage works](https://www.pyimagesearch.com/2017/11/06/deep-learning-opencvs-blobfromimage-works/):
      - Before use this function code, not only install opencv you also need to install: **pip install imutils**
      - Purpose: 
        1. Data pre-processing.
        2. Use cv2.dnn.blobFromImage() to convert the input image into the format required by Cafee framework.
           ![alt text](https://drive.google.com/uc?id=1G3IqZmpci63l76nRA7efRea2oqINWiYw)
      - Code: blob = cv2.dnn.blobFromImage(image, scalefactor=1.0, size, mean, swapRB=True)
        1. image: The image you want preprocessing.
        2. scalefactor: The scale of image enlarged or reduced.
        3. size: Size depends on the default input image size of the CNN Model, such as image Length, width and depth.
        4. mean: These are our mean subtraction values.
        5. swapRB: Set whether to exchange R and B channels.
      - mean subtraction values: In [Adrian Rosebrock's Blog](https://www.pyimagesearch.com/2017/11/06/deep-learning-opencvs-blobfromimage-works/) he say: Mean subtraction is used to help combat illumination changes in the input images in our dataset.
        
 ### Referance
 1. [Holistically-Nested Edge Detection](https://www.pyimagesearch.com/2019/03/04/holistically-nested-edge-detection-with-opencv-and-deep-learning/)
 2. [Python, argparse, and command line arguments](https://www.pyimagesearch.com/2018/03/12/python-argparse-command-line-arguments/)
 3. [Deep learning: How OpenCV’s blobFromImage works](https://www.pyimagesearch.com/2017/11/06/deep-learning-opencvs-blobfromimage-works/)
