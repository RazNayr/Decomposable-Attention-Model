# Applying Recurrent Layers to the Decomposable Attention Model for Natural Language Inference

The aim of this project is to investigate whether adding recurrent components to the decomposable attention model (DAM) [1] could enhance the performance of the overall network. Additionally, the proposed enhancements will be strict in maintaining a lower amount of trainable parameters than those required for other RNN models, so as to determine if an increase in performance could be achieved with minimal increase in parameters.

Note:
> To run the project, make sure you view INSTRUCTIONS for installing the necessary packages. * </br> To fully understand the project scope and see results, please read the pdf present in the repo. *

</br>
</br>

## Models

This project extends Parikh et al.'s Decomposable Attention Model (DAM) [1] by adding reccurent components to the original.
The following models were defined:

1. DAM
2. DAM-INTRA (DAM with intra-sentence attention)
3. DAM-BiLSTM (DAM with bilateral LSTM)
4. DAM-BiGRU (DAM with bilateral GRU)


</br>
</br>

## Directories
#### _1. dataset_
* Stores SNLI zipped folder.
* Stores SNLI unzipped train, validation and test sets.
* Populated when running dataset-utils.ipynb.


#### _2. model-representations_
* Stores the visualised architectures of each model.


#### _3. saved-models_
* Contains hdf5 files representing the best weights obtained when training the models.
* These files are overriden when running model-trainer.ipynb and used when running model-evaluator.ipynb.

</br>
</br>

## Notebooks

#### _1. data-visualizer.ipynb_
* Notebook used to observe the distribution of the SNLI dataset.
* This is also used to explain decisions taken throughout the project, such as choosing the maximum sequence lengths.


#### _2. data-utils.ipynb_
* Used to retrieve the SNLI dataset and unzip the necessary train, validation and test files.


#### _3. model-evaluator.ipynb_
* Used to evaluate the models saved in the saved-models directory.
* Quantitative Evaluation
  - Classification Report
  - Confusion Matrix
  - ROC Curve
  - Precision-Recall Curve

* Qualitative Evaluation
  - Observation of Incorrect Predictions
  - Custom Input Predictions

#### _4. model-trainer.ipynb_
* Used to train the models and display their architecture.
* Display accuracy against loss for training and validation sets after training. 

</br>
</br>

## References
[1] A. P. Parikh, O. Tackstr ¨ om, D. Das, and J. Uszkoreit, “A Decomposable Attention Model for Natural Language Inference,” ¨
arXiv:1606.01933 [cs], June 2016. arXiv: 1606.01933 version: 1.
