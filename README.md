# PDF to Image Processor and Comparator

This repository contains a Python script designed for processing PDF files to extract images, converting those images to grayscale, displaying them, and highlighting differences between two such images. The script utilizes a combination of libraries including pdf2image, cv2 (OpenCV), numpy and PIL (Python Imaging Library) and employs matplotlib for visualization purposes.

### Features

PDF to Image Conversion: Converts pages from PDF files into images for further processing.

Automatic Image Rotation: Applies EXIF-based orientation to correct the image's rotation automatically.

Image Resizing: Adjusts the size of the extracted images to a specified target size, maintaining the aspect ratio.

Grayscale Conversion: Converts images to grayscale to simplify processing and reduce variations.

Difference Highlighting: Calculates and displays the differences between two images, highlighting changes or discrepancies.

Overlay Visualization: Creates an overlay of the difference image on one of the original images to visually represent differences.

Implementation Details

### Libraries Used

pdf2image: For converting PDF files into images.

cv2 (OpenCV): For image processing tasks such as conversion to grayscale, calculating differences between images and creating overlays.

numpy: For handling arrays and performing numerical operations on image data.

PIL (Python Imaging Library): For image manipulation tasks like resizing and displaying.

matplotlib: For displaying images within a Jupyter notebook environment.

### Approach

PDF Conversion and Processing: The script starts by converting a PDF file into an image. It then automatically corrects the image's orientation and resizes it to a specified target size. The image is then converted to grayscale to reduce variations and simplify further processing.

Displaying Processed Images: The processed images are displayed using matplotlib, allowing for a visual inspection of the images after conversion and processing.

Highlighting Differences: To highlight differences between two images, the script first ensures that both images have the same dimensions. It then calculates the absolute difference between the images, inverts the difference image to make discrepancies more visible and normalizes the result. This difference image is then overlaid on one of the original images, creating a composite image that visually highlights the differences.

Saving Results: The final overlay image, which highlights differences between the two processed images, is saved to disk as a JPEG file.

### Usage

Ensure you have the necessary libraries installed:

#
pip install pdf2image opencv-python-headless numpy Pillow matplotlib
#

To use the script, simply run it in a Jupyter notebook or other Python environment. Modify the pdf_path and save_path parameters as needed to specify the input PDF files and the desired location for the processed images.

### Additional Information

This script is designed for use in environments where visual comparison of documents or images extracted from PDF files is required. It is particularly useful for tasks like document verification, automated proofreading or any scenario where highlighting visual differences between documents is beneficial.
