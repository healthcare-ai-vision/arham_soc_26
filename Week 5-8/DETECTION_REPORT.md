# TIGER Grand Challenge — Detection Track (Lymphocyte/Plasma Cell Detection)

*Report generated: 2026-07-22 10:09*

## Dataset Summary

- **Total ROI images:** 4016
- **Sources:** RUMC, JB, TCGA
- **Preprocessing:** Macenko stain normalization, resize to 512x512, COCO -> YOLO conversion
- **Split:** 70/15/15 train/val/test, stratified by source

## Results

2 model configuration(s) evaluated. Sorted by mAP@0.5:0.95 (the strictest standard detection metric).

| architecture   |   precision |   recall |       f1 |    map50 |   map50_95 | mask_guided   |
|:---------------|------------:|---------:|---------:|---------:|-----------:|:--------------|
| faster_rcnn    |    0.582759 | 0.671134 | 0.623832 | 0.600687 |   0.517564 | False         |
| yolov8n        |    0.582969 | 0.575276 | 0.579097 | 0.582699 |   0.347509 | False         |

**Best configuration:** `faster_rcnn` — F1 = 0.6238, mAP@0.5 = 0.6007, mAP@0.5:0.95 = 0.5176

## Notes

- `*` in the chart legend indicates mask-guided peritumoral-stroma patch selection was used for that run (see `05_Training_Detection.ipynb`, Step 3).
- Stain normalization (Macenko) was added beyond the official TIGER baseline, based on EDA evidence of clear color-distribution differences across the RUMC/JB/TCGA sources.
