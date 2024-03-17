# Question answering project

This project aims to create a system that can generate the answer to a determined question. This system is made of 2 different models. One, (information retrieval) is in charge of reading the user's question and identifying the document with related information about it.
The other reads the found document and the user's question to generate text with the requested answer.

## Information retrieval

This is the system part that indexes all the documents in a dataset and identifies the appropriate one for the user's question.

[Papers by Subject] dataset has been used as a corpus dataset. You can check code implementation in the following collab notebook

<a target="_blank" href="https://colab.research.google.com/github/https://colab.research.google.com/drive/1z8yL7FyolUSLP-qTwOK1NYkurvPB6qUh?usp=sharing">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>


[Papers by Subject]: https://www.kaggle.com/datasets/arplusman/papers-by-subject/data
