Plans for Search Improvement

1. language sensitivity
    a. built ts_vectors with the correct language config
        i. deploy all available language configs to existing postgresql install
        ii. determine how to deploy additional ones (Polish, etc.)
        iii. map ISO language codes to ts config name
    b. Langauge of the search request, as well:
        i. provide mechanism in API to set  query language
        ii. guess language if nor provided? (Frontend? Backend?)
    c. What about other non-latin languages? Chinese, etc.
        i. design additional indicies for non-alphabetic languages
        ii. switch to using those indicies based on query language

2. Speed up (with weighted search)
    a. investigate lumping additional info into tsvector, with weights:
        i. GIN index doesn't work with weights: do GIST?
        ii. can we replicate weights in SQL w/  joins?
            i.e. merge all fields (title, subject, keywords, etc.) into FTI,
                use matches on other fields as well
        iii. Push narrowing of search (matches for author, keyword, etc.) into SQL query

3. search language improvements
    a. allow quoted phrases for adjacency
    b. ?




