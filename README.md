# Text-Summerizer-using-Cosine-Similarity-NLP-

Summarization can be defined as a task of producing a concise and fluent summary while preserving key information and overall meaning.

How text summarization works?

In general, there are two types of summarization, abstractive and extractive summarization.

1.	Abstractive Summarization: 

Abstractive methods select words based on semantic understanding, even those words did not appear in the source documents. It aims at producing important material in a new way. They interpret and examine the text using advanced natural language techniques in order to generate a new shorter text that conveys the most critical information from the original text.
It can be correlated to the way human reads a text article or blog post and then summarizes in their own word:
Input document → understand context → semantics → create own summary

2.	Extractive Summarization: 

Extractive methods attempt to summarize articles by selecting a subset of words that retain the most important points.
This approach weights the important part of sentences and uses the same to form the summary. Different algorithm and techniques are used to define weights for the sentences and further rank them based on importance and similarity among each other:
Input document → sentences similarity → weight sentences → select sentences with higher rank

We will be using an unsupervised machine learning approach to find the sentences similarity and rank them. One benefit of this will be, you don’t need to train and build a model prior start using it for your project.

It’s good to understand Cosine similarity to make the best use of code you are going to see. Cosine similarity is a measure of similarity between two non-zero vectors of an inner product space that measures the cosine of the angle between them. Since we will be representing our sentences as the bunch of vectors, we can use it to find the similarity among sentences. Its measures cosine of the angle between vectors. Angle will be 0 if sentences are similar. (as cos 0 = 1, i.e similarity is 100%)

![image](https://user-images.githubusercontent.com/84669222/142742382-d511d42c-7b46-4521-8192-066eaf6a7710.png)

The algorithm will follow those steps:

Input article → split into sentences → remove stop words → build a similarity matrix → generate rank based on matrix → pick top N sentences for summary → output the summarized text

