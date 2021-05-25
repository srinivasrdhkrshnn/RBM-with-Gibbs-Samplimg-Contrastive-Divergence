# CS6910-Assignment-4: Contrastive Divergence Algorithm

### Steps to run the program
- The code is done in a Google colab notebook. It can be opened and run in Google colab or jupyter notebook.
- Block Gibbs Sampling Assignment 4.ipynb has solutions for questions 1, 2, 3.
- Contrastive Divergence Assignment 4.ipynb has solutions for questions 4, 5, 6 and 7.
- Change
- Run the whole notebook to get the outputs for all questions.
- The sweep for hyperparameter sweeps is commented out by default. Uncomment the cell to run the sweep across the given dictionary

## Block Gibbs Sampling Assignment 4.ipynb
Run all the cells except the last one. 
To train a model, edit the following values in the last cell (values for best  model are already given)

```python
rbm_epochs = 5              
classifier_epochs = 1         
k = 300
n_hidden = 128
r = 5
learning_rate = 0.01

``` 

  where :
  ```
  rbm_epochs -- (int) Number of RBM training epochs
  classifier_epochs -- (int) Number of classifier network training epochs
  k -- (int) Number of steps for which you will run the Markov chain
  n_hidden -- (int) Dimension of hidden layer
  r -- (int) Number of samples drawn after the chain converges
  learning_rate -- (float) Learning Rate
  ```

Then, run the last cell

The resulting model will be stored in rbm_parameters and classifier_param.

To train a custom model, run

```python
rbm_parameters,classifier_param = rbm_classifier(X_train,Y_train,X_val,Y_val,X_test,Y_test,rbm_epochs,classifier_epochs,k,r,n_hidden,learning_rate)
``` 

  where :
  ```
  X_train,Y_train -- Training Input and Output Data
  X_val,Y_val -- Validation Input and Output Data
  X_test,Y_test -- Test Input and Output Data
  rbm_epochs -- (int) Number of RBM training epochs
  classifier_epochs -- (int) Number of classifier network training epochs
  k -- (int) Number of steps for which you will run the Markov chain
  n_hidden -- (int) Dimension of hidden layer
  r -- (int) Number of samples drawn after the chain converges
  learning_rate -- (float) Learning Rate
  ```


To run a sweep, run

```python
sweeper(sweep_config,PROJECT_NAME)
```

where :
  ```
  sweep_config -- (dict) wandb sweep config dictionary
  PROJECT_NAME -- (string) wandb project name
  
  ```

  
## Contrastive Divergence Assignment 4.ipynb
Run all the cells until "Training over best model. 
To train a model, edit the following values in the last cell (values for best  model are already given)

```python
rbm_epochs = 20
classifier_epochs = 1
k = 2
n_hidden = 256
learning_rate = 0.001

``` 

  where :
  ```
  rbm_epochs -- (int) Number of RBM training epochs
  classifier_epochs -- (int) Number of classifier network training epochs
  k -- (int) Number of steps for which you will run the Markov chain
  n_hidden -- (int) Dimension of hidden layer
  learning_rate -- (float) Learning Rate
  ```

Then, run the last cell

The resulting model will be stored in rbm_parameters and classifier_param.

To train a custom model, run

```python
rbm_parameters,classifier_param = rbm_classifier(X_train,Y_train,X_val,Y_val,X_test,Y_test,rbm_epochs,classifier_epochs,k,n_hidden,learning_rate)
``` 

  where :
  ```
  X_train,Y_train -- Training Input and Output Data
  X_val,Y_val -- Validation Input and Output Data
  X_test,Y_test -- Test Input and Output Data
  rbm_epochs -- (int) Number of RBM training epochs
  classifier_epochs -- (int) Number of classifier network training epochs
  k -- (int) Number of steps for which you will run the Markov chain
  n_hidden -- (int) Dimension of hidden layer
  learning_rate -- (float) Learning Rate
  ```


To run a sweep, run

```python
sweeper(sweep_config,PROJECT_NAME)
```

where :
  ```
  sweep_config -- (dict) wandb sweep config dictionary
  PROJECT_NAME -- (string) wandb project name
  
  ```

For the remaining visualisation questions, run the remaining cells

Link for WandB report: https://wandb.ai/cs6910krsrd/CS6910%20ASSIGNMENT%204/reports/CS6910-Assignment-4---Vmlldzo3MTY5NTY

Link for Contrastive Divergence Assignment 4.ipynb Colab NB : https://colab.research.google.com/drive/14VbiJQE42JL9ChvGpXHBoz6VIJxeMhmi?usp=sharing

Link for Block Gibbs Sampling Assignment 4.ipynb Colab NB : https://colab.research.google.com/drive/1i7kzVAFaCLjMMEvdWiSAK_Md00EndrdB?usp=sharing
