# parameter-optimization
# SVM Hyperparameter Tuning on Sensorless Drive Diagnosis Dataset

This project applies hyperparameter optimization on the [Sensorless Drive Diagnosis dataset](https://archive.ics.uci.edu/ml/datasets/dataset+name) using Support Vector Machines (`NuSVC` from `sklearn`). It explores different strategies to balance model accuracy and training time.

---

## 📁 Files

| File | Description |
|------|-------------|
| `Sensorless_drive_diagnosis.txt` | UCI dataset with 48 features and 11 motor condition classes |
| `svm_fast_tuning.ipynb` | Colab notebook for running SVM optimization |
| `superfast_convergence_graph.png` | Plot showing accuracy over trials |
| `svm_results.csv` | (Optional) Table with sample-wise best accuracies |
| `README.md` | This documentation |

---

##  Optimization Approach

- Model: `NuSVC` (non-linear SVM with parameter `nu`)
- Methods Tested:
  - `Optuna` (slowest, full Bayesian optimization)
  - `RandomizedSearchCV` (balanced)
  - ✅ **Minimal Manual Loop** (fastest & used in final version)

---

## 📊 Results (Summary)

- Accuracy achieved: ~97% with `rbf` kernel and `nu ≈ 0.1`
- Best kernel: `rbf`
- Convergence stabilizes within 3–5 parameter trials

![image](https://github.com/user-attachments/assets/1c5f6d78-7332-4486-8c75-a17999959d28)



---

