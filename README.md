# retraction-indexing-agreement

This is a longitudinal project that assesses the retraction indexing of publications across bibliographic databases.

## [Tag v2.1.3](2.1.3) [Latest Release] 
**Cite code v2.1.3 as:**
- Salami, M. O., McCumber, C., & Williams, D. (2026). Retraction indexing agreement: Fall 2026 Preprint Final Code (2.1.3) [Python]. Zenodo. https://doi.org/10.5281/zenodo.24382523

**Cite preprint as:**
- Salami, M. O., McCumber, C., Schneider, J., & Williams, D. (2026). Analyzing the consistency of retraction indexing. MetaArXiv. TODO:DOI

**Cite data as:**
- Salami, M. O. & McCumber, C. (2026). Redacted dataset for Analyzing the Consistency of Retraction Indexing (Version 3) [Dataset]. University of Illinois Urbana-Champaign Databank. TODO:DOI

 **Code contributors:**
 - Jou Lee (ORCID: 0000-0001-8927-0370) prototyped an earlier version [v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0) pipeline for the [STI2023 Paper](https://doi.org/10.55835/6441e5cae04dbe5586d06a5f).

### Description
This Jupyter notebook is used for the assessment of retraction indexing agreement among data sources: BCI, BIOABS, CCC, Compendex, GEOBASE, MEDLINE, PubMed, Retraction Watch, Scopus, and Web of Science Core. 

Starting with v2.1.3 we drop Crossref from our analysis, to avoid using a large number of known retraction notices.
Our original Crossref data collection on 2024-07-03 collected DOIs for retraction notices whereas we intended to collect DOIs for retracted publications. In v2.1.3, Steps 1-5 remain unchanged; after Steps 1-5 have been run, we run Drop_Crossref; the results become the input for Step 6 and Step 7. 

v2.0.3 contains additional visualizations and a correction to a visualization compared to v2.0.2. 

v2.0.2 and later code releases remove items from Retraction Watch that are not in their "Retraction" category. Our previous code unintentionally included non-retracted items in analysis because Retraction Watch categorizes items as "Expression of concern", "Correction", or "Reinstatement" as well as "Retraction” in their publicly available Crossref data. We since added code to filter out these non-retracted items.

**Setup**

Follow these steps to set up the code:
1. Install the proper version of Jupyter notebook (our version: 6.4.11).
2. Install the standard Python libraries: ast, collections, datetime, json, os, re, time, and unicodedata.
3. Install third-party packages: tqdm, pandas, requests, seaborn, matplotlib, numpy, and yake and any packages listed in requirements.txt
4. Create configuration file (config.json). Insert your email and API keys for Elsevier databases (Compendex, GEOBASE, and Scopus) and Web of Science Core. Institutional token (insttoken) will be required for Elsevier if you are running the code.

**Run the Code**
1. Download the "retraction-indexing-agreement" folder or clone the web URL: https://github.com/infoqualitylab/retraction-indexing-agreement.git
2. Set your working directory to  `retraction-indexing-agreement/core` and create data and result subfolders. Create subfolders for data as shown below.
3. Run the code in the `retraction-indexing-agreement/drop_crossref/` subfolder, starting with Step1 and continuing through Step5.
4. Set your working directory to  `retraction-indexing-agreement/drop_crossref/` and create result, coverednotindexed_old, and retractionyear_old subfolders.
5. Copy the contents of `retraction-indexing-agreement/core/data/coverednotindexed` to `retraction-indexing-agreement/drop_crossref/coverednotindexed_old`. Shown below.
6. Copy the relevant files of the subfolders of `retraction-indexing-agreement/core/data/` to `retraction-indexing-agreement/drop_crossref/retractionyear_old`. Shown below.
7. Copy `retraction-indexing-agreement/core/data/unionlist/unionlist_completed_2024-07-09.csv` to `retraction-indexing-agreement/drop_crossref/unionlist_completed_old_2024-07-09.csv`. Shown below.
8. Run the `Drop_Crossref.ipynb` notebook to filter out Crossref data
9. Run the cells in the notebook accordingly.
10. Run the Step6 and Step7 notebooks to generate figures and results.
11. Run the cells in the notebook accordingly.

Final repository structure. Items surrounded by "<>" are created by running the `core` part of the project and copying data over to `drop_crossref`.
```
retraction-indexing-agreement/
|
├── core/
│   ├── config.json
│   ├── data/
│   │   ├── coverednotindexed/
│   │   ├── crossref/
│   │   ├── engineeringvillage/ 
│   │   ├── journal/ 
│   │   ├── pubmed/
│   │   ├── retractionwatch/
│   │   ├── scopus/
│   │   ├── unionlist/
│   │   ├── webofscience/
│   ├── src/
│   │   ├── Step1_DataCollectionFromSources_and_UnionList.ipynb
│   │   ├── Step2_HandlingItemsWithoutDOI_ButWithPubMedID.ipynb 
│   │   ├── Step3_DataCollection_of_Indexedasretracted_and_Coveredin.ipynb
│   │   ├── Step4_DataCollection_of_RetractionYear.ipynb
│   │   ├── Step5_JournalFieldClassification.ipynb
├── drop_crossref/
│   ├── coverednotindexed_old/
│   │   ├── <contents of retraction-indexing-agreement/core/data/coverednotindexed>
│   ├── result/
│   ├── retractionyear_old/
│   │   ├── <bci_retractionyear_2024-07-03.csv>
│   │   ├── <bioabs_retractionyear_2024-07-03.csv>
│   │   ├── <ccc_retractionyear_2024-07-03.csv>
│   │   ├── <crossref_retractionyear_2024-07-03.csv>
│   │   ├── <pubmed_retractionyear_2024-07-03.csv>
│   │   ├── <retractionwatch_2024-07-03.csv>
│   │   ├── <webofsciencecore_retractionyear_2024-07-03.csv>
│   ├── Drop_Crossref.ipynb
│   ├── Step6_ DataAnalysis.ipynb
│   ├── Step7_ OtherInPaperAnalysis.ipynb
│   ├── <unionlist_completed_old_2024-07-09.csv>
```

## [Tag v2.0.3](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v2.0.3)
**Cite code v2.0.3 as:**
- Salami, M. O. & McCumber, C. (2026). Retraction indexing agreement: Summer 2026 Preprint Final Code (2.0.3) [Python]. Zenodo. https://doi.org/10.5281/zenodo.21724316

**Cite preprint as:**
- Salami, M. O., McCumber, C., & Schneider, J. (2026). Analyzing the consistency of retraction indexing. MetaArXiv. https://doi.org/10.31222/osf.io/gvfk5_v4

**Cite data as:**
- Salami, M. O. & McCumber, C. (2026). Redacted dataset for Analyzing the Consistency of Retraction Indexing (Version 2) [Dataset]. University of Illinois Urbana-Champaign Databank. https://doi.org/10.13012/B2IDB-8114408_V2 

**Code contributors:**
- Jou Lee (ORCID: 0000-0001-8927-0370) prototyped an earlier version [v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0) pipeline for the [STI2023 Paper](https://doi.org/10.55835/6441e5cae04dbe5586d06a5f).

## [Tag v2.0.2](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v2.0.2)
**Cite code v2.0.2 as:**
- Salami, M. O. & McCumber, C. (2026). Retraction indexing agreement: Summer 2026 Preprint Final Code (2.0.2) [Python]. Zenodo. https://doi.org/10.5281/zenodo.21250735

**Cite preprint as:**
- Salami, M. O., McCumber, C., & Schneider, J. (2026). Analyzing the consistency of retraction indexing. MetaArXiv. https://doi.org/10.31222/osf.io/gvfk5_v3

**Cite data as:**
- Salami, M. O. & McCumber, C. (2026). Redacted dataset for Analyzing the Consistency of Retraction Indexing (Version 2) [Dataset]. University of Illinois Urbana-Champaign Databank. https://doi.org/10.13012/B2IDB-8114408_V2 

**Code contributors:**
- Jou Lee (ORCID: 0000-0001-8927-0370) prototyped an earlier version [v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0) pipeline for the [STI2023 Paper](https://doi.org/10.55835/6441e5cae04dbe5586d06a5f).

## [Tag v2.0.1](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v2.0.1)
**Cite code v2.0.1 as:**
- Salami, M. O. & McCumber, C. (2025). Retraction indexing agreement: Fall 2025 Preprint Final Code (2.0.1) [Python]. Zenodo. https://doi.org/10.5281/zenodo.17518295

**Cite preprint as:**
- Salami, M. O., McCumber, C., & Schneider, J. (2025). Analyzing the consistency of retraction indexing. MetaArXiv. https://doi.org/10.31222/osf.io/gvfk5_v2

**Cite data as:**
- Salami, M. O. & McCumber, C. (2024). Redacted dataset for Analyzing the Consistency of Retraction Indexing (Version 1) [Dataset]. University of Illinois Urbana-Champaign Databank. https://doi.org/10.13012/B2IDB-8114408_V1 

**Code contributors:**
- Jou Lee (ORCID: 0000-0001-8927-0370) prototyped an earlier version [v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0) pipeline for the [STI2023 Paper](https://doi.org/10.55835/6441e5cae04dbe5586d06a5f).

## [Tag v2.0.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v2.0.0)
**Cite code v2.0.0 as:**
- Salami, M.O & McCumber, C. (2024). Retraction indexing agreement: 2024 Preprint Final Code (2.0.0) [Python]. Zenodo. https://doi.org/10.5281/zenodo.14183542
- (part of https://doi.org/10.5281/zenodo.7851297)

**Code contributors:**
- Jou Lee (ORCID: 0000-0001-8927-0370) prototyped an earlier version [v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0) pipeline for the [STI2023 Paper](https://doi.org/10.55835/6441e5cae04dbe5586d06a5f).

**Preprint:**
- Salami, M. O., McCumber, C., & Schneider, J. (2024). Analyzing the consistency of retraction indexing. MetaArXiv. https://doi.org/10.31222/osf.io/gvfk5

**Dataset**:
- Salami, M. O. & McCumber, C. (2024). _Redacted Dataset for Analyzing the Consistency of Retraction Indexing_ (Version 1) [Dataset]. University of Illinois at Urbana-Champaign Databank. https://doi.org/10.13012/B2IDB-8114408_V1

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
- Salami, M. O. & McCumber, C. (2024). _Dataset for Reassessment of the agreement in retraction indexing across 4 multidisciplinary sources: Crossref, Retraction Watch, Scopus, and Web of Science_ (Version 1) [Dataset]. University of Illinois at Urbana-Champaign Databank. https://doi.org/10.13012/B2IDB-8457537_V1


## [Tag v1.1.0](https://github.com/infoqualitylab/retraction-indexing-agreement/tree/v1.1.0)
**Cite code v1.1.0 as:** <br>
- Jou (Laura) Lee (2023). Code for Assessing the agreement in retraction indexing across 4 multidisciplinary sources: Crossref, Retraction Watch, Scopus, and Web of Science <br>

**Code authors:**
- Jou Lee (0000-0001-8927-0370) with contributions from Malik Salami (0000-0002-2329-5660) and Tzu-Kun Hsiao (0000-0002-2314-5777).<br>

**Paper:**
- Schneider, J., Lee, J., Zheng, H., & Salami, M. O. (2023, September). _Assessing the agreement in retraction indexing across 4 multidisciplinary sources: Crossref, Retraction Watch, Scopus, and Web of Science_ [Conference paper]. In 27th International Conference on Science, Technology and Innovation Indicators (STI 2023). International Conference on Science, Technology and Innovation Indicators. http://doi.org/10.55835/6441e5cae04dbe5586d06a5f
