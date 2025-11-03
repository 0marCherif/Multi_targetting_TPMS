tensor_data.pl
The dictionary in this file contains tensorized features for reviewers and papers, as well as pairwise TPMS and bids scores. 

The keys are: "r_subject" (reviewer's subject area vector, m-by-#subjects), 
"p_subject" (paper's subject area vector, n-by-#subjects), 
"p_title" (paper title's bag-of-words vector, n-by-#words),
"tpms" (TPMS scores between pairs of reviewers and papers, m-by-n), 
"label" (bids scores between pairs of reviewers and papers, m-by-n).

Data dimensions: m = 2483, n = 2446, #subjects = 368, #words = 930


papers_dictionary.json
This file contains raw information about papers. 
Each entry is keyed by the paper's index (from 0 to n-1) and the value is a dictionary containing keys: 
["title", "abstract", "authors"].


reviewers_dictionary.json
This file contains raw information about reviewers. 
Each entry is keyed by the reviewer's index (from 0 to m-1) and the value is a dictionary containing keys: ["name", "papers"]. 
The value for the key "papers" is a list of papers that the reviewer has authored. 
Similar to papers_dictionary.json, 
each paper here is represented by a dictionary containing keys: ["title", "abstract", "authors"].