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

3. FindHateSpeech Class: This class generates polarity score of a text.

4. Main Class: This section binds all the classes.
I gathered only titles if the search word appeared in the link.
If the search word appeared in the raw html text, I scrape through all the paragraphs and store paragraphs which have the word.

5. Arguments: This is where all the main or key points for this code to run or find is defined.

Points:

*"key_index" : ["2020-29", "2020-24","2020-16","2020-10", "2020-05"],
"website" : "fda.gov/drugs/\*",
"dataframe_path" : "output.csv",
"search_word" : "hydroxychloroquine",
"positive_threshold" : 0.2,
"threads" : 6
*

#### How to run:

Keep it simple. Download this file, and execute it on command line or any Python supported IDE.

#### Scope of Improvement:
As of now, the code will consider only one paragraph for every link to figure out if the article supports the use of Hydroxychloroquine.
Also, scrapping part is too long. This can be reduced by the proper use of multithreading.
