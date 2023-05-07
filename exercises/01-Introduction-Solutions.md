# 01 introduction

1. **Where do you face Machine Learning?** <br>
   Currently we face machine learning almost in every field. It's widely used in medical field, tech industry, corporate companies, entertainment. One can find mostly find it in classification problems *e.g.* fraud detection in banks, helping to diagnose deseases in medical care, removing men from the loop in repetitive tasks and many more.
   In the recent time, the level of interaction with the machines has also tremendous improvement. ChatGTP lets us to intearct with it as if it was an actual human-being.
   
2. **What is Machine Learning?** <br>
   Kurzgesagt machine learning is the process of learning from available data in order to solve a specific task.

3. **What is training data?** <br>
   Experience, the whole exposed data during the training phase is called training data.

4. **What is training set?** <br>
   Examples that a system uses to learn are called training set.

5. **How do we measure performance?** <br>
   After training the model, one measures the performance by running the model through the test dataset. This will indicate how well the model perfoms when encountered with the unseen data.
   Cost function measures the distance between the linear model's predictions and the training examples; the objective is to minimize the distance.
   
6. **Why is it beneficial to use ML?** <br>
   It can generalize problems which would normally require implementation of tiny bit details with excessive maintanence and also can detect uncovered patterns within the dataset which would increase the performance and decrease the error rate of the work that would have been done in other way.
   
8. **What does data mining mean?** <br>
   Data mining is term used for the process of information generation out of vast unlabeled data. This process involves data preparation, statistical methods and ML too.
   
9. **What type of Machine Learning systems can you classify?** <br>
- Supervised Learning
- Unsupervised Learning
- Semi-supervised Learning
- Reinforcement Learning
- Transfer Learning
- Diffusion model
- GANs
- ...
   
10. **Describe 4 major categories shortly and point out the most important algorithms.** <br>
Look at above. These categories include algorithms like:
- K-means
- Regression
- Super Vector Machines
- DBSCAN
- Hierarchical Cluster Analysis
- ...    

11. **What is batch vs. online learning?** <br>
- Batch Learning: Name for model training using chunks of available data.
   1. Model is trained
   2. Deployed to PROD
   3. Runs without learning additional content
- Online Learning: Model gets incrementally trained by individual samples or mini-batches. It can be used for training systems on huge datasets that cannot fit in one machine’s main memory (**out-of-core** learning).
The algorithm loads part of the data, runs a training step on that data, and repeats the process until it has run on all of the data.
- Learning Rate: How fast a model adapts to changing data.

12. **What is instance-based vs. model-based learning?** <br>
They are two main generalization approaches.
- Instance-based: Works by comparing instances
- Model-based: Works by comparing the position with the known data borders.

13. **What are common problems with Machine Learning algorithms and datasets?** <br>
- Model:
   - Overfitting, underfitting
- Data:
   - Garbage-in garbage-out
   - Nonrepresentative data
   - Unreasonable effectiveness of data
   - Irrelevant features (noise)
   - Data mismatch    

14. **How to do testing & validation?** <br>
- Split available data into training & test sets.
- The error rate in the new cases is called -> generalization error (out-of-sample error)
- If the training error is low, the generalization error is high there is overfitting.

15. **What does "No free lunch theorem" state?** <br>
    "If you make absolutely no assumption about the data, then there is no reason to prefer one model over any other."