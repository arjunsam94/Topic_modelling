# Topic modelling with blog titles

## Background
To analyze BetterHelp's SEO content for a personal project, I exported the blog data from the platform, <a href="https://mangools.com/">Mangools</a>.

## Problem
The raw data exported from Mangools had over 400 blog titles and it was difficult to identify themes behind content that is driving traffic to Betterhelp.

## Solution
Used Word2Vec and LDA Topic modelling to identify top topics that all blog titles fall under. This involved:

* Tokenized all words in the blog titles, removed stop words, and applied lemmatization to preprocess the dataset.
* Used TfidfVectorizer to create vector embeddings and a document-term matrix.
* Identified the top 6 topics and relevant terms using the Latent Dirichlet Allocation (LDA) method.

## Results
* Topics 1 and 3 show that blog titles focusing on relationships/partners are quite common to form a theme, indicating that Betterhelp generates siginficant traffic with this theme.
* Topic 2 shows that blogs focusing student mental health issues are also common enough to form a theme.
* Other topics seem to be centered around promotions.

## Considerations
* While topic modeling is effective when applied to the entire dataset, it can yield more targeted insights when applied to data filtered by specific metadata such as age, country, or device, depending on the analysis objectives.
* For large document collections, leveraging LLMs can be an efficient approach to identify key themes and generate meaningful content, though their speed may vary compared to traditional topic modeling algorithms depending on computational resources.
