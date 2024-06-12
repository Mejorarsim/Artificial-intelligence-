## Connect with Me

Explore more projects and connect with me on GitHub:

[Mejorarsim GitHub Profile](https://github.com/Mejorarsim)

---

# OCR with Pytesseract and OpenCV

This project demonstrates Optical Character Recognition (OCR) using Python libraries Pytesseract and OpenCV. The goal is to extract text from images and visualize the detected characters with bounding boxes.

## Installation

Before running the project, ensure you have installed the necessary libraries:

```bash
pip install pytesseract opencv-python
```

Additionally, make sure Tesseract OCR is installed on your system. You can download it from [Tesseract-OCR](https://github.com/tesseract-ocr/tesseract) and set the executable path in the script.

```python
import pytesseract

# Set the path to Tesseract executable
pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files (x86)\Tesseract-OCR\tesseract.exe"
```

## Usage

1. Clone the repository or download the project files.

2. Navigate to the project directory.

3. Replace `'Test1.jpg'` with your own image file name in the script.

4. Run the script `ocr.py`:

   ```bash
   python ocr.py
   ```

5. The script will:
   - Load the specified image file.
   - Resize the image for display purposes.
   - Perform OCR to extract text from the image using Pytesseract.
   - Display the resized image with the extracted text printed to console.
   - Draw bounding boxes around each detected character and display the result.

## Script Explanation

- **Image Loading and Checking**: The script checks if the specified image file exists and loads it using OpenCV (`cv2.imread`).

- **Image Resizing**: The image is resized to ensure compatibility with both Pytesseract (which requires RGB format) and for display purposes (`cv2.resize`).

- **OCR with Pytesseract**: The resized image is converted to RGB format and passed to Pytesseract's `image_to_string` method to extract text from the image.

- **Bounding Boxes**: Pytesseract's `image_to_boxes` method is used to detect characters and their bounding box coordinates. These coordinates are used to draw bounding boxes and overlay the characters on the image using OpenCV functions (`cv2.rectangle` and `cv2.putText`).

- **Display**: The final result, including the image with bounding boxes and the extracted text, is displayed using OpenCV's `cv2.imshow`.

## Example Output

After running the script with your image, you will see the resized image with bounding boxes around detected characters, and the extracted text printed to the console.

---

Feel free to customize the script further based on your specific requirements or expand the README with additional details as needed. This should provide a clear overview for users interested in using or contributing to your OCR project.
