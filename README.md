# Final Machine Learning Project INT3405E 55

This repository contains the implementation of the final machine learning project, where we utilize ensemble models and perform post-processing with majority voting for submission generation. The project is designed to improve the robustness and accuracy of predictions by combining the outputs of multiple models.

## Table of Contents
- [Project Overview](#project-overview)
- [Models Used](#models-used)
- [Post-Processing](#post-processing)
- [File Structure](#file-structure)
- [Requirements](#requirements)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project involves combining predictions from three machine learning models using ensemble techniques. Specifically, we implement a `VotingRegressor` to aggregate predictions and a custom post-processing pipeline to refine the results. The pipeline includes weighting, majority voting, and tie-breaking strategies.

## Models Used

1. **LightGBM**
   - Optimized gradient boosting algorithm.
   - Handles large datasets efficiently.

2. **XGBoost**
   - Gradient boosting algorithm widely used in competitions.
   - Known for flexibility and scalability.

3. **CatBoost**
   - Gradient boosting library with native categorical data handling.
   - Efficient with high-quality predictions.

## Post-Processing

After generating predictions from the ensemble models, a post-processing pipeline is applied:

1. **Weighted Aggregation**:
   - Combines predictions from two submissions with specified weights.

2. **Majority Voting**:
   - Selects the most frequent prediction among weighted results and individual models.
   - Handles tie cases with a fallback strategy (e.g., mean).

3. **Final Submission**:
   - Outputs the final `id` and predicted values in a CSV format for submission.

## File Structure

```
project/
├── data/
│   ├── train.csv  # First submission file
│   ├── test.csv  # Second submission file
├── final_ML_project_team_14.ipynb # Main notebook
├── requirements.txt       # Project dependencies
├── submission.csv         # Final output file
└── README.md              # Project documentation
```

## Requirements

To run this project, you need the following dependencies:

- Python 3.7+
- pandas
- numpy
- scipy
- lightgbm
- xgboost
- catboost

Install the required packages using:

```bash
pip install -r requirements.txt
```

## Usage

1. **Prepare Data**:

2. **Run the Notebook**:
   - Open and execute the `final_ML_project_team_14.ipynb` notebook.

3. **Generate Final Submission**:
   - The processed submission file will be saved as `submission.csv`.

### Command-Line Execution

Alternatively, use the scripts for specific tasks:

- Train and predict with ensemble:

- Perform post-processing:

## Contributing

Lê Ngọc Minh Châu	21020174
Hà Quang Nhuệ	21021524
Trần Lê Thành Trung	21020671

## License

This project is licensed under the MIT License. See the LICENSE file for details.

