# Twitter_Depression_Detection
**REFERENCE for the 'Twitter Classes' :  https://github.com/vprusso/youtube_tutorials/tree/master/twitter_python

## ISSUE

In today's world, we are often consumed with our phones and our lives on social media rather than making connections in the real world. This can have a significant negative impact on our social emotional stability and moods. We can esliy get some news that lots of people who are suffering from mental illness such as depression, however, it is hard for us to notice their situation to help them. 

## SOLUTION

I tried to solve this problem by using social-media itself. Made a model that can find out depression value by analyzing one’s tweets. This supposed that someone who is suffering from depression does not use the exact word ‘depress’ or ‘depression’. Therefore, this model should be made by the principle based on what and how words are related to ‘depress’ 

### Json -> extract and modify -> insert into DB
![3](https://user-images.githubusercontent.com/70621565/103338544-b9328d80-4a4c-11eb-95ff-786f4f4bee58.jpg)
![4](https://user-images.githubusercontent.com/70621565/103338552-bdf74180-4a4c-11eb-82bd-bfca7415315c.jpg)
### HOW TO MAKE THE DEPRESSION_SCORE MODEL
  a. TOKENIZE the refined TEXT with the KEY words that polarity value is lower than -0.5 (tokenized words related to bad emotion)
  
  b. TOKENIZE the refined TEXT with the KEY words that polarity value is 0(tokenized words related to neutral emotion)
  
  c. The Result from 1st step - Result from 2nd step
  
  d. GIVE penalty to stop words from the result of step 4.
  
  e. Delete KEY WORDS and Ad materials from the result of step 3.
  
![6](https://user-images.githubusercontent.com/70621565/103338555-c18ac880-4a4c-11eb-81e3-336276f1ca79.jpg)
![7](https://user-images.githubusercontent.com/70621565/103338558-c3548c00-4a4c-11eb-88be-2048fbce7fbd.jpg)

## RESULT

![image](https://user-images.githubusercontent.com/70621565/103339080-6eb21080-4a4e-11eb-8d5f-ff374012abdf.png)
![image](https://user-images.githubusercontent.com/70621565/103339089-72de2e00-4a4e-11eb-9535-a5a0f57cd2d7.png)
![image](https://user-images.githubusercontent.com/70621565/103339092-7671b500-4a4e-11eb-962e-7c3aaa48a8d0.png)

## EXTENSTION

This model is not only about depression detection but also positive and negative Word Vectors for any keywords.
For example, suppose that we want to predict the 'Samsung Electronics' stock price. With this model, we can define positive and negative word vectors regarding 'Samsung electronics'. After that, it enables us to get implicitly positive and negative real-time tweets about 'Samsung electronics' which can be a feature for the stock prediction.


## How to commit 

1. Fill the .env file with your twitter authenticaters 

2. Open the TwT_DP_DETECTION.ipynb and commit the cell sequentially.( without step 1, you can commit the example model with the json files that I extracted)



