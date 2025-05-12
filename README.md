# Cross-Lingual Word Embedding Alignment

This repository contains my implementation for the Sarvam Research Fellowship assignment on aligning English and Hindi word embeddings, focusing on both supervised and unsupervised cross-lingual alignment methods.

## Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Repository Structure](#repository-structure)
- [Data Preparation](#data-preparation)
- [Execution Guide](#execution-guide)
- [Results and Evaluation](#results-and-evaluation)
- [References](#references)
- [Contact](#contact)
- [License]

## Project Overview

Cross-lingual word embeddings are essential for multilingual NLP tasks such as translation, information retrieval, and semantic similarity. This project aligns monolingual FastText embeddings for English and Hindi into a shared cross-lingual space using both supervised (Procrustes method) and unsupervised (adversarial training with CSLS) approaches. The work follows the guidelines provided in the Sarvam Research Fellowship assignment.

## Objectives

- Implement supervised cross-lingual alignment using the Procrustes method.
- Evaluate translation accuracy using Precision@1 and Precision@5 metrics.
- Conduct an ablation study on the impact of bilingual lexicon size.
- (Optional) Implement and compare an unsupervised alignment approach using adversarial training and CSLS.

## Repository Structure

```
├── main_objective_Haryaksh.ipynb        # Supervised Procrustes alignment (main task)
├── optional_objective_Haryaksh.ipynb    # Unsupervised adversarial alignment (optional task)
├── data/                               # Folder for embedding and dictionary files
│   ├── en-hi.txt                       # Training dictionary (from MUSE)
│   ├── en-hi.test.txt                  # Test dictionary (from MUSE)
│   ├── cc.en.300.vec                   # English FastText embeddings
│   └── cc.hi.300.vec                   # Hindi FastText embeddings
└── README.md                           # Project documentation
```

## Data Preparation

- Use pre-trained FastText embeddings for English (`cc.en.300.vec`) and Hindi (`cc.hi.300.vec`).
- Bilingual dictionaries (`en-hi.txt` for training, `en-hi.test.txt` for testing) are sourced from the [MUSE dataset](https://github.com/facebookresearch/MUSE).
- Limit vocabulary to the top 100,000 most frequent words in each language.

## Execution Guide

1. **Google Colab Recommended**: Open either notebook (`main_objective_Haryaksh.ipynb` or `optional_objective_Haryaksh.ipynb`) in Google Colab for best compatibility.
2. **Data Setup**: 
   - Create a folder named `sarvam-assignment-folder` in your Google Drive.
   - Upload the required embedding and dictionary files into this folder.
3. **Notebook Instructions**: 
   - Follow the step-by-step instructions in each notebook.
   - All dependencies (NumPy, SciPy, PyTorch, etc.) are installed and used within the notebooks.
   - For the optional task, a GPU with at least 19GB RAM is recommended due to computational requirements.
4. **Reproducibility**: All code is documented, and key steps are explained for clarity and reproducibility.

## Results and Evaluation

- **Supervised Alignment**: Achieves strong translation accuracy, with Precision@1 and Precision@5 reported on the MUSE test dictionary.
- **Ablation Study**: The notebooks include experiments with varying bilingual lexicon sizes to analyze their impact on alignment quality.
- **Optional Task**: The adversarial training and CSLS-based unsupervised alignment method is implemented for further comparison, with results discussed in the notebook.
- **Sample Output**: Detailed translation examples and evaluation metrics are included in the notebook outputs.

## References

- [MUSE: Multilingual Unsupervised and Supervised Embeddings](https://github.com/facebookresearch/MUSE)
- [FastText Word Embeddings](https://fasttext.cc/)
- Conneau et al. (2017), "Word Translation Without Parallel Data"

## Contact

For questions or clarifications, please contact:  
**Haryaksh Manuh Bhardwaj**  
Email: f20220900@goa.bits-pilani.ac.in



## License
This project is proprietary material developed for Sarvam AI fellowship selection. All rights reserved.

---

*This project was developed as part of the Sarvam Research Fellowship selection process. All materials are intended for evaluation by the Sarvam AI team.*

