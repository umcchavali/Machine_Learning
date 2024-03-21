# Machine_Learning
A few projects including KNN, XGboost, etc

## Project Glass
KNN Classifier 
We have been provided with the "glass-2.csv" dataset, which contains information about various types of glass. Each row represents a different type of glass, and the columns represent different features of the glass samples. The last column denotes the type of glass, which is the target variable

### Data Preprocessing and tuning
1. Import dependencies
2. Load data
3. Check Correlation
4. Split dataset into test and train
5. Use the knn.fit and accuracy score to determine the model's accuracy.
### Tune the model to achieve an accuracy above 70% (No Overfitting)
Selecting the Optimal k Value:
The selection of the nearest neighbors k, is critical as it influences the balance between bias and variance in the model ( as we have seen in the bias variance trade-off). 

A smaller value of k results in a more complex decision boundary, which can lead to overfitting and increased sensitivity to noise in the data. 
(Vice Versa) A larger value of k results in a smoother decision boundary, potentially leading to underfitting and reduced model complexity.

To identify the optimal value of k that achieves a balance between bias and variance, grid search can be used over 10 different values of k. By plotting the cross-validation accuracy corresponding to each value of k, we want to determine the point at which the model demonstrates optimal performance. This process makes sure that overfitting is avoided by selecting a suitable k that generalizes well to unseen data while effectively capturing the underlying patterns in the training data.

### Grid Search
Grid search is used to automatically find the best combination of hyperparameters for the K-Nearest Neighbors classifier. It systematically evaluates different hyperparameter combinations using cross-validation to optimize the model's performance. This approach saves time and effort compared to manual tuning and helps prevent overfitting by testing the model on various subsets of the data. Ultimately, grid search aims to identify the hyperparameters that yield the highest accuracy on unseen data.
The plotted graph gives us more insight into what the use cases might look like. The visual is a great place to start for this model.

### Plot a cross validation accuracy for 10 values of k and provide inference.
Cross-validation accuracy is used to visualize how well our model performs with different values of k. 
By trying out various k values and observing the resulting accuracy scores, we can identify the optimal k that strikes a balance between bias and variance (again we are looking at the boas variance trade-off). This helps us avoid overfitting, where the model performs very well on the training data but poorly on unseen data.
We will select a k value that generalizes well to new, unseen data, ensuring our model is robust and reliable.

## Final Model
Achieved:
73% Test Accuracy
Inference: The plot shows the cross-validation accuracy for different values of k.
From the plot, we can observe that the highest accuracy is achieved when k is around 3 or 5.
As k increases, the accuracy decreases, indicating that a smaller value of k is preferred for this dataset.
