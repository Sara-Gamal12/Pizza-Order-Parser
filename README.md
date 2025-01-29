# Pizza-Order-Parser
<img src="https://gifdb.com/images/high/cool-cartoon-pizza-edln331mt37gmdoy.gif" height="500px"/>

## 📝Table of Contents
- <a href ="#Overview">Overview</a>
- <a href ="#started"> Get Started</a>
- <a href ="#modules"> Modules</a>
  - <a href ="#preprocessing">Preprocessing</a>
  - <a href ="#Architecture">Architecture</a>
- <a href ="#contributors">Contributors</a>

## 🔍Overview<a id="Overview">
 The goal of this project is to develop sequence models that can accurately identify key
 items in complex food ordering requests, focusing specifically on pizza customization.
 By organizing natural language into actionable data, this project tackles real-world NLP
 challenges where specialized entities (such as "toppings," "pizza sizes," and "crust
 types") require precise extraction. This enables a more robust fulfillment of orders in
 online food applications

## 💻Get Started<a id="started">

### Prerequisites
- Ensure you have **Python 3.8+** installed. Download it from [python.org](https://www.python.org/downloads/).
- Install Jupyter Notebook if you haven't already:
  ```sh
  pip install notebookV
  ```
### 1. Clone the repository:
``` bash
git clone https://github.com/Sara-Gamal12/Pizza-Order-Parser
```
### 2. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate     # On Windows

```
### 3. Install dependencies:

```bash
pip install --upgrade tensorflow pandas numpy
```
 ### 4. Run Jupyter Notebook:
```sh
    jupyter notebook
```
 ### 5. Open nlp-demo.ipynb and execute the cells in order to see the output.
  you can change the written order to any other order


## 🧱Modules<a id="modules">

### 🛠️ Preprocessing and Feature Extraction <a id="preprocessing">
1. Cosine Similarity with Sentence Embeddings:
    Compute sentence embeddings for each sentence.
    Add a sentence to the training set only if its cosine similarity with all previously added sentences is below a defined threshold, ensuring uniqueness.
2. UNK Augmentation:
    Randomly introduce "UNK" tokens at various positions in sentences.
    This encourages the model to better handle unseen words during training.
3. Synonym Replacement:
    With a certain probability, replace words with their synonyms to help the model generalize and understand various word forms.
4. Unique Words and Tags Selection:
    Identify and select distinct words and associated tags for the training data.
5. BIO Tagging Format:
 Use the BIO tagging scheme, labeling entities with 'B' (beginning) and 'I' (inside) to mark entity boundaries.
### 🧠 Architecture <a id="Architecture">
<img src="https://github.com/user-attachments/assets/1c677741-bf3d-4d90-b1b0-ba06e7cdf11b" width="500">

 #### 🤖 Two Named Entity Recognition NER Models:
1. The first model predicts the topping-style entities.
2. The second model predicts the PIZZAORDER and DRINKORDER entities.
3. The outputs of both NER models are then combined and converted into a structured JSON format for further processing
#### 📚 Layers
1. Embedding Layer: Each word in the sentence is mapped to a dense vector.
2. Bidirectional LSTM:This layer reads the input sequence in both forward and reverse directions, helping the model capture dependencies.



## ⭐Contributors<a id ="contributors">
<table  align='center'> 
<tr>
    <td align="center">
        <a href="https://github.com/yousefosama654">
            <img src="https://avatars.githubusercontent.com/u/93356614?v=4" width="100;" alt="yousefosama654"/>
            <br />
            <sub><b>Yousef</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/EmanElbedwihy">
            <img src="https://avatars.githubusercontent.com/u/120182209?v=4" width="100;" alt="EmanElbedwihy"/>
            <br />
            <sub><b>Eman</b></sub>
        </a>
    </td>
        <td align="center">
        <a href="https://github.com/nesma-shafie">
            <img src="https://avatars.githubusercontent.com/u/120175134?v=4" width="100;" alt="nesma-shafie"/>
            <br />
            <sub><b>Nesma</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/Sara-Gamal12">
            <img src="https://avatars.githubusercontent.com/u/106556638?v=4" width="100;" alt="Sara-Gamal1"/>
            <br />
            <sub><b>Sara</b></sub>
        </a>
    </td></tr>
</table>
<!-- readme: collaborators -end -->
<h2 align='center'>Thank You. 💖 </h2>
