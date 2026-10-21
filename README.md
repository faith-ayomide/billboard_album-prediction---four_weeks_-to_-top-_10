# billboard_album_prediction-four_weeks_to_top_10

can an album's first four weeks on the billboard 200 predict a future top 10 run? this project uses historical chart data and machine learning to find out!

# four weeks to top 10 🎵

can an album's first four weeks on the billboard 200 predict whether it will reach the top 10 later?

this project started with my habit of listening to music and wondering why some albums become huge successes while others don't. i wanted to explore whether machine learning could help predict an album's future chart performance using its first four weeks on the billboard 200.

## what i did

- cleaned and explored historical billboard 200 chart data.
- used an album's first four chart positions to create features for prediction.
- built and compared logistic regression and random forest models.
- evaluated the models using accuracy, precision, recall, f1-score and roc-auc.
- explored which early chart positions were most useful for predicting later success.
- tested the random forest model on albums by artists that were not included in its training set.

## results

the random forest model performed best overall on the chronological test set.

| metric | score |
|---|---:|
| accuracy | 93.0% |
| precision | 61.8% |
| recall | 79.4% |
| f1-score | 0.695 |
| roc-auc | 0.936 |

the model correctly identified 385 of the 485 albums that reached the top 10 after their first four weeks. however, it also made some incorrect predictions, so its results should not be treated as guarantees.

feature importance analysis showed that an album's fourth-week chart position was the most influential feature, followed by its third-week position. this suggests that performance across the first few weeks may provide useful information about an album's later chart success.

## tools used

- python
- pandas
- numpy
- matplotlib
- scikit-learn
- jupyter notebook / google colab

## dataset

the data was obtained from [utdata's billboard 200 repository](https://github.com/utdata/rwd-billboard-data), which regularly collects and updates billboard chart data.

this project uses the available historical billboard 200 records to explore album performance and predict later top 10 success. the analysis is based on the dataset version used during development.

## future improvements (●'◡'●)

this is an ongoing project, and there are several areas i would like to explore next:

- add spotify audio features to see whether musical characteristics improve predictions.
- include an artist's previous chart history.
- experiment with other machine learning models and compare their performance.
- improve the validation process and explore ways to make predictions more reliable.

as i continue learning, i plan to build on this project, test new ideas and improve the model over time.

## conclusion

this project gave me an opportunity to apply data cleaning, exploratory data analysis, feature engineering and machine learning to something i genuinely enjoy: music.

the results suggest that an album's early chart performance can provide useful clues about its future success, although there is still room for improvement. more importantly, this is a starting point for further experimentation and learning.
