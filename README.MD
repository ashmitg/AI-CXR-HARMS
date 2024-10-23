# AI Harms CXR Project

This repository is dedicated to the AI Harms CXR Project.

## Table of Contents

- [Abstract](#abstract)
- [Project Structure](#project-structure)
- [Model Training](#model-training)
  - [Original Multi-Label Model](#original-multi-label-model)
  - [ConvNeXt Models](#convnext-models)
- [Analysis](#analysis)
  - [Decision Tree Analysis](#decision-tree-analysis)
  - [Grad-CAM Analysis](#grad-cam-analysis)
  - [Further Analysis in `paper.txt`](#further-analysis-in-papertxt)
- [Conclusion](#conclusion)

---

### Abstract
(placeholder)
---

### Project Structure
- **`TEST_score_tabular.csv`**: 
- **`TRAIN_score_tabular.csv`**:
- **`VAL_score_tabular.csv`**: 
---

### Model Training

#### Original Multi-Label Model
The original model used a multi-label classification approach, simultaneously predicting five conditions from CXR images. The model was trained using the following label encoding:

```python
condition_to_index = {
    'Cardiomegaly': 0,
    'Pleural Effusion': 1,
    'Edema': 2,
    'Fracture': 3,
    'Consolidation': 4,  # Consolidation, Lung Opacity, and Pneumonia are treated the same
    'Lung Opacity': 4,
    'Pneumonia': 4
}
```



#### Second Iteration
In the second iteration, five separate ConvNeXt models were trained, each focusing on one of the five labels. This helped in isolating the performance of the models for each specific condition. These models can be found at:

- [Link to ConvNeXt models repository](https://huggingface.co/gotchu/convnext-models)
- [Link to Training performed by jerry]()


## Analysis

### Decision Tree Analysis
Kasper conducted a decision tree analysis to explain how the neural network performs, focusing on how different values of the ViewPosition attribute affected prediction errors. The decision tree shows splits based on whether the X-ray was taken from a Posteroanterior (PA) view or another view. Each node includes a pie chart indicating the proportion of correct vs. incorrect predictions.

- [Link to Kasper's Decision Tree Analysis](https://github.com/kapiblue/cxr-analysis/blob/main/mimic_decision_tree_single_feature.ipynb)

### Grad-CAM Analysis
Ashmit used Grad-CAM (Gradient-weighted Class Activation Mapping) to visualize which parts of the X-rays the models relied on during classification. This analysis supported the finding that the models were potentially using peripheral areas, such as the borders of the X-rays
- [Link to Ashmit's analysis](https://github.com/ashmitg/grad-cams)


### Further Analysis
Jaitra provided additional insights into the project, which are included in the `/paper.txt` file. This document includes an in-depth explanation of the analysis and findings.

## Conclusion
(Placeholder)



## Support

For support, please open an issue


## Contributing

Contributions are always welcome!



## Authors

- [@]()
- [@]()
- [@]()
- [@]()
