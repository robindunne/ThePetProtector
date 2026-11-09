# Pet Protector – White Cat Detection

This project includes trained YOLOv5 and YOLOv8 models to detect a specific white cat in images or video. The models are already trained and ready to run.

## Model Performance

| Model   | mAP@0.5 | Precision | Recall | F1 Score |
|---------|---------|-----------|--------|----------|
| YOLOv5  | 0.776   | 0.596     | 0.938  | 0.73     |
| YOLOv8  | 0.329   | 0.3–0.5   | 0.4    | 0.40     |

**Use YOLOv5.** It performs better on the dataset.

## Setup

Install the required dependencies:

```bash
pip install -r requirements.txt

HOW TO RUN:
YOLOv5: 
cd yolov5
python detect.py \
  --weights ../runs/train/pet_protector_model/weights/best.pt \
  --source ../test_images/your_image.jpg \
  --conf 0.25 \
  --img 640

YOLOv8:
cd yolov8
yolo task=detect \
  mode=predict \
  model=runs/detect/train/weights/best.pt \
  source=test_images/your_image.jpg
