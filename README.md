# HOW OUR MODEL WORKS

We have used YOLO custom-trained model with Tesseract to detect and recognize text within images. Here's a step-by-step explanation of how they work together:

### Step-by-Step Process Object Detection with YOLO:

**Load YOLO Model:** Load your custom-trained YOLO model (best.pt file).

**Detection:**Use the YOLO model to detect objects in the input image. For text detection, the model should be trained to recognize text regions.

**Extract Bounding Boxes:** YOLO will provide bounding boxes for each detected text region.
Image Preprocessing:

**Crop Text Regions:** For each bounding box detected by YOLO, crop the corresponding region from the original image. These cropped images will contain the text that needs to be recognized.

**Optional Enhancements:** Preprocess the cropped images to enhance text readability (e.g., binarization, resizing, denoising).

### Text Recognition with Tesseract:

**OCR on Cropped Images:** Apply Tesseract OCR on each cropped image to recognize the text. Tesseract will convert the images of text into machine-readable text.
**Post-processing:** Optionally, clean up the recognized text (e.g., removing special characters, correcting common OCR errors).
