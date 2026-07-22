# TIGER Grand Challenge — Segmentation Track (Tumor / Stroma / Rest)

*Report generated: 2026-07-22 10:12*

## Dataset Summary

- **Patch size:** 256x256
- **Sources:** RUMC, JB, TCGA
- **Preprocessing:** Macenko stain normalization, 7-class -> 3-class remap (Rest/Tumor/Stroma), ImageNet normalization at training time
- **Split:** 70/15/15 at the image (slide) level before patching, stratified by source

## Results

1 model configuration(s) evaluated. Sorted by mIoU (mean Intersection-over-Union across Rest, Tumor, Stroma).

| architecture    | encoder   | loss_type   | class_weights   | augmentation   |   test_miou |   test_mean_f1 |   iou_Rest |   f1_Rest |   iou_Tumor |   f1_Tumor |   iou_Stroma |   f1_Stroma |
|:----------------|:----------|:------------|:----------------|:---------------|------------:|---------------:|-----------:|----------:|------------:|-----------:|-------------:|------------:|
| unet_pretrained | resnet34  | dice_ce     | True            | True           |     0.56549 |       0.721445 |   0.535796 |  0.697744 |    0.532701 |   0.695114 |     0.627972 |    0.771478 |

**Best configuration:** `unet_pretrained` (encoder: resnet34) — mIoU = 0.5655, mean F1 = 0.7214

## Comparison Charts

![Segmentation model comparison](segmentation_comparison_chart.png)

![Per-class IoU comparison](segmentation_per_class_iou_chart.png)

## Notes

- Stain normalization (Macenko) and the 7-class -> 3-class remap (`{0:0, 1:1, 2:2, 3:0, 4:0, 5:0, 6:2, 7:0}`) follow the official TIGER baseline directly — these were not open decisions for this track.
- `class_weights=True` runs use inverse-frequency loss weighting to address the Rest-heavy class imbalance found in the Segmentation EDA.