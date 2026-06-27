# RT-DETR v2 Object Detection Fine-Tuning

Fine-tuning **RT-DETR v2** for custom object detection using the **Hugging Face Transformers** ecosystem.

The model is trained to detect three classes:

* 🗑️ Trash
* 🗑️ Bin
* ✋ Hand

The project demonstrates the complete workflow—from dataset preparation and training to inference and deployment with Hugging Face Spaces.

---

## Live Demo

Try the Gradio application here:

**Hugging Face Space:** https://huggingface.co/spaces/ashutosh-kedar/ECO-VISION

Upload an image and the model detects:

* Trash
* Bin
* Hand

It also visualizes the predicted bounding boxes and confidence scores.

---

## Fine-Tuned Model

The trained model is available on Hugging Face:

**Model:** https://huggingface.co/ashutosh-kedar/rt-detr-v2-finetuned-trash-hand-bin-bbox

You can directly load it using the Transformers library.

---

## Project Overview

This repository contains everything required to:

* Fine-tune RT-DETR v2 on a custom dataset
* Prepare datasets in Hugging Face format
* Train using Hugging Face Trainer
* Evaluate model performance
* Run inference on custom images
* Deploy with Gradio on Hugging Face Spaces

---
---

##  Tech Stack

* Python
* PyTorch
* Hugging Face Transformers
* Hugging Face Datasets
* TorchMetrics
* RT-DETR v2
* Gradio
* Hugging Face Spaces

---

##  Model

Base model:

**RT-DETR v2**

RT-DETR v2 is a real-time transformer-based object detector that performs end-to-end object detection without requiring Non-Maximum Suppression (NMS). It offers an excellent balance between speed and accuracy while remaining easy to fine-tune for custom datasets.

---

##  Classes

| ID | Class |
| -- | ----- |
| 0  | Trash |
| 1  | Hand  |
| 2  | Bin   |

---

## Installation

Clone the repository

```bash
git clone https://github.com/ashutosh-kedar/RT-DETR-v2-Object-Detection-Fine-Tuning.git

cd RT-DETR-v2-Object-Detection-Fine-Tuning
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

##  Inference

Example using the Hugging Face model:

```python
from transformers import RTDetrImageProcessor
from transformers import RTDetrV2ForObjectDetection

processor = RTDetrImageProcessor.from_pretrained(
    "ashutosh-kedar/rt-detr-v2-finetuned-trash-hand-bin-bbox"
)

model = RTDetrV2ForObjectDetection.from_pretrained(
    "ashutosh-kedar/rt-detr-v2-finetuned-trash-hand-bin-bbox"
)
```

---

## Use Cases

* Environmental cleanup
* Smart waste management
* Community awareness projects
* Computer Vision learning
* Custom object detection workflows

---

##  Note

This model was fine-tuned on a relatively small custom dataset.

While it performs well on many examples, it may still produce incorrect detections in challenging scenarios. The primary goal of this project is to demonstrate an end-to-end object detection pipeline using the Hugging Face ecosystem.

---

## Learning Outcomes

During this project I learned:

* Fine-tuning RT-DETR v2
* Object detection with Hugging Face Transformers
* Custom dataset preprocessing
* Bounding box formatting
* Evaluation using mAP
* Inference pipeline creation
* Gradio deployment
* Hugging Face Hub integration

---

##  If you found this project useful

If this repository helped you, consider giving it a ⭐ on GitHub.

Feedback and contributions are always welcome!
