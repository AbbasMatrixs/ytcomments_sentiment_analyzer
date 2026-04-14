
                                                                        **Sentiment Analysis of YouTube Comments**

Step 1: Scraping Comments
use Selenium to collect comments from 3 YouTube videos. The browser was automated to scroll and load more comments until we gathered 5k comments.
These were saved in a CSV file.

Step 2: Preprocessing Text
The comments were cleaned by:
- Removing links, symbols, emojis, and extra spaces
- Lowercasing all words
- Removing common and YouTube-related stopwords
- Lemmatizing words to their root form (e.g., “likes” → “like”)
The clean dataset ready and save into cleaned_Youtube csv file.

Step 3: Feature Engineering
Each comment received a sentiment score using TextBlob (positive or negative).
We then used TF-IDF to turn the text into numerical features that represent word importance.

Step 4: Model Training
A Logistic Regression model was trained using the TF-IDF features.
We split the data (80% train, 20% test) and labeled each comment as positive or negative based on its sentiment score.

Step 5: Model Evaluation
The model was tested on unseen data and achieved accuracy. It was able to correctly classify most comments based on their sentiment.


Summary
We built a full sentiment analysis pipeline from scratch — starting with scraping YouTube comments, cleaning them, assigning sentiment,
 and training a model to detect if a comment is positive or negative.
