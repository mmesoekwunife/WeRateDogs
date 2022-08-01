# WeRateDogs

## Dataset

The datasets used for this analysis were gathered from three
different sources.
* The twitter_archive_enhanced.csv file was manually
downloaded from udacity and uploaded and read in using read_csv().

* The image_predictions.tsv file was downloaded from this
[URL](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv) using the requests library.

* The tweet_json.txt was gotten by querying the Twitter API
for additional data using the python tweepy library.

### Objective

Wrangle the twitter data (@WeRateDogs) to create
interesting and trustworthy analyses and visualizations.

### Data quality issues

The following issues were observed after assessing the dataset.

* Twitter archive table

1. Only original tweets are needed therefore no retweets.

2. Original tweets with images (image_urls).

3. Descriptive column name (dog_name) instead of name.

4. "O" instead of "O'Malley" as dog name.

5. Texts not readable in source columns.

6. Erroneous datatypes (tweet id, timestamp, source, dog stage,
rating numerator, and rating denominator)

7. &amp; instead of & in the text column.

8. Some texts contain floof and still have 'None' as their dog
stage values.

9. The dog_name column contains inconsistencies like a, the,
quite, an, such, not, very, mad etc.

10. Tweet with incorrect rating of 24/7 which means another thing.

* Image predictions table

1. Erroneous datatypes (tweet_id)

* Tweet count table

1. tweet_id instead of id in order to merge with the other
tables.

* Tidiness issues

1. One variable in four columns in twitter archive table
(dog_stages).

2. Merge the Image predictions, tweet count and twitter
archive tables to form a single table.

A copy of each dataset was made before cleaning the data quality issues and finally stored 
to aid the exploratory data analysis.

## Analyzing and Visualizing Data

### Insights:

1. Dogs with low ratings are either tweets without a dog's picture in it or a plagiarized post for example, a twitter handler @BBAnimals posted a picture with Dog_rates tag on it.    The links to [plagiarism tweet](https://t.co/YbEJPkg4Ag) and [No dog picture tweet](https://t.co/Asgdc6kuLX)      

2. Pupper is the most popular dog stage while the least is floofer.

3. The highest rated dog is Atticus with a rating of 177.6.

4. Tweet id 822872901745569793 had the highest favorite counts of 132810 while tweet id 744234799360020481 had the highest   retweet counts of 79515.

5. Tweet id 666102155909144576 had the least favorite and retweet counts of 16 and 81 respectively.

6. Charlie is the most popular dog name.

### insights from visualization:

1. The month of June had the highest number of retweets and favorites count 
while the month of September and August had the least.

2. Bulk of the retweets fall within the range of 0-10000 while that of favorites 
fall within 0 - 40000 with a few outliers. The outliers are mostly from the year
2016 and 2017.

3. The ratings over the years fall within the range of 0 - 2 with a few outliers. 
The outliers account for the unique rating system of WeDogRates.

4. The Labrador retriever and Golden retriever were the top dog two breeds predicted 
by Model A based on the favorites count.
