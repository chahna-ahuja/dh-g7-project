Add column wise grel_scripts as a markdown file so grel_scripts will contain:
alephsystem_column (markdown will say mostly unchanged, remove duplicates process)
dom_id (markdown will say mostly unchanged, remove duplicates process)
author_column, (author workflow- written by chahna and liangyu, see report for detailed steps
  - write this has two versions to keep authenticiy of our workflow 
  - version 1: chahna's version
  - version 2: liangyu's version 
authorwikidata_column (wikidata reconcilation workflow- written by liangyu, see report for detailed steps)
title_column (title workflow- written by chahna, again this has two version) 
  - version 1: chahna's exact workflow
  - version 2: liangyu's version from comments in notion's title workflow section
edition_column (edition workflow just format puncutations) 
series_column (series workflow just format puncutations)
subject_column  (subject workflow just format puncutations)
imprint_column, (imprint workflow = written by chahna)
otherauthors_column (otherauthors workflow- written by chahna)

each of these markdown files should have grel code and process of cleaning in detail (copy+paste process from notion + use code block in markdown for code) 

how to add codeblock for GREL 

```javascript
// GREL example: lowecase columns
value.toLowercase().trim()

For, json folder- please add json history from OpenRefine

*Delete the section above divider after you're done adding these scripts, Xinran! (including the divider)*
|-----|-------------------------|-----------|------------------------------------------|------------------------------------------------------------------------------------------------|

### Workflow Process and Scripts
- The **grel_scripts** folder contains each column's detailed workflow process, GREL scripts and its versions, written by the team members: Chahna Ahuja, Liangyu Gan, Xinran Liu. 
- The table below summarizes the data cleaning and transformation process as operated on each column. 

| No. | Name                    | Status    | Comments                                  | Instance                                                                                       |
|-----|-------------------------|-----------|------------------------------------------|------------------------------------------------------------------------------------------------|
| 1   | aleph system no.        | Unchanged | Unique identifier                         | *014810954*                                                                                   |
| 2   | DOM id                  | Unchanged | Unique identifier                         | *lsidyv31b63e2f*                                                                               |
| 3   | author (o)              | Unchanged | Original personal author column           | *foote, samuel. 1720-1777*                                                                    |
| 4   | author (n)              | Modified  | Cleaned version of author (o)             | *foote, samuel*                                                                                |
| 5   | author_wikidata_url     | New       | Wikidata URL from author (n)              | *https://www.wikidata.org/wiki/Q766758*                                                       |
| 6   | author_wikidata_id      | New       | Wikidata identifier from author (n)       | *Q766758*                                                                                      |
| 7   | title (o)               | Unchanged | Original title column                      | *[the nabob; a comedy in three acts [and in prose]. ... published by mr.colman.] [electronic resource]* |
| 8   | title (n)               | Modified  | Cleaned and standardized title            | *the nabob; a comedy in three acts*                                                           |
| 9   | metadata                | New       | Supplementary title information           | *[and in prose]. published by mr.colman....*                                                  |
| 10  | edition                 | Modified  | Standardized edition data                  | *another edition*                                                                              |
| 11  | other authors (o)       | Unchanged | Original secondary authors                 | *colman, george, the elder.*                                                                  |
| 12  | other authors (n)       | Modified  | Cleaned secondary authors                  | *colman, george, the elder*                                                                   |
| 13  | series                  | Modified  | Standardized series information           | **NULL**                                                                                        |
| 14  | subject                 | Modified  | Standardized subject terms                 | *english drama. british drama india*                                                          |
| 15  | imprint (o)             | Unchanged | Original imprint column                     | *london, 1795.*                                                                               |
| 16  | p year                  | New       | Publishing year extracted from imprint    | *1795*                                                                                         |
| 17  | p location              | New       | Publishing location extracted from imprint| *london*                                                                                       |
| 18  | p name                  | New       | Publisher name extracted from imprint     | **NULL**                                                                                        |
| 19  | type                    | Unchanged | `Comedy', `Tragedy' and `Play' as types   | *comedy*                                                                                       |
### Json History

The **json_history** contains json history for each subdataset, cleaned by different members:
- Comedy: Chahna Ahuja
- Tragedy: Xinran Liu
- Play: Liangyu Gan
