# Defect-Detection-and-localization-BOLD


**Overview**
This project focuses on detecting and localizing bolts using image processing and deep learning techniques, specifically from two images.

**Requirements**
- PyTorch
- -OpenCV3
- NumPy
- PIL
- scikit-image
- Matplotlib

**How to Run**
1. Open a terminal in the directory.
   
3. Run the defect_detector.py script with Python, specifying the image path using the --imagepath argument.

**Example:**
python defect_detector.py --imagepath D:\switchon\main_data\good_image.png

3. The class of the image (withbolt or withoutbolt) will be printed. If the image is classified as withbolt, the coordinates of the detected bolt will also be printed.

4. The image will be displayed with the class label in the title. If the image belongs to the withbolt class, a rectangular bounding box will be shown around the bolt. Press any key to close the image, after which the class and coordinates will be printed again.

**Additional Information**
- The two images were augmented to create a dataset of 4860 images.
- A ResNet34-based classifier was built for the cropped (and augmented) images, achieving an accuracy of about 92%.
- The full pipeline, tested on the 4860 augmented images, achieved an accuracy of about 91%.
- The entire process took 1034 seconds, averaging 0.21 seconds per image after loading the model.
