# Text Classification using Natural Language Processing (NLP)

Text classification is a process of assigning tags/categories to documents, which helps us to structure and analyze text in an automatic, fast and cost effective way.
The aim in this project is to classify the product category based on product descriptions using Natural Language Processing (NLP) algorithm.

## The workflow in this project is as below:
### Load and Clean the Data
Of the total 50,425 data almost half are duplicates, but we still have enough data that can be used to train the model. 
A total of 27,803 data are pre-processed before being used to train the model. 

### Text Pre-processing
It is important to pre-process text to make it easier for the model to properly understand the patterns contained in the data, some of the things that need to be done at this point are:
- Case Folding, change the text to lowercase.
- Remove punctuation from the text.
- Remove stop-words, such as ‘i’,’you’,’a’,’the’,’he’,’which’, etc.
- Tokenizing, the process of dividing text into smaller parts called tokens.
- Sequence and Padding, represent each sentence with a sequence of numbers, then we pad the sequences so that we can have the same length for each sequence.

### Modeling
The model use the Biddirectional LSTM, consists of two dense layer with 'ReLU' activation function followed by a dropout layer to avoid overfitting and a final output layer with 'Softmax' activation function. 
And then in the process of compiling the model we use 'Adam' optimizer and 'Binary Crossentropy' for the loss function.

**Results:**

![accuracy](https://github.com/user-attachments/assets/08aa27a9-3c66-40b7-b445-65976bea007e)
![loss](https://github.com/user-attachments/assets/f4e0d179-f78f-4caa-b753-fc5fe7792e8f)

The performance of the model was quite good with 93% accuracy.
