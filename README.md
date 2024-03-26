Authors: [Daniel Frau Alfaro], [Jesús López Galbis], [Cristina Romero Mirete], [Iñigo Zárate Rico]

# Question answering project

This project aims to create a system that can generate the answer to a determined question. This system is made of 2 different models. One, (information retrieval) is in charge of reading the user's question and identifying the document with related information about it.
The other reads the found document and the user's question to generate text with the requested answer.

## Information retrieval

This is the system part that indexes all the documents in a dataset and identifies the appropriate one for the user's question.

[Papers by Subject] dataset has been used as a corpus dataset. This dataset counts 50.000 academic papers. You can check code implementation in the following Google Collab notebook.

<a target="_blank" href="https://colab.research.google.com/drive/1z8yL7FyolUSLP-qTwOK1NYkurvPB6qUh?usp=sharing">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

To evaluate different model performances to be used with the final dataset ([Papers by Subject]), another smaller dataset with ground truth information is used. [CISI] dataset fills these requirements with 1.460 documents and 112 associated queries. You can find tested models with results in the table below, and also a Google Collab notebook with the experiment results.

<a target="_blank" href="https://colab.research.google.com/drive/1JdqBLOO3AnFsDi-wWicBVNeeelsZa_UJ?usp=sharing">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>


In the following table information retrieval results are shown
|Information retrieval| |Evaluation without FAISS| |Evaluation whit FAISS| |
|:---:|:---:|:---:|:---:|:---:|:---:|
|**Corpus**|**Modelo**|**MRR**|**Precisión**|**MRR**|**Precisión**|
|**CISI**|all-MiniLM-L6-v2|14,3 // 78,6|29,6 // 84,8|21,1 // 81,7|43,7 // 91|
| |bert-base-uncased|7,9 // 16,4|14 // 28,8|11 // 25,9|22,3 // 35,7|
| |declutr-sci-base|9,33 // 57,2|17,5 // 75,7|14,2 // 66|27,6 // 80|
|**PBS**|all-MiniLM-L6-v2|76|83|93,5|98,8|
| |bert-base-uncased|15|23|30|40|
| |arxiv-distilroberta-base-GenQ|46|70,7|80,5|90,4|

In the following table language generation results are shown
|Language generation| | Query-Aware evaluation| | | | Query-Independent evaluation| | | |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|**Corpus**|**Modelo**|**BLEU**|**BERT-Precision**|**BERT-Recall**|**BERT-F1Score**|**BLEU**|**BERT-Precision**|**BERT-Recall**|**BERT-F1Score**|
|**CISI**|bart-large-scientific-lay-summarisation|0|83|78,4|80,6|0|83|78,5|80,6|
| |llama-2-chat-13b|1.315|83.52|80.845|82.83|0|89.24|83.77|86.42|
| |google/gemma-2b-it|0|83.46|79.68|81.53|0|75.67|73.70|74.68|
|**PBS**|bart-large-scientific-lay-summarisation|0|89,4|88,3|88,8|0|89,4|88,2|88,8|
| |llama-2-chat-13b|0|89.71|90.37|91.28|0|90.09|83.87|87.32|
| |google/gemma-2b-it|0|88.32|88.16|87.93|0|76.5|73.94|75.65|




[Papers by Subject]: https://www.kaggle.com/datasets/arplusman/papers-by-subject/data
[CISI]: https://www.kaggle.com/datasets/dmaso01dsta/cisi-a-dataset-for-information-retrieval
[Cristina Romero Mirete]: https://github.com/crisrm128
[Daniel Frau Alfaro]: https://github.com/DanielFrauAlfaro
[Jesús López Galbis]: https://github.com/jlg90
[Iñigo Zárate Rico]: https://github.com/izarte
