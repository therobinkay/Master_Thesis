# Master_Thesis

## other_data.zip
Contains *citationBara.csv*, *doipacs.csv*, *rhom.csv*, *cen.csv*

#### citationBara.csv
Initial dataset describing the citation relationship. Contains:
- **citing_doi**:   DOI of the paper that cites
- **cited_doi**:    DOI of the paper that is cited

#### doipacs.csv
Identifies which PACS each paper belongs to. Contains:
- **doi**:          DOI of the paper
- **0**:            True = paper is in PACS 00
- **1**:            True = paper is in PACS 10
- **2**:            True = paper is in PACS 20
- **3**:            True = paper is in PACS 30
- **4**:            True = paper is in PACS 40
- **5**:            True = paper is in PACS 50
- **6**:            True = paper is in PACS 60
- **7**:            True = paper is in PACS 70
- **8**:            True = paper is in PACS 80
- **9**:            True = paper is in PACS 90
- **exceptions**:   any unnatural values in 'PACS' columns

#### rhom.csv
Used for merging a new DataFrame (only) for homophily analysis. Contains:
- **paper**:        DOI of the paper
- **gender**:       gender of the primary author
- **year**:         publication year of the paper

#### cen.csv
Used for finding PageRank centrality for all papers. Contains (unexplained data columns are identical to *citationBara.csv*):
- **citing_doi**
- **citing_gender**:  gender of the primary author of the citing paper
- **cited_doi**
- **cited_gender**:   gender of the primary author of the cited paper

## data.zip
Contains *data.csv*:

#### data.csv
A master DataFrame used for the first part of Thesis (Chapter 3, 4). Contains:
- **doi**:          DOI of the paper
- **id**:           id of the participating author
- **gender**:       gender of the participating author
- **order**:        position listed of the participating author
- **numAuthor**:    number of participating authors in the paper
- **is_last**:      True = the author is the last author of the paper
- **is_alpha**:     True = the paper lists authors alphabetically
- **year**:         publication year of the paper
- **articleType**:  type of the paper
- **journal**:      journal of the paper

## cdata.zip
Contains *cdata.csv*:

#### cdata.csv
A master DataFrame used for the second part of Thesis (Chapter 5). Divided into two data column sections:
- **citing...**:    information about citing paper
- **cited...**:     information about cited paper

Contains (unexplained data columns are identical to *data.csv* and *doipacs.csv*):
- **doi**
- **id**
- **gender**
- **order**
- **numAuthor**
- **is_last**
- **is_alpha**
- **year**
- **articleType**
- **journal**
- **0**
- **1**
- **2**
- **3**
- **4**
- **5**
- **6**
- **7**
- **8**
- **9**
- **exceptions**

## homophily_PACS.zip
Used for further analysis of homophily, distinguished by subfield (See Thesis Chapter 5 for more details). Contains *hom0.csv*, *hom1.csv*, *hom2.csv*, *hom3.csv*, *hom4.csv*, *hom5.csv*, *hom6.csv*, *hom7.csv*, *hom8.csv*, *hom9.csv*.

Each file contains:
- **paper1**:     DOI of the first article of the pair
- **gender1**:    gender of the primary author of the first article of the pair
- **year1**:      publication year of the first article of the pair
- **paper2**:     DOI of the second article of the pair
- **gender2**:    gender of the primary author of the second article of the pair
- **year2**:      publication year of the second article of the pair
- **qval**:       q-value of the pair
- **k**:          True = the pair has a citation relationship between them

## Analysis1.ipynb
Includes the following Analyses:
- Author Order Analysis
- Productivity Analysis
- Dropout Author Analysis
- Frequently Cited Paper (Degree Centrality) Analysis
- Self-citation Analysis
- PageRank Centrality Analysis

## Analysis2.ipynb
Includes the following Analyses:
- Similarity (Homophily) Analysis
- Similarity Degree Centrality Difference Analysis
- Similarity PageRank Centrality Difference Analysis
