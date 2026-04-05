# Swin Transformer for Face Anti-Spoofing under Adversarial Attacks

## 📌 Overview

This project studies the performance and robustness of the Swin Transformer model for face anti-spoofing.
We compare different transfer learning strategies and evaluate their behavior under adversarial attacks (FGSM and PGD).

We also investigate the impact of adversarial training in improving model robustness.

---

## 🎯 Objectives

* Compare multiple transfer learning strategies:

  * Freeze all layers
  * Fine-tune all layers
  * Partial fine-tuning (3 strategies)
* Evaluate robustness against:

  * FGSM attack
  * PGD attack
* Improve robustness using adversarial training

---

## 📊 Dataset

We use the **LCC FASD dataset**:

👉 https://www.kaggle.com/datasets/faber24/lcc-fasd

⚠️ Note: The dataset (~5GB) is not included in this repository.
Please download it manually from Kaggle and update the dataset path in the notebooks.

---

## 📁 Repository Structure

```
antispoofing-swin-transformer/
│
├── notebooks/     # All experiments
├── models/        # Trained models
└── README.md
```

---

## 📓 Notebooks

| Notebook                         | Description                                                 |
| -------------------------------- | ----------------------------------------------------------- |
| `01_swin_freeze_all.ipynb`       | Swin Transformer with frozen layers + evaluation on attacks |
| `02_swin_finetune_all.ipynb`     | Full fine-tuning strategy                                   |
| `03_swin_partial_finetune.ipynb` | 3 partial fine-tuning strategies + attack evaluation        |
| `04_adversarial_training.ipynb`  | Adversarial training (Fine-tune strategy 2)                 |

---

## ⚔️ Adversarial Attacks

We evaluate the model using:

* **FGSM (Fast Gradient Sign Method)**
* **PGD (Projected Gradient Descent)**

Each model is tested on:

* Clean data
* Adversarial samples

---

## 🧠 Adversarial Training

Adversarial training is applied on the best-performing model (Fine-tune Strategy 2)
by injecting adversarial examples during training to improve robustness.

---

## 📈 Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-score

---

## 🚀 Key Insights

* Transfer learning strategy strongly impacts robustness
* Fine-tuning increases performance but may reduce robustness
* Adversarial training improves resistance to attacks

---

## ▶️ How to Run

1. Download the dataset from Kaggle
2. Update dataset path in notebooks
3. Run notebooks in order:

```
01 → 02 → 03 → 04
```

---

## 👨‍💻 Author

Tanani Mouhsin
Big Data & AI Engineering Student
