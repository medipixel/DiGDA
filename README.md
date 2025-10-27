# Diffusion-Based User-Guided Data Augmentation for Coronary Stenosis Detection

by [Sumin Seo](https://scholar.google.com/citations?user=QzzhNTYAAAAJ&hl=en), [In Kyu Lee](https://scholar.google.com/citations?user=WYCKXg0AAAAJ&hl=en), Hyun-Woo Kim, Jaesik Min, and Chung-Hwan Jung

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]  
[![arXiv Paper](https://img.shields.io/badge/arXiv-2508.00438-orange.svg?style=flat)](https://arxiv.org/pdf/2508.00438)

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

## News
📣 **2025/10/27**: Our relabeled dataset and [final manuscript](https://papers.miccai.org/miccai-2025/0238-Paper3613.html) are now available online.

📣 **Accepted at MICCAI 2025!** Check out our [arXiv paper](https://arxiv.org/pdf/2508.00438), and the dataset will be updated soon.

## Introducing DiGDA
We present DiGDA, a novel data augmentation method for lesion detection that generates realistic angiography images with varying levels of lesion severity by conditioning a diffusion model on lesion-specific vessel masks. 
Our pipeline produces high-quality synthetic images that preserve anatomical vessel structures while reflecting user-specified lesion severity, including highly severe cases. 
We demonstrate that incorporating these user-guided synthetic images into lesion detection pipelines significantly improves detection performance.  
As part of our contribution, we release the updated annotations of the [ARCADE dataset](https://doi.org/10.5281/zenodo.10390295), specifically re-annotated for stenosis severity classification and lesion detection tasks.

## How to Use Our Dataset
1. Download images from [ARCADE dataset](https://doi.org/10.5281/zenodo.10390295) and place them under the corresponding directory: `data/{split}/images`.
2. Check out our annotations:
  - Each annotation is provided in YOLO format: `class x_center y_center width height`. All coordinates are normalized by the original image size.
  - Class information:
    - **Class 0**: **Non-severe** lesion (%DS ≥ 50% and %DS < 70%) evaluated by our in-house experienced clinicians.
    - **Class 1**: **Severe** lesion (%DS ≥ 70%).
3. Train or evaulate your model using our relabeled dataset.
4. Share your experience with us!
  - We welcome feedback, suggestions, and collaboration.
  - Feel free to contact the authors (sumin.seo@medipixel.io).

## Citation and License
If you use our relabeled dataset, please cite both our paper and the ARCADE dataset paper, and follow the [CC BY-NC-SA 4.0 license](https://creativecommons.org/licenses/by-nc-sa/4.0/).
```
@inproceedings{seo2025diffusion,
  author    = {Seo, Sumin and Lee, In Kyu and Kim, Hyun-Woo and Min, Jaesik and Jung, Chung-Hwan},
  title     = {Diffusion-Based User-Guided Data Augmentation for Coronary Stenosis Detection},
  booktitle = {International Conference on Medical Image Computing and Computer-Assisted Intervention},
  year      = {2025},
  publisher = {Springer},
  note      = {DOI will be available upon publication}
}

@article{popov2024dataset,
  author    = {Popov, Maxim and Amanturdieva, Akmaral and Zhaksylyk, Nuren and Alkanov, Alsabir and Saniyazbekov, Adilbek and Aimyshev, Temirgali and Ismailov, Eldar and Bulegenov, Ablay and Kuzhukeyev, Arystan and Kulanbayeva, Aizhan and others},
  title     = {Dataset for Automatic Region-Based Coronary Artery Disease Diagnostics Using X-ray Angiography Images},
  journal   = {Scientific Data},
  volume    = {11},
  number    = {1},
  pages     = {20},
  year      = {2024},
  publisher = {Nature Publishing Group UK, London}
}
```
## 📧 Contact Info
If you have any questions, please contact the corresponding author, Sumin Seo (sumin.seo@medipixel.io).
