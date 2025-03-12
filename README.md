# Simple-Transformer-Translation-Model-LLM

This project demonstrates a basic Transformer model for translation tasks. It uses a small dummy dataset to build, train, and save a translation model. The model includes both encoder and decoder parts along with positional encoding.

**What It Does**

**Builds a Vocabulary:**

The code creates simple vocabularies for source and target languages from a list of sentences.

**Tokenizes Sentences:**
It converts sentences into lists of token IDs, adding special tokens for start-of-sentence (<sos>), end-of-sentence (<eos>), unknown words (<unk>), and padding (<pad>).

**Creates a Custom Dataset:**

A custom dataset class is defined to provide tokenized source-target sentence pairs for training.

**Defines the Transformer Model:**

The model consists of:

Positional Encoding: Adds order information to token embeddings.
Encoder Layers: Use multi-head attention and feed-forward networks to process the source sentence.
Decoder Layers: Use masked self-attention and encoder-decoder attention to generate the target sentence.
Final Output Layer: Maps decoder outputs to target vocabulary logits.
Trains the Model:
A training loop runs the model over the dummy dataset using teacher forcing. It computes the loss (ignoring padding tokens) and updates the model using the Adam optimizer.

**Saves the Model:**

After training, the model is saved to a file (transformer_translation.pth).

**How to Run**
Install Dependencies:
Make sure you have PyTorch installed. You can install it via pip if needed:

bash
Copy
pip install torch
Run the Code:
Save the code to a Python file (for example, transformer_translation.py) and run:

bash
Copy
python transformer_translation.py
The training process will print loss values during training, and the trained model will be saved.
