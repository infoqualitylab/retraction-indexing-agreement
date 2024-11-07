# retraction-indexing-agreement

This is a longitudinal project that assesses the retraction indexing of publications across bibliographic databases.

## [Tag v1.2.1](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.2.1) [Latest Release] 

### Description
This Jupyter notebook is used for the reassessment of the union list of Schneider et al. (2023) after a 15-month period.

**Setup**
1. Follow these steps to set up the code:
2. Install the proper version of Jupyter notebook (our version: 6.4.11)
3. Install the standard Python libraries: ast, collections, datetime, json, os, re, time, and unicodedata 
4. Install third-party packages: tqdm, pandas, requests, seaborn, matplotlib and numpy
5. Create configuration file (config.json). Insert your email and API keys for Elsevier (Scopus)  and Web of Science. Institutional token (insttoken) will be required for Elsevier if you are running the code

**Run the Code**
1. Download “retraction-indexing-agreement” folder or clone the web URL: https://github.com/infoqualitylab/retraction-indexing-agreement.git
2. Set your working directory to  “retraction-indexing-agreement” and create ‘dataset’ and ‘result’ subfolders. Create subfolders for dataset as shown below. Add the April 2023 union list "unionlist_completed_2023-09-03-crws-ressess.csv" in the sti2023 subfolder.

```
retraction-indexing-agreement/
|
├── config.json
├── dataset/
│   ├── sti2023/ 
│   ├── coverednotindexed/
│   ├── crossref/
│   ├── retractionwatch/
│   ├── scopus/
├── MET-STI2024_Reassessment_of_retraction_indexing_agreement.ipynb
├── result
```

3. Enter your email, API Keys and insttoken into the config.json file
4. Run “MET-STI2024_Reassessment_of_retraction_indexing_agreement”
5. Install the libraries as mentioned above
6. Run the cells accordingly 

**Cite code v1.2.1 as:**
- Salami, M.O. & McCumber, C. (2024). Retraction indexing agreement: ASIS&T MET-STI2024 Paper Final Code (1.2.1) [Python]. Zenodo. https://doi.org/10.5281/zenodo.7851297 (or use the more specific Zenodo v1.2.1 DOI being generating)

 **Code contributors:**
 - Jou Lee (ORCID: 0000-0001-8927-0370) prototyped an earlier version [v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0) pipeline for the [STI2023 Paper](https://doi.org/10.55835/6441e5cae04dbe5586d06a5f).


**Paper:**
- Salami, M. O., McCumber, C., & Schneider, J. (2024, November 6-13). Reassessment of the agreement in retraction indexing across 4 multidisciplinary sources: Crossref, Retraction Watch, Scopus, and Web of Science. _ASIS&T MET-STI 2024: Workshop on Informetric, Scientometric and Scientific and Technical Information Research_. https://doi.org/10.5281/zenodo.14004526 

**Slides**:
- Salami, M. O., McCumber, C., & Schneider, J. (2024, November 13). _Reassessment of the agreement in retraction indexing across 4 multidisciplinary sources: Crossref, Retraction Watch, Scopus, and Web of Science_ [Conference presentation]. ASIS&T MET-STI 2024: Workshop on Informetric, Scientometric and Scientific and Technical Information Research, virtual. https://hdl.handle.net/2142/124990 

**Dataset**:
- Salami, M. O. & McCumber, C. (2024). _Dataset for Reassessment of the agreement in retraction indexing across 4 multidisciplinary sources: Crossref, Retraction Watch, Scopus, and Web of Science_ (Version 1) [Data set]. University of Illinois at Urbana-Champaign Databank. https://doi.org/10.13012/B2IDB-8457537_V1


## [Tag v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0)
**Cite code v1.1.0 as:** <br>
- Jou (Laura) Lee (2023). Code for Assessing the agreement in retraction indexing across 4 multidisciplinary sources: Crossref, Retraction Watch, Scopus, and Web of Science <br>

 **Code authors:**
 - Jou Lee (0000-0001-8927-0370) with contributions from Malik Salami (0000-0002-2329-5660) and Tzu-Kun Hsiao (0000-0002-2314-5777).<br>

**Paper:**
- Schneider, J., Lee, J., Zheng, H., & Salami, M. O. (2023, September). _Assessing the agreement in retraction indexing across 4 multidisciplinary sources: Crossref, Retraction Watch, Scopus, and Web of Science_ [Conference paper]. In 27th International Conference on Science, Technology and Innovation Indicators (STI 2023). International Conference on Science, Technology and Innovation Indicators. http://doi.org/10.55835/6441e5cae04dbe5586d06a5f
