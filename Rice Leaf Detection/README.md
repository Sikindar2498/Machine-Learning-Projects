# Rice-Disease

## Domain Analysis
This dataset contains 120 jpg images of disease-infected rice leaves.It is a multi class classification task. The images are grouped into 3 classes based on the type of disease. There are 40 images in each class. Classes ● Leaf smut ● Brown spot ● Bacterial leaf blight

Classes

1.Leaf smut :-It is caused by the Gram-negative bacterium Xanthomonas oryzae pv.It causes wilting of seedlings and yellowing and drying of leaves.

2.Brown spot :- Brown spot is a fungal disease that infects the coleoptile, leaves, leaf sheath, panicle branches, glumes, and spikelets. Its most observable damage is the numerous big spots on the leaves which can kill the whole leaf. 

3.Bacterial leaf blight :- Leaf smut, caused by the fungus Entyloma oryzae, is a widely distributed, but somewhat minor, disease of rice. The fungus produces slightly raised, angular, black spots (sori) on both sides of the leaves 

## Pre-Proccessing steps:

Splitting the  Data

Training: Dataset to be used while training.

Validation: Dataset to be tested against while training.

Test: Dataset to be tested against after we trained a model.   

Prefetching solves the inefficiencies from naive approach as it aims to overlap the preprocessing and model execution of the training step. In other words, when the model is executing training step n, the input pipeline will be reading the data for step n+1.


Data augmentation in data analysis are techniques used to increase the amount of data by adding slightly modified copies of already existing data or newly created synthetic data from existing data. It acts as a regularizer and helps reduce overfitting when training a machine learning model.

FINAL CONCLUSION *

CNN (Baseline Model) Before Hyperparameter Tuning: Validation Loss: 1.4186 AND Validation Accuracy: 78.26%
After Hyperparameter Tuning: Validation Loss: 0.8586 AND Validation Accuracy: 65.22%

OBSERVATION : After hyperparameter tuning, the loss improved (lowered), but the accuracy dropped significantly. This suggests the model might have overfit or found a suboptimal point in the loss landscape.

2.VGG16 (Pretrained Model)

Validation Loss: 1.0361

Validation Accuracy: 82.61%

OBSERVATION : VGG16 outperformed the CNN model in terms of accuracy while maintaining a relatively lower loss. It seems to generalize well for my dataset. This is expected because VGG16 benefits from pretrained weights and a deeper architecture designed for robust feature extraction.

3.EfficientNet

Validation Loss: 1.0985

Validation Accuracy: 34.78%

OBSERVATION :

The low accuracy suggests that EfficientNet is struggling to learn meaningful patterns on my dataset. or a mismatch between the dataset size and EfficientNet's requirements. EfficientNet is powerful but often requires more data and careful fine-tuning.

RECOMMENDATION :
Based on these results:

VGG16 is the most recommendable model because it has the highest validation accuracy (82.61%) and a reasonable loss. It leverages the strength of transfer learning effectively.

CNN (Original) could also be considered if I want a simpler model, though it performs slightly worse than VGG16.

EfficientNet might not be suitable unless If i can improve its performance with additional tuning or a larger dataset.






