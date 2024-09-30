# neural-network-challenge-2

1. Preprocessing the Data
Imported the dataset and selected relevant columns for X (input features) and y (target columns: Attrition and Department).
Used LabelEncoder and OneHotEncoder to convert categorical features like OverTime, Attrition, and Department into numerical representations.
Applied StandardScaler to scale the numerical features, ensuring uniform distribution for better model performance.
Split the data into training and testing sets.

2. Building the Model
Used Keras' Functional API to build a non-sequential neural network with shared layers and two branched outputs:
One branch predicts Department using softmax activation.
The other branch predicts Attrition using softmax activation.
Added two shared hidden layers to extract common features before branching.

3. Training the Model
Trained the model for 10 epochs using the adam optimizer and categorical crossentropy loss function for both branches.
Achieved reasonable accuracy for both branches during the training process.

4. Evaluating the Model
Evaluated the model on the testing data.
Final results:
Department accuracy: 87.8%
Attrition accuracy: 64.6%

Key Concepts:

Branching Neural Networks: A neural network model with shared layers that branches into multiple outputs, each responsible for predicting a different target.
Data Preprocessing: Includes encoding categorical variables, scaling features, and splitting data into training and testing sets.
Multi-task Learning: Solving two prediction tasks (attrition and department) in a single model using shared representations.
Future Improvements:

Experimenting with hyperparameters like learning rate and batch size.
Using class weights or data augmentation to balance the dataset if needed.
Considering additional metrics like precision, recall, and F1-score, especially for imbalanced target classes like attrition.

