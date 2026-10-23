# Practice Activity 9-1: Regression Models and Pipelines

Completed **parts 11–14** of the supplied K-Nearest Neighbors and Decision Trees for Regression notebook. The notebook includes executed code, saved plots, model comparison tables, and written interpretations. Earlier instructional examples and discussion prompts are retained.

[**Open the completed notebook**](Practice_Activity_9_1_Regression_Models_and_Pipelines.ipynb)

The solutions predict `SalePrice` in dollars from `Gr Liv Area`, `Bedroom AbvGr`, `Full Bath`, `Half Bath`, and `Neighborhood`:

- **11:** Scaled numerical features and one-hot neighborhood indicators in a 10-nearest neighbors pipeline, with a predicted-versus-actual scatter plot.
- **12:** Comparison of seven values of k, with a written choice based on validation RMSE.
- **13:** A depth-4 regression tree pipeline, a full tree plot, an interpretation of its learned splits and leaf values, and a predicted-versus-actual scatter plot.
- **14:** Comparison of eight depth settings, an explanation of the selected depth, and final evaluation of the selected models on reserved test data.

A fixed 60%/20%/20% training/validation/test split keeps preprocessing and model selection separate from final testing. The best tested validation settings are **k=5** (RMSE **$38,522.68**) and **max_depth=10** (RMSE **$41,080.87**). These are comparisons on one split, not universal optimal settings.

## Run

The notebook renders directly on GitHub, including its saved results. To rerun locally, use Python 3.11 or newer from this directory:

```bash
python -m pip install -r requirements.txt
jupyter notebook Practice_Activity_9_1_Regression_Models_and_Pipelines.ipynb
```

Choose **Run All**. The two input datasets are included in `data/`; the notebook falls back to the original HTTPS dataset URLs when opened by itself in Colab. The depth-4 tree is also saved as a [larger image](artifacts/decision_tree_depth_4.png).

For command-line execution:

```bash
jupyter nbconvert --to notebook --execute --inplace Practice_Activity_9_1_Regression_Models_and_Pipelines.ipynb
```

The completed notebook was executed from a fresh kernel with Python 3.14.6, pandas 3.0.3, NumPy 2.4.6, scikit-learn 1.9.0, and Matplotlib 3.11.0. Exact tied-neighbor choices and resulting KNN scores can vary across library versions.

## Sources

The assignment and introductory notebook material come from the [provided Colab notebook](https://colab.research.google.com/drive/1uzExfeQSbLi_mHOs45u39039Ea0C-KRw). The included data are the same files referenced there: [Ames Housing](https://dlsun.github.io/pods/data/AmesHousing.txt) and [Bordeaux wines](https://dlsun.github.io/pods/data/bordeaux.csv). The requested solutions are in parts 11–14; the earlier sketch-and-discussion prompts remain as supplied.
