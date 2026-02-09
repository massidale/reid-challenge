# Urban Person Re-Identification via Part-Aware Transformer

This repository contains a research project on **Domain Generalization for Person Re-identification (DG-ReID)**, developed during my academic period at **Universidad Autónoma de Madrid (UAM)**. 

The project focuses on enhancing the generalization capabilities of Transformer-based models in urban surveillance contexts, building upon the **Part-Aware Transformer (PAT)** framework.

## 🚀 Research & Contributions

My work focused on testing the robustness of the PAT architecture under distribution shifts and optimizing the feature embedding space. Key contributions include:

* [cite_start]**Loss Function Analysis**: Implementation and comparative evaluation of **Adaptive Sparse Pairwise Loss (ASPL)** versus standard Triplet Loss[cite: 1, 3].
* [cite_start]**Urban Adaptation**: Fine-tuning the model for urban scenarios to improve the extraction of generic features (e.g., clothing patterns, accessories)[cite: 1, 3].
* [cite_start]**Performance Evaluation**: Comprehensive study using **mAP** and **Cumulative Matching Curve (CMC)** metrics to validate zero-shot generalization[cite: 1].

## 📊 Detailed Report
For a complete technical analysis of the methodology, loss functions (Adaptive Sparse Pairwise Loss vs Triplet Loss), and experimental results, please refer to the full report: **[ReID.pdf](./ReID.pdf)**

## 🛠 Instructions
This implementation is based on [TransReID](https://github.com/damo-cv/TransReID).

1.  **Environment**: 
    ```bash
    conda create -n pat python==3.10
    conda activate pat
    bash environments.sh
    ```
2.  **Configuration**: Modify the model and dataset paths in `./config/PAT.yml`.
3.  **Training**: Run the training script with:
    ```bash
    bash run.sh
    ```
4.  **Evaluation**: 
    ```bash
    python test.py --config ./config/PAT.yml
    ```

## 📜 Citation
This project utilizes the Part-Aware Transformer architecture introduced in:
```bibtex
@inproceedings{ni2023part,
  title={Part-Aware Transformer for Generalizable Person Re-identification},
  author={Ni, Hao and Li, Yuke and Gao, Lianli and Shen, Heng Tao and Song, Jingkuan},
  booktitle={Proceedings of the IEEE/CVF International Conference on Computer Vision},
  year={2023}
}
