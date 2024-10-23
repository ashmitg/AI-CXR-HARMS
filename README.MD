# AI Harms CXR Project

## Table of Contents
- [Abstract](#abstract)
- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Data](#data)
- [Methodology](#methodology)
- [Model Development](#model-development)
- [Analysis](#analysis)
- [Results](#results)
- [Discussion](#discussion)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [References](#references)

## Abstract
[Placeholde]

## Introduction

### Background
This project investigates potential biases and harms in AI systems used for chest X-ray (CXR) analysis.

### Problem Statement
[placeholder]
## Project Overview

### Objectives
1. [placeholder]

### Key Research Questions
- How do model predictions vary across different patient demographics?
- What role does image acquisition technique play in model performance?
- Are there systematic biases in condition detection?

## Data

### Datasets
- Training Set: `TRAIN_score_tabular.csv`
- Validation Set: `VAL_score_tabular.csv`
- Test Set: `TEST_score_tabular.csv`

### Data Structure
Each dataset contains:
- Patient demographics
- Image metadata
- Clinical annotations
- Model predictions
- Ground truth labels

## Methodology

### Model Architecture

#### Original Multi-Label Model
```python
condition_to_index = {
    'Cardiomegaly': 0,
    'Pleural Effusion': 1,
    'Edema': 2,
    'Fracture': 3,
    'Consolidation': 4,  # Consolidated with Lung Opacity and Pneumonia
    'Lung Opacity': 4,
    'Pneumonia': 4
}
```

#### ConvNeXt Models
Five separate models were trained for individual conditions:


### Training Process
- Architecture: ConvNeXt
- Loss Function: [Placeholder]
- Optimization: [Placeholder]
- Learning Rate: [Placeholder]
- Batch Size: [Placeholder]
- Training Duration: [Placeholder]

## Analysis

### Decision Tree Analysis
- Conducted by Kasper
- Focus on ViewPosition attribute impact
- Analysis of PA vs. other view angles
- Visualization of prediction error patterns
- Repository: [Decision Tree Analysis](https://github.com/kapiblue/cxr-analysis/blob/main/mimic_decision_tree_single_feature.ipynb)

### Grad-CAM Analysis
- Conducted by Ashmit
- Visualization of model attention
- Identification of relevant image regions
- Analysis of potential shortcuts in model decision-making
- Repository: [Grad-CAM Analysis](https://github.com/ashmitg/grad-cams)

### Fairness Metrics
-

## Results

### Model Performance
[Placeholder for model performance metrics across different groups]

### Bias Analysis
[Placeholder for detailed bias analysis findings]

### Fairness Evaluation
[Placeholder for fairness metric results]

## Discussion

### Key Findings
[Placeholder for main conclusions]

### Limitations
[Placeholder for study limitations]

### Future Work
[Placeholder for proposed future research directions]

## Installation

### Prerequisites
```bash

```

### Setup
```bash

```

## Usage

### Model Training
```bash

```

### Evaluation
```bash

```

## Contributing
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License
[Placeholder for license information]

## References
1. [Placeholder for references]
2. Link to ConvNeXt models: [HuggingFace Repository](https://huggingface.co/gotchu/convnext-models)
3. Additional analysis in `paper.txt`
## Support

For support, please open an issue


## Authors

- [@]()
- [@]()
- [@]()
- [@]()
