# License Plate Detection with YOLO and OCR

This repository contains an enhanced method to detect **vehicle license plates** using **YOLO v3** with integrated **OCR (Optical Character Recognition)** capabilities. The system not only detects license plates but also extracts and recognizes the text content, supporting both Arabic and Latin characters.

## ✨ Features

- **Real-time license plate detection** using YOLO v3
- **OCR text extraction** with EasyOCR supporting Arabic and English
- **Multi-language support** for Arabic (تونس) and Latin characters
- **Flexible input options**: images, videos, or webcam
- **High accuracy** with configurable confidence thresholds
- **Automatic output organization** with separate folders for results


## 🔨 Requirements

- Python 3.7+
- OpenCV 4.5+
- EasyOCR 1.6+
- NumPy
- Pillow
- python-bidi
- arabic-reshaper

## 📦 Installation

1. Clone this repository:
```bash
https://github.com/AminePro7/yolo-license-plate-detection.git
cd yolo-license-plate-detection
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

3. **⚠️ IMPORTANT**: Download the YOLO weights file (required for the model to work):
   - **Option 1**: Download from [Google Drive](https://drive.google.com/file/d/1vXjIoRWY0aIpYfhj3TnPUGdmJoHnWaOc/)
   - **Option 2**: Download the split RAR files from [this GitHub repository](https://github.com/alitourani/yolo-license-plate-detection/tree/master/weights) and extract them
   - Place the extracted `model.weights` file in the project root directory
   - **Note**: The weights files are not included in this repository due to their large size (~248 MB)

## 💡 Usage

### Detect license plates in a single image:
```bash
python object_detection_yolo.py --image=image1.jpeg
```

### Process a video file:
```bash
python object_detection_yolo.py --video=cars.mp4
```

### Use webcam for real-time detection:
```bash
python object_detection_yolo.py
```

## 📁 Project Structure

```
yolo-license-plate-detection/
├── object_detection_yolo.py    # Main detection script with OCR
├── classes.names               # Class labels file
├── darknet-yolov3.cfg         # YOLO configuration
├── model.weights              # YOLO weights (download required)
├── convert.py                 # Utility for dataset conversion
├── requirements.txt           # Python dependencies
├── image*.jpeg               # Sample test images
├── weights/                  # Split weight files (RAR format)
└── yolo_output_images/       # Output directory for processed images
```

## 🎯 Configuration

You can adjust the detection parameters in `object_detection_yolo.py`:

- `confThreshold = 0.5`: Confidence threshold for detection
- `nmsThreshold = 0.4`: Non-maximum suppression threshold
- `CONFIDENCE_THRESHOLD = 0.50`: OCR confidence threshold

## 🔍 OCR Features

The system includes advanced OCR capabilities:

- **EasyOCR integration** for robust text recognition
- **Arabic text support** for regional license plates
- **Text filtering and cleaning** to improve accuracy
- **Confidence-based filtering** to reduce false positives
- **Automatic text ordering** from left to right

## 🧑‍💻 Contributers

<a href="https://github.com/alitourani/yolo-license-plate-detection/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=alitourani/yolo-license-plate-detection" />
</a>

## 🔗 Citation

Please cite the following paper in case you have used this repo:

```
@inproceedings{Khazaee2020,
	author = {Khazaee, Saeed and Tourani, Ali and Soroori, Sajjad and Shahbahrami, Asadollah and Suen, Ching Y.},
	title = {{A Real-Time License Plate Detection Method Using a Deep Learning Approach}},
	booktitle = {Lecture Notes in Computer Science (including subseries Lecture Notes in Artificial Intelligence and Lecture Notes in Bioinformatics)},
	doi = {10.1007/978-3-030-59830-3_37},
	isbn = {9783030598297},
	issn = {16113349},
	keywords = {Automatic number-plate detection,Deep learning,Image processing,Intelligent Transportation Systems},
	pages = {425--438},
	volume = {12068 LNCS},
	year = {2020}
}
```
