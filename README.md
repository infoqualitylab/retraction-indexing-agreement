# retraction-indexing-agreement

This is a longitudinal project that assesses the retraction indexing of publications across bibliographic databases.

## [Tag v2.0.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v2.0.0) [Latest Release] 

### Description
This Jupyter notebook is used for the assessment of retraction indexing agreement among data sources: BCI, BIOABS, CCC, Compendex, Crossref, GEOBASE, MEDLINE, PubMed, Retraction Watch, Scopus, and Web of Science Core. 

**Setup**
1. Follow these steps to set up the code:
2. Install the proper version of Jupyter notebook (our version: 6.4.11).
3. Install the standard Python libraries: ast, collections, datetime, json, os, re, time, and unicodedata.
4. Install third-party packages: tqdm, pandas, requests, seaborn, matplotlib, numpy, and yake.
5. Create configuration file (config.json). Insert your email and API keys for Elsevier databases(Compendex, GEOBASE, and Scopus) and Web of Science Core. Institutional token (insttoken) will be required for Elsevier if you are running the code.

**Run the Code**
1. Download the "retraction-indexing-agreement" folder or clone the web URL: https://github.com/infoqualitylab/retraction-indexing-agreement.git
2. Set your working directory to  “retraction-indexing-agreement” and create data, result, src subfolders. Create subfolders for data as shown below.
3. Run the code in the src subfolder.

```
retraction-indexing-agreement/
|
├── config.json
├── data/
│   ├── coverednotindexed/
│   ├── crossref/
│   ├── engineeringvillage/ 
│   ├── journal/ 
│   ├── pubmed/
│   ├── retractionwatch/
│   ├── scopus/
│   ├── unionlist/
│   ├── webofscience/
├── result
├── src/
│   ├── Step1_DataCollectionFromSources_and_UnionList.ipynb
│   ├── Step2_HandlingItemsWithoutDOI_ButWithPubMedID.ipynb 
│   ├── Step3_DataCollection_of_Indexedasretracted_and_Coveredin.ipynb
│   ├── Step4_DataCollection_of_RetractionYear.ipynb
│   ├── Step5_JournalFieldClassification.ipynb
│   ├── Step6_ DataAnalysis
│   ├── Step7_ OtherInPaperAnalysis.ipynb
```

3. Enter your email, API Keys and insttoken into the config.json file
4. Run the files in the src files
5. Install the libraries as mentioned above
6. Run the cells accordingly 

**Cite code v2.0.0 as:**
- Salami, M.O & McCumber, C. (2024). Retraction indexing agreement: QSS Paper Final Code (2.0.0) [Python]. Zenodo. https://doi.org/10.5281/zenodo.7851297 (or use the more specific Zenodo v2.0.0 DOI being generated)

 **Code contributors:**
 - Jou Lee (ORCID: 0000-0001-8927-0370) prototyped an earlier version [v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0) pipeline for the [STI2023 Paper](https://doi.org/10.55835/6441e5cae04dbe5586d06a5f).

**Paper:**
- Salami, M. O., McCumber, C., & Schneider, J. (2024). Analyzing the Consistency of Retraction Indexing. Under review. QSS PAPER DOI GOES HERE 

**Dataset**:
- Salami, M. O. & McCumber, C. (2024). _Dataset for Analyzing the Consistency of Retraction_ (Version 1) [Data set]. University of Illinois at Urbana-Champaign Databank. QSS DATABANK DOI GOES HERE

## [Tag v1.2.1](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.2.1)
**Cite code v1.2.1 as:**
- Salami, M.O. & McCumber, C. (2024). Retraction indexing agreement: ASIS&T MET-STI2024 Paper Final Code (1.2.1) [Python]. Zenodo. https://doi.org/10.5281/zenodo.14052823
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
