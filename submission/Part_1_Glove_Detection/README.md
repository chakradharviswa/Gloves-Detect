## Dataset
Public PPE glove detection dataset sourced from Roboflow Universe.

## Model Used
YOLOv8 (Ultralytics)

## Training
The model was fine-tuned on the dataset for 20 epochs using a GPU.
Images were resized to 640x640.

## Preprocessing
Standard YOLO augmentations such as scaling and flipping were applied.

## What Worked
The model performs well under normal lighting conditions and clear hand visibility.

## What Didn’t
Performance drops for blurred images and partially visible hands.

## How to Run
Place input images in the input_images folder and run:
python detection_script.ipynb
