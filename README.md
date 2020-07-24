# TLInternship2020
## Find Articles Supporting cause of Hydroxychloroquine

This project aims on finiding links which support the cause of Hydroxychloroquine.
Its a sample project on NLP and NLTK is one the most useful library

Comcrawl is used for finding important links within a particular domain, and beautiful soup for scrapping those links

Only one file is used to run the entire project (however, it can be splitted into multiple files)

#### Code Structure:

The code can be broken down into 5 parts
1. Crawler Class: This class uses comcrawl library to gather important links within a specific domain. In this case, I used fda.gov domain to find links related to hydroxychloroquine. Alternative to this can be who.int
For the sake of simplicity, only one domain is chosen

2. WebPageReader Clsss: This class scrapes through links to find text related to search_word (hydroxychloroquine). The search word can be anything and the code will alter the way we want. I used bs4 library to scrape through the links.

3. 
I gathered only titles if the search word appeared in the link.
If the search word appeared in the raw html text, I scrape through all the paragraphs and store paragraphs which have the word.
