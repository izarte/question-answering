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

<a target="_blank" href="https://colab.research.google.com/drive/1z8yL7FyolUSLP-qTwOK1NYkurvPB6qUh?usp=sharing">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

| Model    | Result   |
|----------|----------|
| Row 1    | Data 1   |
| Row 2    | Data 2   | 



[Papers by Subject]: https://www.kaggle.com/datasets/arplusman/papers-by-subject/data
[CISI]: https://www.kaggle.com/datasets/dmaso01dsta/cisi-a-dataset-for-information-retrieval
