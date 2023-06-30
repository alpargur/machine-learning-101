# 09 - Neural Networks

1. Describe the general architecture of a Wide&Deep model. What is the advantage of this architecture?
   - This method enables us to feed the simple features and deep aspects into the models last layer.
   - This way simple features won't be put in the background from models' perspective.
   - It is also very flexible architecture, we can feed in multiple inputs.

2. Let's assume we want to predict a property of an image. e calculate some features like sharpness, white portion and feed them as additional input besides the image pixels. What type of architecture would you recommend?
   - A wide&deep model with multiple inputs. That way we would also put an emphasis on the respective features while training the model and it would pay more attention to these details.
   - Since we want to predict magnitude of a property it would be a better choice to use some different model than LogisticRegression.

3. How to avoid to adjust a model multiple times?
- Callback, early-stopping

4. How to avoid optimizing the number of epochs?
   - With callbacks we can also set a patience for model. This way it has a certain threshold for the number of next iterations if the model's performance does not improve and it breaks the training saving resource & time (early-stopping)

## Fine-tuning
1. Ways to fine-tune hyperparameters of a neural networks automatically?
   - `RandomizedSearchCV` & `GridSearchCV` can be used by wrapping a keras model in a **scikeras.wrappers** `KerasRegressor`

2. Why does it make sense to have multiple hidden layers, while NNs can still solve complex tasks with one layer?
   - Deep networks have higher parameter efficiency and they yield better results when using the same amount of data.

3. How can the layers be interpreted?
   - Lower layers learn structurally fundamental more basic stuff (lines, shapes etc)
   - Higher layers learn more complex / high-level of structures (cube or pyramid)

4. What is transfer learning? Why is it useful?
   - Transfer learning is basically using a pre-trained model (except output layer) and train it for a similar task. It is faster than training from scratch and effective, yet doesn't make sense for small problems.

6. What is a good distribution of number of neurons across the different hidden layers?
   - Pyramid structure said to be a good strategy, nowadays having the same number of neurons across hidden layers is a preferred as well.

7. What is the recommended alternative to gradually adjust the number of neurons to avoid overfitting?
   - You can use more layers and do earlystopping to avoid overfitting.
  
8. Which hyperparameter is said to be the most important?
   - Optimal learning rate is half of the max learning rate sometimes
   - A simple approach for tuning the learning rate is to start with a large value that
   makes the training algorithm diverge, then divide this value by 3 and try again,
   and repeat until the training algorithm stops diverging. At that point, you gener‐
   ally won’t be too far from the optimal learning rate. That said, it is sometimes
   useful to reduce the learning rate during training: 
   
9. What are the benefits of large batch sizes and what needs to be considered?
   - A small batch size ensures that each training iteration is very fast, and although a large batch size will give a more precise estimate of the gradients, in practice this does not matter much since the optimization landscape is quite complex and the direction of the true gradients do not point precisely in the direction of the optimum. However, having a batch size greater than 10 helps take advantage of hardware and software optimizations, in particular for matrix multiplications, so it will speed up training. Moreover, if you use Batch Normalization (see Chapter 11), the batch size should not be too small (in general no less than 20).

10. How to find the best batch-size for a specific model?
    - Start with a large batch-size and warm-up learning rate, if the model is unstable then try training again with a smaller batch-size.
