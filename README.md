## Performance Comparison

The proposed model was evaluated against standard pothole detection architectures, including YOLOv11n-seg and a hybrid YOLOv11n + Mask R-CNN approach.

### Quantitative Results

| Model  | Precision (%) | Recall (%) | mAP@50 (%) | Parameters |
|------|------:|------:|------:|------:|
| YOLOv11n + Mask R-CNN | 93.92 | 93.95 | 92.44 | 46.3M |
| YOLOv11n-seg | 87.00 | 90.60 | 94.47 | 2.3M |
| **YOLOv11n + SE + CBAM + Dilated Convolution (Proposed)** | **92.50** | **90.10** | **95.61** | **2.82M** |

### Key Observations

- The proposed model achieved the **highest mAP@50 of 95.61%**, outperforming all baseline models.
- Despite having only **2.82 million parameters**, it significantly outperformed the much larger YOLOv11n + Mask R-CNN model with **46.3 million parameters**.
- The integration of **SE attention**, **CBAM**, and **dilated convolutions** improved feature representation and boosted small pothole detection accuracy.
- The model provides an excellent trade-off between detection performance and computational efficiency, making it suitable for real-world UAV deployment.

### Qualitative Results

Visual comparisons show that the proposed model:

- Detects small and irregularly shaped potholes more accurately.
- Produces tighter bounding boxes.
- Reduces false positives and missed detections.
- Performs robustly under varying road textures and lighting conditions.
