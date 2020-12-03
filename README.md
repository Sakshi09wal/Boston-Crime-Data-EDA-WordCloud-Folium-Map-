# NLP

1. Data Preprocessing: The dataset consists of articles regarding Crime in NYC that were acquired from the News Articles from lots of USA Online news article by continuous querying using a wrapper for the News API over a period of 2 months.
           The batch of articles are acquired in raw JSON format. Various properties of the articles such as the content, description, URLs, publishedAt, title, source and other information including the title, source are extracted. The Description can provide a good source for creating discriminating features and they were folded as terms into the bag of words model for each headline where they were present. The publishedAt can also later provide a method to achieve time over topic model.

1.1	Text-Cleansing Process: The purpose of text cleaning is to simplify the text data and convert into a language that machine can understand. News Articles are written in natural language for human to understand. But those data are not always easy for computers to process. Hence, In this process, there are following steps in text cleansing:

•	Tokenization: A document is treated as a string, removing all the punctuations and then
partitioned into a list of tokens.
•	Removing stop words: Stop words such as conjunction and propositions, common noun like "the", "if", "and" ... are frequently occurring but no significant meanings which need to be removed. Also removing a lot of unwanted words which often come to the news articles but do not make any sense as a topic.
•	Stemming word: Stemming word that converts different word form into similar canonical
form. This process reduces the data redundancy and simplifies the later computation.

2. Methodology: This section deals with the two techniques employed in this work to topic-model our data. We ﬁrst discuss the LDA approach and then focus on the use of LDA Mallet Model. Both the techniques were implemented in Python (version 3.4) using the Gensim library. Genism provides a wrapper to implement Mallet’s LDA from within Gensim itself.
2.1. Text Mining: Text mining is the process of extracting good-quality information from text. Text mining usually involves the process of structuring the input text, finding patterns within the structured data, and finally evaluation and interpretation of the output. Typical text mining tasks include text categorization, text clustering, document summarization, keyword extraction and etc. In this research, statistical and machine learning techniques will be used to mine meaningful information and explore data analysis.
2.2. Topic Modelling: In machine learning and natural language processing, topic models are those  models, which provide a probabilistic approach to extract the significant tokens from the text and provide a probability of their significance using weight and scores . The "topics" signifies a unknown,  uncalculated , variable relations that link words in a vocabulary and their occurrence in the news article or a document . A article  is seen as a mixture of topics. Topic models discover the unknown themes throughout the collection and annotate the documents according to those themes. Each word is seen as drawn from one of those topics. Topic modelling provides us with methods to organize, understand and summarize large collections of textual information. It helps in:
•	Identifying the  hidden topical patterns that are present across the article or the document
•	Annotating documents according to these topics
•	Using these annotations to manage, search and conclude texts

Topic modelling can be described as a method for finding a group of topics  from a collection of news articles (documents ) that represents the information in the collection. 
There are many techniques that are used to obtain topic models. Finally, A document coverage distribution of topics is generated and it provides a new way to explore the data on the perspective of topics.
                                   

2.3 LDA Model On Crime data: LDA’s approach to topic modeling is it considers where document consider as a collection of topics and topic consider as a collection of words.
Gensim’s Library of the LDA algorithm. Mallet’s version of library often gives a better quality of topics LDA model is the best approach for extracting the topic from the document. Once you provide the algorithm with the number of topics, it will rearrange the topics outspread inside that documents and keywords. Create the Dictionary and Corpus needed for Topic Modeling where The two main inputs to the LDA topic model are the dictionary and the corpus. Gensim creates a unique id for each word in the document. Corpus is a combinatin of word_id and word_frequency.
For Building the Topic Model We have to train the LDA model. In addition to the corpus and dictionary, you need to provide the number of topics as well.
       Apart from that, alpha and beta are hyperparameters that affect sparsity of the topics. According to the Gensim docs, both defaults to 1.0/num_topics prior.
           Here are the dominant topic after using the LDA model on crime data.
 
       
And there also word cloud I found after using LDA on crime data:












3.Results : The coherence score is for assessing the quality of the learned topics. For one topic, the words i,j being scored in ∑i<j Score(wi,wj) have the highest probability of occurring for that topic.[7] The score that I have achieved was approximately 53% from the crime data.
3.1.Coherence Model : Firstly, we want our models to be simple and not to have too many topics. For instance, having 20 topics would trigger topics overlapping, potentially producing inaccurate results. 
                      Next, we aim for our model to have the highest coherence value. Coherence value measures the average of pairwise word similarity scores of words in a topic. The higher it is, the more accurate our model will be. As such, we tried two different models, each with the number of topics set from two to ten respectively and plotted a graph of their coherence values, as shown in the figure below.

 

3.2Visualising Our LDA Model 
We deployed a package – pyLDAvis – to help us visualize our model. An interactive copy of the visualization is provided in the attached code. A snapshot of the visualization is as follows:
 


4. Conclusion:
Crime data is a sensitive domain where topic modelling techniques play vital role for crime analysts and law-enforcers to precede the case in the investigation and help solving unsolved crimes faster. Similarity measures are an important factor which helps to find unsolved crimes in crime pattern. LDA algorithm is one of the best methods for finding best topics related to crime. This paper deals detailed study about importance of LDA in crime domain.

5. Discussion: 
The scope of crime data analysis extends far and wide. This thesis provides only a starting point to crime data analysis. Future work may want to include a deeper analysis of historic data to create patterns or more recent data for newer developments. Multiple year data allows for a comparison of annual trends, which is especially important when considering holidays. Using multiple years can
provide more crime rate information for rainy days so that a more concrete conclusion can be drawn .In addition to our objective of simply discovering how worldwide health topic evolves over time, we also discovered several insights that was out of our initial scope. We discovered the pattern in how each news channel from different part of the world tend to report their news article.
It was also discussed within project’s group member, in future ,  we can augment two additional datasets to increase the accuracy and quality of the results .
•	In first approach we can analyze how unemployment rates are related with crime data in the news articles and in second approach we can find how poverty levels are  related to crime rate  in the new articles . 
•	We can also augment geolocation with poverty level with the crime committed. This will further facilitate the better quality and accuracy of the whole model. We also discovered that it is possible for us to determine the time period in which events are happening, even when there is no specific period mentioned online in the news article .So augmenting time with geolocation will get us interesting insight and patterns in relation to the news online .

