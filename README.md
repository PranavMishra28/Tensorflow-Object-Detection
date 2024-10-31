# TensorFlow Object Detection Project

## Overview
This project demonstrates object detection using TensorFlow. It involves capturing images through a webcam, labeling them, and training a model to detect custom objects.

## Project Structure
```
├── images/                      # Directory to store collected images
├── 1. Image Collection.ipynb    # Notebook to capture images
├── 2. Training and Detection.ipynb  # Notebook to train the model
└── README.md                    # Project documentation
```

## Requirements
Make sure you have the following dependencies installed:
- Python 3.x
- TensorFlow 2.x
- OpenCV
- PyQt5

To install the dependencies, use:
```bash
pip install tensorflow opencv-python pyqt5 lxml
```

## Steps to Run the Project

### 1. Image Collection
1. Connect your webcam.
2. Open `1. Image Collection.ipynb`.
3. Run the cells to capture images. Change `labels` and `number_imgs` variables as needed.

### 2. Training and Detection
1. Open `2. Training and Detection.ipynb`.
2. Download pre-trained models from the TensorFlow Model Zoo.
3. Update the paths and train the model using your collected images.

## Image Labeling
1. Install LabelImg:
   ```bash
   pip install labelImg
   ```
2. Clone the repository:
   ```bash
   git clone https://github.com/tzutalin/labelImg
   cd labelImg && make qt5py3
   ```
3. Use LabelImg to annotate the images.

## Directory Setup
Ensure the following directories exist:
```bash
mkdir -p Tensorflow/workspace/images/collectedimages
mkdir -p Tensorflow/workspace/images/train
mkdir -p Tensorflow/workspace/images/test
```

## Model Training
1. Set up the pipeline configuration.
2. Train the model using the custom images.
3. Evaluate the model and export it for inference.

## Exporting the Model
Use the following command to export the trained model:
```bash
python exporter_main_v2.py --input_type image_tensor --pipeline_config_path path/to/config --trained_checkpoint_dir path/to/checkpoint --output_directory path/to/export
```

## Troubleshooting
- Ensure your Python environment is properly configured.
- Restart the kernel if packages are not detected.
- Use `!pip install --upgrade <package>` to update dependencies.

## Acknowledgments
This project uses TensorFlow's Object Detection API and LabelImg for annotations. Special thanks to TensorFlow's open-source community.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
