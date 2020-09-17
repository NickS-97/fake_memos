# Python Faker Package - Audit Memos

This python notebook was part of a final group project for my Audit Innovation Masters Course

The goal of the project was to train a classifier (using RapidMiner software) to classify an audit memo as either an 'inventory memo' or a 'subsequent events memo.' We obviously needed training data for the model, but there are no publicly available audit memos and drafting enough by hand would have taken an enormous amount of hours. 

To solve the issue of training data, we decided to generate synthetic data using the Faker package. We first downloaded all the text from the PCAOB AS (see links below). We then used JMP software to generate word lists of the most commonly used words in each standard. We took the top 100 and imported them as lists into the notebook. 

Using these two separate keyword lists, we randomly generated sentences using the Faker package that contained both the key words and "noise" - random words such as 'dog' that have nothing to do with auditing. Becuase we controlled which list (either inventory or sub events) we pulled the keywords from, we could classify the fake "memo". We quickly generated 2000 memos each for both inventory and subsequent events and used these to train our model. 

I thought this was a fun way to tackle the challenge of training data, and so I wanted to share this solution. It has made me curious as to how often synthetic data is used in model training and development. 