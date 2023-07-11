## Text Summarizer & Analyzer

##### SwiftSummarizer | Creator
**Business Problem:** Free Tool to Summarize and get key insights into any piece of text. 

**Solution Highlights:** 
  * Summarizer uses PyTorch and Transformers to encode semantic meanings of sentences which are fed into a clustering algorithm to create a robust summary. Key insights generated with NLP methods, spacy, transformers.
  * Responsible for building Django Web App and integrating the backend with a ReactJS frontend. Used Django REST framework, passed data via AJAX calls. Deployed using Git-LFS and PythonAnywhere.

**Write-up:** 

Built Django Web App and all Machine Learning models. I was also responsible for compiling the entire system and pushing it into Production. While Deployed, Swift Summarizer averaged about 400 page views per month.

The summarizer model was built using Pytorch. The first step was to separate the article into sentences and preprocess all text. From there, we can use a word embedding model to get the semantic meaning of each word in a vectorized format. Each word embedding is joined to form the original sentences and we now have a sentence embedding.

These sentence embeddings are fed into an unsupervised clustering model which is able to accurately construct a robust summary. The various insights like identifying key phrases, rare words, names, and locations are generated using various Natural Language Processing methods, the spacy library, and the transformers model.

On the Web App side, I built the Django Web App and integrated the backend with a ReactJS frontend. To pass data from the client-side to the backend, I used Django REST framework and AJAX calls. I deployed the finished product using Git-LFS and PythonAnywhere.

Below is a walkthrough on how the app works.

You will first be prompted to paste in an article that you want summarized. You can also upload an image and the OCR algorithm will convert the image to text to then be used for summarization. You would then select a summary size and hit submit to generate a summary and key insights.

<img src="images/ss_1.png?raw=true" />

After hitting submit, you will see that a summary has been generated.

<img src="images/ss_2.png?raw=true" />

Along with a summary, Swift Summarizer also provides insights like key phrases, rare words, names, and any locations found in the article.

<img src="images/ss_3.png?raw=true" />

###### All Intellectual Property of this work belongs to Purdue University and therefore I cannot show any code.


