# Macleay-Museum-Insects
Data science exploration into the distribution and characteristics of Macleay Museum insects with a focus on butterflies. The final report is created through knitting the code base in RStudio.
To view two phylogenetic figures in the report, `insects_report.html` must be opened from the same directory as `phylowidget.html` and `phylowidget_lep.html`.

## Data dictionary
Many data sets have been used for this project. 

The data comes from small paper labels that are physically connected to each specimen. In entomology a specimen is usually pinned through the body with a metal pin. On this pin is sometimes attached a label. Each specimen is pinned into a container (generally a wooden drawer) with related species. Drawers in this dataset are represented by Fields A-C.  When more than one specimen of a single species was collected in a ‘collection event’ (unique time/place/collector) a single label was written, and all the specimens represented in the collection event were pinned in association with this label. Field G includes this information. 

The data set `ProvenanceOfEntomology.xlsx` has two main sheets. "List by species COMPLETE 2017" has the following fields:

|    Field   |    Name                                   |    Description                                    |    Format                |    Values                                   |    Notes                                                                                        |
|------------|-------------------------------------------|---------------------------------------------------|--------------------------|---------------------------------------------|-------------------------------------------------------------------------------------------------|
|    A       |    Level 1                                |    Identifier for storage                         |    integer and text      |    ‘111’ or ‘Historic’                      |    Relevant to museum                                                                           |
|    B       |    Level 2                                |    Identifier for storage                         |    integer               |    1-97; A, B, Lamberton Box, ...            |    Relevant to museum; not all numbers between 1 and 97 used                                    |
|    C       |    Level 3                                |    Identifier for storage                         |    integer               |    1-76                                     |    Relevant to museum; not all numbers between 1 and 76 used                                    |
|    E       |    Name in label                          |    Identification when known                      |    text                  |    Genus, species, sub-species, author      |    Sp means an animal of this species;                                                          |
|    F       |    Locality on label                      |    Geographical place where animal collected      |    text                  |    City, country, continent, not known      |    Great variety in this Field. It is the one that I would like to pivot   the research on.     |
|    G       |    Number of specimens under this label   |    Animals with a shared E and F                  |    integer               |    1-60                                     |    Where blank, 1 specimen is assumed to be total number                                        |
|    H       |    Biological Order                       |    Highest level of categorisation                |    text                  |    Single name                              |    Stands for E when identification not known                                                   |
|    I       |    Biological Family                      |    Level of categorisation                        |    text                  |    Single name                              |    Could be used to simplify data set                                                           |

The "By location" sheet has important information in the "Number of specimens" column relating to the amount of specimens in a collection event.

`taxonomyData.csv` contains taxonomy data for each species.

`locationData.csv` contains location data for each location.

`temp3.csv` contains temperature data in Kelvin for a particular subset of the final data set formed in the code.

`replacement.csv` contains location names and their manually replaced value.
