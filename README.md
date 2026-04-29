# Who Talks About What? Gendered Political Agendas in French Legislative Manifestos (1973–1993)

### Author: Micaela Linares

## 📄 Abstract
This study examines gender-based thematic differences in political manifestos among candidates to legislative elections in France from 1973 to 1993, using the Archelec corpus produced by Science Po. I implement Latent Dirichlet Alloca- tion (LDA), an unsupervised machine learning technique, to discover the most frequently covered topics and assess their distribution by gender. The results suggest that political communication is not gender neutral. While men largely prioritize "high politics" and broad concerns, focusing on socioeconomic and regional development issues, as well as on electoral and institutional frameworks ; female candidates exhibit greater thematic breadth , often incorporating stronger ideological and identity-based components. They are more likely to engage with ecology, gender, and labor identity topics and to occupy the poles of the ideological spectrum, addressing either "regalian" traditionalism or far-left class struggle. Al- together, these findings suggest a gendered structuring of political communication and policy agendas in a context marked by low female representation and the ideological polarization of the Cold War and immediate post-Cold War transition.


## 📂 Project Structure

* **`report.pdf`**: The final research report.
* **`code/`**:
    * `EDA.ipynb`: exploration of and filtering out 'non déterminé' gender, document and text descriptive statistics, top-word gender and time descriptive analyses.
    * `LDA.ipynb`: text BoW vectorization, LDA topic modeling, model selection, and gender topic analysis.
    * `text_preprocessing.ipynb`: Text cleaning.
* **`data/`**: digitalized manifestos' transcriptions, French stopwords and cleaned dataset.
* **`literature/`**: academic references.
* **`metadata/`**: Candidate and substitute demographics and election-specific metadata.
* **`temp/`**: saved LDA models for model selection (from 3 to 20 topics). Requires Git LFS.
* **`fr_core_news_md-3.8.0-py3-none-any.whl`** : French spaCy model used for lemmatization.


## ⚙️ Setup & Reproduction
To reproduce the analysis:
1. Ensure Git LFS is installed and pull the large files.
2. Run `text_preprocessing.ipynb` to produce the cleaned data file 'cleaned_master_data.parquet' and save it in `data/`  (optional, as 'cleaned_master_data.parquet' is already provided).
3. Run `EDA.ipynb` to explore the parquet dataset and obtain descriptive statistics on the corpus.
4. Run `LDA.ipynb` to vectorize the text, run the LDA models and reproduce gender topic analysis.
