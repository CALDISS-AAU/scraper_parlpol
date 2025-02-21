## Log for development of DKParl scraper

#### 2022-12-05
- Develop first version of scraper for downloading resumes/minutes from Danish Parliament (https://www.ft.dk/da/dokumenter/dokumentlister/referater)
    - `modules/dkparl_scraperfunctions.py`
- Downloading all resumes from 2007-10-02 to 2022-12-05 as HTML using script `dkparl_scrape_files.py`
- NOTE: Resumes before 2007-10-02 are stored as pdf - *need download function for pdf files*


#### 2022-12-13
- Starting development on parser for html files

#### 2022-12-16
- Parsing html files 2007-2022
- Failed added to txt file in data directory
- NOTE: *Add filename to data*

#### 2022-12-19
- Validating data:
    - about 490 with mismatch between agenda length and item length - "Spørgsmål til ministeren" a different format.
- Updating parser:
    - Adding filename to data
    - Adding "meddelelser fra Formanden"
    - Separating items based on "ShortTitle" instead of ItemNo (fits format "Spørgsmål til ministeren" as well)
- Validating after update:
    - 16 with mismatch between agenda length and item length
    - 7 failed



#### 2025-01-2024
Changes made:

- Updated the dkparl_scrape_files.py file with new entry dates 
- Enabled SSL check in dkparl_scraperfunctions.py
- Configured the file_out_p  var in dkparl_parse-files.py
