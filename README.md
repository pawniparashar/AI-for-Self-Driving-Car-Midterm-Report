# AI-for-Self-Driving-Car-Midterm-Report
### Midterm Submission for the WiDS 2025 project "AI for Self-Driving Car: Build a Traffic Sign Classifier".
**AIM: To build a ML Model that can recognise 43 German traffic signs irrespective of their condition.**

The purpose of this project primarily roots at the challenge that while humans instinctively recognise traffic signals, a computer analyses graphics as a complex grid of numerical pixel values and even minor discrepancies such as poor lighting, weather conditions, or motion blur, can lead to misclassification, which poses a significant safety risk.

To address this challenge we are building a **Traffic Sign Classifier** by using **Machine Learning** and **Deep Learning**. Instead of manually coding rules for every possible sign, we are training a **Convolutional Neural Network (CNN)** to recognize patterns independently based on the dataset.

***Week 1***

_Building the foundation_

In the first week I learnt the fundamentals of Python including variables and datatype, strings, lists and tuples, dictionaries and sets, conditional expressions, loops, functions and recursion. To reinforce the concept I practiced some problems based on them. Additionally, I gained a basic idea of machine learning for the project. The main purpose of this week was to strengthen my command over python syntax for ease in coding and gain a foundational understanding of Machine Learning.

***Week 2***

_Diving deep into ML concepts and Pandas_

Week 2 was dedicated to the mathematical foundations of machine learning, focusing on Linear Regression. This involved understanding how models establish relationships between variables by fitting a straight line to data points. To better understand this we used an example of predicting the price of a house based on its size. 

A major part of the work involved the Cost Function, which serves as a tool to evaluate accuracy by measuring the gap between predictions and actual data. Learning to calculate averaged squared error was essential to see how a model quantifies its own inaccuracies.

The process of model optimization was explored through Gradient Descent. This algorithm functions by iteratively adjusting parameters to minimize the cost function, until the algorithm converges, meaning the cost no longer decreases significantly and the parameters stabilize near a minimum.

Alongside the theory, I spent time learning and practicing with the Pandas library to handle and analyze data efficiently.

***Week 3***

_Neural Networks > Linear Regression_

Week 3 focused on moving from basic math to more powerful AI models. It started with Linear Regression, which works well for simple, straight-line predictions like house prices. However, when tested on curvy or complex data, this method failed because a straight line cannot adapt to complex shapes, a problem called underfitting.

To fix this, a Neural Network was built using Keras. By adding hidden layers and "neurons," the model gained the flexibility to bend and match complex patterns. This is the foundation for the traffic sign project: while a straight line can't recognize a sign, a neural network can be molded to understand the complex shapes and edges of road signals.

Based on Neural Networks, Assignment 1 was on predicting vehicle fuel efficiency.

***Week 4***

_Understading CNN and Evaluation Metrics_

Week 4 focused on the transition to Convolutional Neural Networks (CNNs) and the logic behind measuring model performance. CNNs are specialized for image tasks because they use filters to scan for spatial patterns like edges and shapes, which is essential for identifying traffic signs. The addition of pooling layers was also explored as a way to simplify data while keeping the most important visual features

A significant part of the work involved a deep dive into Evaluation Metrics to determine if a model is truly effective. For regression tasks, MAE, RMSE, etc. were used to quantify the error margin between predictions and actual values.

For classification, we moved to the Confusion Matrix, which tracks exactly where a model succeeds or fails. This included learning about Precision (reliability of positive hits), Recall (ability to find all targets), and the F1-Score, which provides a balanced view of both. These metrics ensure the classifier is reliable enough for real-world driving scenarios.

Assignment 2 was focused on how CNN is an upgrade over ANN by comparing both their precisions.

***Week 5***

_Implementation and Pipeline Development_

The final phase of the midterm focused on building the end-to-end Traffic Sign Classifier using the GTSRB dataset. This involved writing a functional pipeline in Python to load, preprocess, and train a deep learning model.Key Implementation Details:Data Processing: Images were loaded, resized to $30 \times 30$, and converted into NumPy arrays. The data was then normalized to a range of $[0, 1]$ and labels were one-hot encoded for the 43 sign categories.CNN Architecture: A Sequential model was developed using convolutional layers for feature extraction, MaxPooling to reduce dimensionality, and Dropout to prevent overfitting.Training & Evaluation: The model was compiled with the Adam optimizer and trained using categorical cross-entropy. Performance was monitored via accuracy and loss curves to ensure the model generalized well to the test set.
