# 09 - Neural Networks

1. Describe the general architecture of a Wide&Deep model. What is the advantage of this architecture?
   - This method enables us to feed the simple features and deep aspects into the models last layer.
   - This way simple features won't be put in the background from models' perspective.
   - It is also very flexible architecture, we can feed in multiple inputs.

2. Let's assume we want to predict a property of an image. e calculate some features like sharpness, white portion and feed them as additional input besides the image pixels. What type of architecture would you recommend?
   - A wide&deep model with multiple inputs. That way we would also put an emphasis on the respective features while training the model and it would pay more attention to these details.
   - Since we want to predict magnitude of a property it would be a better choice to use some different model than LogisticRegression.

3. How to avoid to adjust a model multiple times?
   - We can save models in HDF5 format and reuse them by loading it into a notebook.

4. How to avoid optimizing the number of epochs?
   - With callbacks we can also set a patience for model. This way it has a certain threshold for the number of next iterations if the model's performance does not improve and it breaks the training saving resource & time.

5. Ways to fine-tune hyperparameters of a neural networks automatically?

6. Why does it make sense to have multiple hidden layers, while NNs can still solve complex tasks with one layer?

7. What is the recommended alternative to gradually adjust the number of neurons to avoid overfitting?

8. Which hyperparameter is said to be the most important?

9. What are the benefits of large batch sizes and what needs to be considered?

10. How to find the best batch-size for a specific model?
