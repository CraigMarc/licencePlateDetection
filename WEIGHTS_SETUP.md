# YOLO Weights Setup Guide

## Option 1: Download Pre-trained Weights

Download the YOLO weights file from [this Google Drive link](https://drive.google.com/file/d/1vXjIoRWY0aIpYfhj3TnPUGdmJoHnWaOc/) and place it in the project root directory as `model.weights`.

## Option 2: Download and Extract Split RAR Files

Download the split RAR files from [this GitHub repository](https://github.com/alitourani/yolo-license-plate-detection/tree/master/weights) and place them in a `weights/` folder, then:

### On Windows:
1. Install WinRAR or 7-Zip
2. Navigate to the `weights/` folder
3. Right-click on `model.part01.rar`
4. Select "Extract Here" or "Extract to weights/"
5. Move the extracted `model.weights` file to the project root directory

### On Linux/Mac:
```bash
# Install unrar if not already installed
# Ubuntu/Debian: sudo apt-get install unrar
# macOS: brew install unrar

# Extract the RAR files
cd weights/
unrar x model.part01.rar
mv model.weights ../
cd ..
```

## Verification

After placing the weights file, verify it's in the correct location:

```
yolo-license-plate-detection/
├── model.weights              # This file should be here
├── object_detection_yolo.py
├── classes.names
└── ...
```

The weights file should be approximately 248 MB in size.

## Troubleshooting

- **File not found error**: Make sure `model.weights` is in the project root directory
- **Extraction issues**: Ensure all RAR parts (part01 through part10) are present
- **Size mismatch**: The extracted file should be around 248 MB
