# Project Steps

## A) Data Collection
We use beautifulsoup to write a script to download all movie scripts from IMSDB.

## B) Data Preprocessing
In this part, we will be cleaning the text files before extracting a list of words from them. The
preprocessing pipeline includes at least 3 steps e.g. (removing spaces, removing stopwords, removing
punctuation).

## C) Feature Extraction
In this part, we will make sure that each movie script has now been converted into a vector of filtered
words.

## D) VAD Vectorization
Converting each movie script’s list of words into valence, arousal and dominance could be done manually
using map() function or could be done using emotion() function using labMT’s builtin method. Since some of the words in the scripts do not have a
corresponding value in the VAD dictionary, we can replace them with 0s. Finally, we now have 3 very
large vectors, that consist of 0s and other values that were replaced from the VAD dictionary. We need
to strip down all the 0s from the vectors and average them using windows of size 500. So every 500 (nonzero)
values will be replaced with a single value that represents the average.

## E) Output
Now that we have 3 vectors for every movie script. We plot all 3 vectors onto the same figure (using any 3
different colors) and save that figure to a jpg file with the same name as the movie script. For instance,
the corresponding figure for the movie “17 Again” would be “17 Again.jpg”

# Samples
## Dark City
![Dark-Ciy](https://github.com/BasselSharaf/Movies-Sentiment-Analysis/assets/15571269/7cf20a95-ab49-4bf4-912b-7629ade53d16)

## Halloween The Curse of Michael Myers
![Halloween-The-Curse-of-Michael-Myers](https://github.com/BasselSharaf/Movies-Sentiment-Analysis/assets/15571269/86ca767a-0595-47d5-9ead-34a0e979fb90)

## Final Destination
![Final-Desinaion](https://github.com/BasselSharaf/Movies-Sentiment-Analysis/assets/15571269/2ba0617d-ed42-4d04-b738-f73c2623cb2d)

## Boogie Nights
![Boogie-Nighs](https://github.com/BasselSharaf/Movies-Sentiment-Analysis/assets/15571269/3d2fa9bd-c67a-4caf-9e37-7e4ae8d6edf4)

