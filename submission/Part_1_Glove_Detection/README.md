# Gloved vs Bare Hand Detection

## Dataset
Roboflow Universe – Glove / Hand PPE Dataset

## Model
YOLOv8n (Ultralytics)

## Training
Fine-tuned pretrained YOLOv8n for 20 epochs using labeled glove images.

## Preprocessing
Images resized to 640x640. Default YOLO augmentations applied.

## Inference
Images from input_images are processed and annotated outputs are saved to output
Detection logs are stored as JSON files in logs

## Limitations
Dataset contains only glove annotations; bare hands are treated as background.

## How to Run
1. Upload images to input_images
2. Run detection_script.ipynb
3. Check output and logs
