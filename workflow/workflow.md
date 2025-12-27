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
