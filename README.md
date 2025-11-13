
# Titanic Survival Prediction

Machine learning model to predict passenger survival on the Titanic using Random Forest and other classification algorithms.

## 📊 Dataset

- **Source**: [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic)
- **Training samples**: 891 passengers
- **Test samples**: 418 passengers

## 🎯 Features

- **Original features**: Pclass, Sex, Age, SibSp, Parch, Fare, Embarked
- **Engineered features**:
  - `FamilySize`: Total family members aboard (SibSp + Parch + 1)
  - `IsAlone`: Binary indicator for solo travelers
  - `Title`: Extracted from passenger names (Mr, Mrs, Miss, Master, Rare)

## 🛠️ Data Preprocessing

1. **Missing Value Imputation**:
   - Age: Filled with median
   - Fare: Filled with median
   - Embarked: Filled with mode

2. **Feature Engineering**: Created FamilySize, IsAlone, and Title features

3. **Encoding**: One-hot encoding for categorical variables

## 🤖 Models

| Model | Cross-Validation Accuracy |
|-------|---------------------------|
| Random Forest | ~82% |
| Gradient Boosting | ~81% |
| Logistic Regression | ~80% |

## 📈 Results

- **Best Model**: Random Forest (n_estimators=200, max_depth=7)
- **Cross-Validation Score**: 0.82 ± 0.02
- **Kaggle Public Score**: ~0.77-0.78

## 🚀 Usage

```python
# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn

# Run the notebook
jupyter notebook Code.ipynb
```

## 📁 Project Structure

```
Titanic/
├── Clean_Code.ipynb              # Main analysis notebook
├── data/
│   ├── train.csv          # Training data
│   ├── test.csv           # Test data
│   └── gender_submission.csv    
└── README.md
```

## 🔧 Hyperparameter Tuning

Used RandomizedSearchCV to optimize:
- `n_estimators`: [200, 400, 600]
- `max_depth`: [5, 7, 10, None]
- `min_samples_split`: [2, 4, 6]
- `min_samples_leaf`: [1, 2, 3]
- `max_features`: ['sqrt', 0.5, 1.0]

## 📝 License

This project is open source and available under the MIT License.

## 👤 Author

**Achal Agarwal**
- GitHub: [@yourusername]((https://github.com/achalagarwal2004))
- Kaggle: [Your Kaggle Profile](https://www.kaggle.com/achalagarwal04)
=======
# Titanic-Machine-Learning-Kaggle
This project is a solution to the famous Titanic survival prediction challenge from Kaggle. The goal is to predict whether a passenger survived or not based on features such as age, gender, passenger class, and other attributes.
