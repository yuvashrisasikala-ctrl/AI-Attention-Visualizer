# Attention-Mechanism-Visualizer

A beginner-friendly AI application that extracts text from study-note images using OCR, converts words into numerical embeddings, and visualizes attention scores using a simple scaled dot-product attention mechanism.

## Project Overview

This project combines OCR, sentence embeddings, attention mechanism, and Streamlit into one application.

A user uploads an image containing study notes. The application:

1. Extracts text from the image using Tesseract OCR.
2. Splits the extracted text into words.
3. Converts the words into numerical embeddings using Sentence Transformers.
4. Creates Query (Q), Key (K), and Value (V) representations.
5. Calculates scaled dot-product attention.
6. Displays attention scores using progress bars.
7. Identifies the word with the highest calculated attention score.

## Project Flow

Image → OCR → Extract Text → Word Processing → Embeddings → Q, K, V → Attention → Visualization

## Technologies Used

- Python
- Streamlit
- Tesseract OCR
- Pytesseract
- Sentence Transformers
- NumPy
- Pillow

## Project Structure

AI-Attention-Visualizer/
│
├── app.py
├── ocr.py
├── embedding.py
├── attention.py


## File Description

| File | Description |
|------|-------------|
| app.py | Main Streamlit application |
| ocr.py | Extracts text from images using Tesseract OCR |
| embedding.py | Generates text embeddings using Sentence Transformers |
| attention.py | Calculates Query, Key, Value and scaled dot-product attention | Contains the required Python packages |

## Features

- Upload JPG, JPEG, and PNG images
- Extract text from images using OCR
- Generate numerical embeddings
- Create Query, Key and Value representations
- Apply scaled dot-product attention
- Visualize word attention scores
- Identify the word with the highest calculated attention score
- Simple and beginner-friendly Streamlit interface

## Installation

### 1. Clone the Repository

git clone <your-github-repository-link>

cd AI-Attention-Visualizer

### 2. Install Required Packages

pip install -r requirements.txt

Or:

pip install streamlit numpy pillow pytesseract sentence-transformers

## Tesseract OCR Setup

Tesseract OCR must be installed separately on Windows.

The default path used in this project is:

C:\Program Files\Tesseract-OCR\tesseract.exe

If Tesseract is installed in another location, update the path in ocr.py.

## Run the Application

Open the project folder in VS Code and run:

python -m streamlit run app.py

For Windows:

py -m streamlit run app.py

The application will open in a web browser.

## Example

The application can process an image containing text such as:

Artificial Intelligence uses machine learning to analyze data.

The application extracts the text, processes the words, generates embeddings, calculates attention scores, and displays the scores using visual progress bars.

## How It Works

Image
  ↓
Tesseract OCR
  ↓
Extracted Text
  ↓
Word Processing
  ↓
Sentence Embeddings
  ↓
Query, Key, Value
  ↓
Scaled Dot-Product Attention
  ↓
Attention Scores
  ↓
Streamlit Visualization

## Attention Mechanism

The project demonstrates the basic idea of scaled dot-product attention.

The attention mechanism uses:

Q = Query
K = Key
V = Value

The basic formula is:

Attention(Q, K, V) = softmax(QKᵀ / √dₖ)V

where dₖ represents the dimension of the Key vectors.

The calculated attention values are used to visualize the relative attention scores for the processed words.

## Important Note

This project is an educational demonstration of the attention mechanism.

The Query, Key, and Value projection matrices are randomly initialized. Therefore, the highest-attention word should not be interpreted as the most important word in a semantic sense.

The project demonstrates the mechanics of applying attention to embeddings rather than reproducing the internal attention maps of a pretrained Transformer.

## Limitations

- OCR accuracy depends on image quality.
- Handwritten text may not be recognized accurately.
- Only the first 20 cleaned words are visualized.
- all-MiniLM-L6-v2 is mainly a sentence-embedding model but is applied to individual words for educational simplicity.
- The Q, K and V projection matrices are randomly initialized.
- The highest-attention word is not necessarily the most meaningful or important word.

## Future Enhancements

- Use a Transformer model with actual token-level attention weights
- Highlight important words in the extracted text
- Highlight words directly on the original image
- Add Tamil and other language support
- Add keyword extraction
- Add topic classification
- Add a study-notes summarizer
- Add question-answering functionality
- Allow users to download an attention report

## Work Pictures

<img width="1442" height="896" alt="1" src="https://github.com/user-attachments/assets/f3e27fd1-bfcf-4d49-adfb-ff5b7429ea44" />

<img width="1502" height="862" alt="2" src="https://github.com/user-attachments/assets/308aaae8-4d14-4766-8fea-6e629b8211eb" />

<img width="1482" height="862" alt="4" src="https://github.com/user-attachments/assets/225814ad-7a54-4c67-9f0d-30d9589db107" />

<img width="1406" height="847" alt="5" src="https://github.com/user-attachments/assets/a131023e-dde2-4c2f-82e9-ceaee744177b" />



## Learning Outcomes

Through this project, I learned:

- How OCR converts images into text
- How embeddings represent text as numerical vectors
- How Query, Key and Value work
- How scaled dot-product attention is calculated
- How attention weights can be visualized
- How Python modules can be connected together
- How to build and run a Streamlit AI application
- How different AI components can be combined into a single application

