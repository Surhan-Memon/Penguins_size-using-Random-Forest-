# Penguins_size-using-Random-Forest-
Penguin Species Classifier — Random Forest
Predicts the species of a penguin (Adelie, Chinstrap, or Gentoo) from physical measurements using a Random Forest classifier. Achieves 97% accuracy on test data.

Dataset
penguins_size.csv — Palmer Penguins dataset with the following columns:

species — target label (Adelie / Chinstrap / Gentoo)
island — island where penguin was observed
culmen_length_mm — bill length
culmen_depth_mm — bill depth
flipper_length_mm — flipper length
body_mass_g — body mass
sex — gender

Missing values are dropped before training.

How It Works
Preprocessing — categorical columns (island, sex) are one-hot encoded using get_dummies. 70/30 train-test split.
Model — RandomForestClassifier with 10 trees and max_features='sqrt'. Straightforward setup, no hyperparameter tuning needed to get strong results on this dataset.
Evaluation — confusion matrix and full classification report. Feature importances extracted directly from the trained forest.

Results
SpeciesPrecisionRecallF1Adelie0.970.950.96Chinstrap0.920.960.94Gentoo1.001.001.00
Overall accuracy: 97% on 101 test samples.
Gentoo penguins are perfectly classified — their physical profile is distinct enough that the model never misses one.

Feature Importances
The most influential features ranked by importance:

culmen_length_mm — 31.9%
body_mass_g — 21.3%
flipper_length_mm — 17.3%
culmen_depth_mm — 10.2%

Bill length alone carries nearly a third of the predictive weight.

Stack
Python · pandas · scikit-learn · matplotlib · seaborn
