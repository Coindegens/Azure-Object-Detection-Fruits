# Detect Objects in Images with Azure AI Custom Vision

This project demonstrates how to use Azure AI Custom Vision to build and deploy an object detection model that can identify and locate fruits (apples, bananas, and oranges) in images.

## Prerequisites

- Azure subscription
- Visual Studio Code
- Git
- Python 3.x
- Azure Custom Vision resources (training and prediction)

## Setup

1. Create Azure Resources:
   - Create Custom Vision resources in Azure Portal (both training and prediction)
   - Note down the endpoints and keys for both resources

2. Install required packages:
```bash
pip install azure-cognitiveservices-vision-customvision==3.1.1
```

## Project Structure

```
azure-ai-vision/
├── training-images/         # Images for model training
└── Python/
    ├── train-detector/     # Python training code
    └── test-detector/      # Python testing code
```

## Usage

### 1. Create Custom Vision Project

1. Go to [Custom Vision Portal](https://customvision.ai)
2. Create new project:
   - Type: Object Detection
   - Domain: General

### 2. Train the Model

Either use the portal UI or the provided training code:

```bash
cd Python/train-detector
python train-detector.py
```

### 3. Test the Model

```bash
cd Python/test-detector
python test-detector.py
```

## Configuration

Update the `.env` configuration file with your:
- Training endpoint and key
- Prediction endpoint and key
- Project ID
- Model name

## Resources

- [Custom Vision Documentation](https://docs.microsoft.com/azure/cognitive-services/custom-vision-service/)
- [Azure AI Services](https://azure.microsoft.com/services/cognitive-services/)

