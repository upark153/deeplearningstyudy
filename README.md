# deeplearningstyudy

## 1. Setup
### 1.1 Install Dependencies 
```
!pip install tensorflow==2.4.1 tensorflow-gpu==2.4.1 opencv-python matplotlib
```
### 1.2 Import Dependencies
```
import cv2
import os
import random
import numpy as np
from matplotlib import pyplot as plt
```
```
from tensorflow.keras.models import Model
from tensorflow.keras.layers import Layer, Conv2D, Dense, MaxPooling2D, Input, Flatten
import tensorflow as tf
```
```
Model(inputs=[inputimage, verificationimage], outputs=[1,0])
```
```
Input(shape=)
```
### 1.3 Set GPU Growth
```
# Avoid OOM errors by setting GPU Memory Consumption Growth
gpus = tf.config.experimental.list_physical_devices('GPU')
for gpu in gpus:
    tf.config.experimental.set_memory_growth(gpu, True)
```
```
gpus, len(gpus) # gpu 확인 코드
```
> [PhysicalDevice(name='/physical_device:GPU:0', device_type='GPU')], 1 

### 1.4 Create Folder Structures
```
# Setup paths
POS_PATH = os.path.join('content', 'drive', 'MyDrive', 'data8', 'positive')
NEG_PATH = os.path.join('content', 'drive', 'MyDrive', 'data8', 'negative')
ANC_PATH = os.path.join('content', 'drive', 'MyDrive', 'data8', 'anchor')
```
```
# Make the directories
os.makedirs(POS_PATH)
os.makedirs(NEG_PATH)
os.makedirs(ANC_PATH)
```

## 2. Collect Positives and Anchors
### 2.1 Untar Labelled Faces in the Wild Dataset
### 2.2 Collect Positive and Anchor Classes
## 3. Load and Preprocess Images
