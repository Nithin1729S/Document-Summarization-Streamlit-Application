# Document-Summarization
Document Summarization App using large language model (LLM) and Langchain framework. Used a pre-trained T5 model and its tokenizer from Hugging Face Transformers library. 
Created a summarization pipeline to generate summary using model.

## Demo



https://github.com/Nithin1729S/Document-Summarization-Streamlit-Application/assets/78496667/6ebbcd0a-2730-45ec-95f2-0483e0260dc1




[Watch the Demo Video on YouTube](https://youtu.be/GOR-pIVZ04w)

## Screenshots
![Screenshot from 2024-07-04 02-29-14](https://github.com/Nithin1729S/Document-Summarization-Streamlit-Application/assets/78496667/619b8fdc-c40c-4526-889a-2087349891f6)

![Screenshot from 2024-07-04 02-29-01](https://github.com/Nithin1729S/Document-Summarization-Streamlit-Application/assets/78496667/ff6ce5f2-c117-40bd-8c56-dcf912bbfbde)

## Overview
1. Import Statements:
   - It begins by importing necessary libraries like Streamlit, Langchain, Transformers, and other Python libraries.

2. Model and Tokenizer Loading:
   - The code loads a pre-trained T5 model (a Transformer-based model) and its associated tokenizer from the Hugging Face Transformers library.
     This model is used for text summarization.
   - Model Used ![MBZUAI/LaMini-Flan-T5-248M](https://huggingface.co/MBZUAI/LaMini-Flan-T5-248M) 

3. File Loader and Preprocessing:
   - The `file_preprocessing` function loads a PDF file using the Langchain library and splits it into smaller text chunks. These text chunks are later used for
     summarization.

4. LLM Pipeline:
   - The `llm_pipeline` function sets up a summarization pipeline using the pre-trained T5 model and tokenizer. It takes the preprocessed text as input and generates
     a summary using the model.

5. Streamlit Setup:
   - The Streamlit app is set up with a title and an option to upload a PDF file.

6. Main Function:
   - The `main` function is the entry point of the app.
   - It provides a file upload button and a "Summarize" button.
   - When a PDF file is uploaded and the "Summarize" button is clicked, it displays the uploaded PDF on the left side and the generated summary on the right side
     of the Streamlit app.

7. HTML Display of PDF:
   - The `displayPDF` function converts the uploaded PDF file into base64 format and embeds it in an HTML iframe, allowing the PDF to be displayed in the app.

8. Streamlit Configuration:
   - The app's layout is configured to be "wide" using `st.set_page_config`.

9. Running the App:
   - Download the model from here https://huggingface.co/MBZUAI/LaMini-Flan-T5-248M/tree/main and save it in a folder named model
   - The model couldn't be uploaded here due to its huge size.
   - The app is launched when the script is run as the main module (`if __name__ == "__main__": main()`).

The main functionality of this app is to upload a PDF document, process it, and then display both the PDF and a summarized version of the document.
It utilizes a pre-trained language model for text summarization and Streamlit for creating a user-friendly interface. Users can upload PDFs and quickly obtain 
summarized content from them.


## Setup and Installation

1. **Clone the Repository**:
    ```bash
    https://github.com/Nithin1729S/Document-Summarization-Streamlit-Application.git
    cd Document-Summarization-Streamlit-Application
    ```

2. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up Model**:
    - Download the model ![MBZUAI/LaMini-Flan-T5-248M](https://huggingface.co/MBZUAI/LaMini-Flan-T5-248M) from huggingface and move the models contents to a folder named model in the root directory.
      
4. **Run application**:
    ```bash
    streamlit run main.py
    ```
