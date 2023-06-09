## Destination recommendation API
- Travel destination recommendation system based on user personality, user current mood, and destination theme (tendency)

## Techstacks.
- Anaconda, Python 3.7, Flask, tensorflow, pandas, numpy, Scikit learn, Jupyter, AWS(EC2(Ubuntu), RDS, S3)

## Data.
- **Destination review text**
   - 'Visit Jeju' review text, 'TripAdvisor' review text crawling
- **Personal preference data**
   - Formation of survey items based on research papers related to travel destination satisfaction according to individual characteristics
- **Google Form** 
   - Five-choice multiple-choice survey questions to identify personal tendencies + travel destination preference according to individual mood

## Model construction.
1. **Travel destination review text theme classification**
   - Input data : Travel destination review text 
   - Model : RNN
   - Output : Classification of leisure/experiences, nature, and education (by softmax)
2. **Travel destination recommendation model**
    - Input data : Personal tendency questionnaire, travel destination classification Softmax(DB), Personal mood labeling data
    - Model : DNN
    - Output : Travel destination recommendation

## Reference.
- [The Effects of 5 Factors of Traveler's Personality on Psychological Happiness and Travel Experience](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART002701039)
- [Reference material](https://www.youtube.com/watch?v=omzBnL22aBA)
    
