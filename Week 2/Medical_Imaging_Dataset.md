## Dataset 1 - Skin Lesion Images for Melanoma

The ISIC 2019 dataset is a large dermoscopic skin lesion dataset containing **25,331** images across 8 diagnostic classes. The 8 diagnostic Classes are :-

- Melanoma (MEL)
- Melanocytic Nevus (NV)
- Basal Cell Carcinoma (BCC)
- Actinic Keratosis (AK)
- Benign Keratosis (BKL)
- Dermatofibroma (DF)
- Vascular Lesion (VASC)
- Squamous Cell Carcinoma (SCC)
  
The class distribution is heavily skewed — 

|Class|Images |
|-----|-------|
|Melanocytic Nevus (NV)|12,875 (50.83%)|
|Melanoma (MEL)|4,522 (17.85%)|
|BCC|3,323 (13.12%)| 
|BKL|2,624 (10.36%)| 
|AK|867 (3.42%)|
|SCC|628 (2.48%)|
|VASC|253 (1%)|
|Dermatofibroma|239 images (0.94%)|

The imbalance factor is approximately 54× between the largest and smallest classes.

**Challenges**

- Images exhibit considerable variation in resolution, ranging from 576×768 to 1024×1024 pixels, distributed across 101 unique resolution sizes.
- Images were acquired at multiple sites with different preprocessing methods — HAM10000 images are 600×450, BCN_20000 images are 1024×1024, and the MSK dataset contains various sizes. This introduces noise from inconsistent capture conditions

---
## Dataset 2 - Brain Cancer

This dataset contains a comprehensive collection of MRI images for brain cancer research, specifically aimed at supporting medical diagnostics. The dataset includes a total of 6056 images, uniformly resized to 512x512 pixels. These images were collected from various hospitals across Bangladesh with the direct involvement of experienced medical professionals to ensure accuracy and relevance. The three Classes are:-

- Brain_Tumor
- Brain_Menin
- Brain_Giloma
  
The class distribution is — 

|Class|Images |
|-----|-------|
|Brain_Tumor|2048 (33.82%)|
|Brain_Menin|2004 (33.09%)|
|Brain_Giloma|2004 (33.09%)| 

The classes are considerably distributed nicely.




