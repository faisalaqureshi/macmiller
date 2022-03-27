# macmiller
An NLP analysis of Mac Miller's music over the ages

## Prevalence of themes across Mac Miller's discography
![matplotlib graph](\macmiller\Screen Shot 2022-03-27 at 4.33.46 PM.png)

## Project Goal:
The aim for this project was to analyze the main themes of Mac Miller's music accross his albums, and to create a reccomendation system of similar Mac Miller songs based on your favorite song.

## Data
I used [lyricsgenius](https://github.com/johnwmillr/LyricsGenius) to scrape lyrics from [genius.com](https://genius.com/) and export it as a json to analyze on Python.

## Files

- SpotifyNLPAnalysis.ipynb: This contains the entire notebook for the project, from start to finish!
- lyrics: This folder contains the json files for all the lyrics across albums.
- table_w_topics.csv: This csv table contains all the songs with the proportion of lyrics that are within a certain topic model

## Techniques/Tools Used

- Count Vectorization
- LDA (Dimentionality Reduction / Topic Modelling)
- POS Mapping (for nltk's Lemmatizer)
- SQL (pandasql)
- Matplotlib / Seaborn
- Cosine Similarity
- Heap Sort
- Regex

## Challenges

One big challenge was choosing accurate stop words: hip hop lyrics are embedded with countless metaphors, so asides from the based "to" "the" and more, I also had to remove the "gonna" "imma" and more. This required some trial and error.

Further, getting the lemmatizer to work was a little tricky as I had to map the POS tag to each word for each song. However, through online resources and my code, I was able to rectify this.

I initially used gensim for the LDA, but later realised that it doesn't help give an accurate proportion for all topics, just the most prevalent ones. Hence, I decided to use scki-kitlearn's LDA modelling as it gave me proportions for all topics.

More trivial challenges are addressed in the notebook!

## Future Scope

For future work, one could analyze the musical elements alongside the lyrics to gather even more interesting insights and a stronger reccomendation system! One could also analyse all of Mac's discography and compare it to other artists.
