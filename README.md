# four weeks to top 10 🎵

can an album's first four weeks on the billboard 200 predict whether it will reach the top 10 later? this project uses historical chart data and machine learning to find out!

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

| metric    | score |
| --------- | ----- |
| accuracy  | 93.0% |
| precision | 61.8% |
| recall    | 79.4% |
| f1-score  | 0.695 |
| roc-auc   | 0.936 |

the model correctly identified 385 of the 485 albums that reached the top 10 after their first four chart weeks. it also missed 100 successful albums and made 238 false positive predictions.

although the model achieved 93% accuracy, accuracy alone doesn't tell the whole story. the precision score means that about 62% of its positive predictions were correct, while its recall score means it identified about 79% of the albums that eventually reached the top 10 after their first four weeks.

feature importance analysis showed that an album's fourth-week chart position was the most influential feature, followed by its third-week position. this suggests that performance across the first few weeks may provide useful information about an album's later chart success.

i also tested the random forest model on albums by artists that weren't included in its training set. it achieved 92.6% accuracy and a roc-auc of 0.915 in that experiment, suggesting that the model can also identify useful patterns for unfamiliar artists.

## tools used

- python
- pandas
- numpy
- matplotlib
- scikit-learn
- jupyter notebook

## dataset

the dataset was obtained from [utdata's billboard 200 repository](https://github.com/utdata/rwd-billboard-data), which regularly collects and updates billboard chart data.

the dataset is not included in this repository because of its size. please visit the original repository to access the data.

the analysis in this project uses the dataset version available during development, so the results may differ if the data is updated.

## future improvements (●'◡'●)

this is an ongoing project, and there are several things i'd like to explore next:

- add spotify audio features to see whether musical characteristics improve predictions.
- include an artist's previous chart history.
- experiment with other machine learning models and compare their performance.
- improve the validation process and explore ways to make predictions more reliable.

as i continue learning, i plan to build on this project, test new ideas and improve the model over time.

## conclusion

this project gave me an opportunity to apply data cleaning, exploratory data analysis, feature engineering and machine learning to something i genuinely enjoy: music.

the results suggest that an album's early chart performance can provide useful clues about its later chart success, although the model still makes mistakes. this project is a starting point for further experimentation, learning and improvement.
