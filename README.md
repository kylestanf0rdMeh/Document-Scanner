# Document Scanner

This project provides a simple document scanner using OpenCV and Python. The scanner detects the edges of a document, finds the contour representing the document, and applies a perspective transform to obtain a top-down view of the document.

## Steps

1. **Detect edges**: Convert the image to grayscale, blur it, and find edges using the Canny edge detector.
2. **Find contours**: Use the edges to find the contour (outline) representing the piece of paper being scanned.
3. **Apply perspective transform**: Transform the perspective to obtain a top-down view of the document.

## Requirements

- Python 3.x
- OpenCV
- imutils
- scikit-image

## Installation

Install the required packages using pip:
```
sh
pip install opencv-python imutils scikit-image
```


## Usage

To run the document scanner, use the following command in your terminal:

```
sh
python scan.py --image images/receipt.jpg
```


Replace `images/receipt.jpg` with the path to the image you want to scan.

## Code Overview

### `scan.py`

This script performs the following tasks:

1. Parses the command-line arguments to get the path to the image.
2. Loads the image and resizes it for easier processing.
3. Converts the image to grayscale, blurs it, and detects edges.
4. Finds the contours in the edged image and identifies the contour representing the document.
5. Applies a perspective transform to obtain a top-down view of the document.
6. Displays the original and scanned images.

### `transform.py`

This module provides functions to:

1. Order the points of the contour to ensure a consistent order.
2. Apply a four-point perspective transform to obtain a top-down view of the document.

## Example

Here is an example of how to run the scanner:
```
sh
python scan.py --image images/receipt.jpg
```


This command will display the original image, the edge-detected image, the contour of the document, and the final scanned document.

## License

This project is licensed under the MIT License.