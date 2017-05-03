# Emotional-Arc-Analysis
### Analyzing the emotional sentiment of entire books to make a recommender system based on langauge.

This project was based on research done [here](https://arxiv.org/abs/1606.07772)

Using Books from [Project Gutenberg](https://www.gutenberg.org/) to get full text versions of a wide range of books.

My goal was to perform sentiment analysis on an entire book. This involved windowing through the entire book in overlapping intervals.
I compared my results to those of the [Hedonometer](http://hedonometer.org/books/v1/). The results were comparable. 

I performed [SVD](https://en.wikipedia.org/wiki/Singular_value_decomposition) to decompose the emotional arcs of the books into six main vectors, and then recompose all sentiment vectors with these six. 

My intution was that this would recreate strongly those stories which match the main six emotional arc vectors. I decided to cluster using agglomerative clustering and visualize the top arcs. 

To verify my results based on random words or if there was some systematic resonance of my windowing system I created randomized word "books" and did the same analysis, emotional arc mapping, SVD, and clustering. I compared the two systems using FFT to see if there were any possible resonances, e.g. any sort of strongly correlated emotional arcs. The results suggest that the random "books" had no such correlation.



The simplified emotional arcs with their labels were used, as well as vectorized books,NLP created features from each book, into a recommender system.

Results were qualitative for the recommender system, because it's rather hard to verify whether or not the language is similar or not.
