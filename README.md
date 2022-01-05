# Text labeling and similarity recognition of agricultural articles
![農業文字辨識](https://user-images.githubusercontent.com/92705727/148278896-7aff606e-44ca-4827-8335-5101e822b193.png)
農業文章文字標註及辨識(https://aidea-web.tw/topic/de144f63-cd15-40b8-81e6-82db5636d598)
# How to use
Everything to get started is in the colab notebook(https://drive.google.com/drive/folders/11S8Hgw3Wah1XLac0DCinUn6SPJzMIRcr?usp=sharing).

# What's in here
1. This model uses the Jieba toolkit with relevant experience to segment the article and replace the synonyms, and sample the keywords after loading the dictionary.
2. Use TF-IDF and Cosine similarity tools, which are suitable for processing the number of keywords, to perform article vectorization and similarity comparison using data query.
3. For four different regression classification models, after comparing the training accuracy, select the KNN model line as the final module to use and make predictions.

# Hint for processing
1. Train data set reading
2. Load Jieba and synonyms dictionary and replace synonyms
3. Use Jieba for tokenization processing
4. Load the keyword dictionary and take out the keywords in the token. This step is divided into three parts: crops, diseases and insect pests, and chemical agents.
5. Establish three categories of keyword quantity parameters for each article
6. Perform TF-IDF processing and vectorize the keywords of each article
7. Perform Cosine similarity processing to generate a comparison value of article similarity
8. In all permutations and combinations, compare the Yes combination of Trainlabel.csv to Label, all other combinations are No
9. Take the combination of Yes and No to filter out the training data set at a ratio of 1:1
10. Load sklearn.linear.model after dimension conversion, divide the data set into Train and Test, and use Logistic Regrssion, KNN, Decision Tree, Support Vector Machine for classification training
11. After comparing the accuracy with F1-Score, select the best model and load the Joblib tool to save the model
