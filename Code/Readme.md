# Text Classification

This project required a blend of data preprocessing, advanced neural network architectures, and meticulous model evaluation. Here's a glimpse into my journey and the methodologies I employed.

## Data Preparation

The initial phase involved gathering data from various sources, ensuring a rich dataset that captures the nuances of human and AI-generated text. I meticulously cleaned and preprocessed the data, focusing on normalizing text and removing unnecessary characters to maintain consistency across the dataset. This preparation was crucial for the model to learn effectively from the text.

## Feature Engineering with TextVectorization

Understanding the importance of transforming text into a format understandable by neural networks, I utilized TensorFlow's `TextVectorization` layer. This powerful layer allowed me to standardize the text, tokenize it, and convert it into numerical data. I tailored the text standardization process to our specific needs, ensuring every word contributed meaningfully to the model's learning process.

## Crafting the Model

Drawing from the latest advancements in NLP, I designed a neural network that combines the strengths of multiple architectures:

- **Embedding Layer**: This layer was the foundation, converting tokens into dense vectors of fixed size, capturing the semantic meaning of words.
- **Bidirectional LSTM**: I integrated LSTM to capture both past and future context, a crucial feature for understanding the flow of language in essays.
- **Transformer Block**: Inspired by the Transformer model's success, I incorporated a custom Transformer block to leverage self-attention mechanisms, enabling the model to weigh the importance of different words in the text.
- **Conv1D and Pooling**: To capture local patterns and reduce dimensionality, I added a Conv1D layer followed by GlobalMaxPooling1D, streamlining the model's input for the final classification layers.

## Model Training and Evaluation

Training the model was an iterative process, where I utilized callbacks like `ModelCheckpoint` and `EarlyStopping` to fine-tune performance and prevent overfitting. After training, I evaluated the model's accuracy and precision through a test set, employing a confusion matrix and classification report to dissect the model's strengths and weaknesses.

