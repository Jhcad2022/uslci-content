# Section 2: How do I publish my data in the USLCI?


[**_Return to TOC_**](./00-sub-handbook-landing.md)


This page is part of the [USLCI Submission Handbook](00-sub-handbook-landing.md).  The purpose of this page is to help you, the Data Provider, understand the process for publishing life cycle inventory (LCI) data in the [U.S. Life Cycle Inventory Database (USLCI)](https://uslci.lcacommons.gov/uslci/search).  If you are looking for information to help you decide if publishing your data in the USLCI fits your publication goals, please see [Section 1: Should I publish my data in the US LCI?](./01-should-i-publish-in-the-uslci.md).  You can also find a list of frequently asked questions [here](03-frequently-asked-questions.md).

This page is divided into the following subsections.
1. [**Working with NREL**](#working-with-nrel)
2. [**Overview of the Digital Curation process**](#overview-digital-curation)
    * [_Appraisal_](#appraisal)
    * [_Ingest & Onboarding_](#ingest-and-onboarding)
    * [_Review_](#review)
    * [_Publication_](#publication)
    * [_Preservation_](#preservation)
3. [**Guidance on Data Compilation in openLCA**](#guidance-data-compilation-openlca)
4. [**Metadata Guidance Tables**](#metadata-guidance-tables)


<a id="working-with-nrel"></a>
## Working with NREL
The data publication process is a collaborative effort between you (i.e., the Data Provider) and the NREL. Practically speaking, that means you will be working closely with one of NREL's LCI Data Curators throughout the publication process.

The Data Curator's role is to guide you through the publication process. This person is trained in LCI data curation and can help you troubleshoot technical issues related to exporting and/or importing LCI data formats, completing dataset metadata fields, and using the openLCA platform.

Your role in the publication process is to transform your raw LCI data into a product that is ready for publication in the USLCI Database. ‘Transform’ means to put your data into the USLCI Database's data format and pair your data with robust metadata so that your data users understand how to properly interpret and apply your data.

The documentation, [metadata guidance](#metadata-guidance-tables), and [resources](./04-resources/04-resources.md) in this Data Submission Guide will be essential resources in that process.

The International Organization for Standardization (ISO) specifies a framework for archival concepts necessary for long-term digital information preservation and access in [ISO 14721:2012](https://www.iso.org/standard/57284.html). This framework designates the importance of provenance information such as the history of content information, custody, and change history.

<br>

![](https://github.com/uslci-admin/private-uslci-content/blob/dev/images/ISO%2014721%20OAIS%20-%20Graphic.png)
**_Open Archival Information System (OAIS) Preservation Description Information_**

<br>

To facilitate compliance with these standards, we use [GitHub](https://github.com/) as our principal project management and communication tool. This platform assists in the storage, handling, and migration of LCI data during the curation and publication process. GitHub contains robust features for version control, issues management, and team communication. Moreover, it makes it easy for the Data Provider to keep a local version of the data curation process and end product once the project is complete. Early in the publication process, the Data Curator will work with you to get you set up with one or more private data repositories on GitHub.

As mentioned in the [Data Formatting](./01-should-i-publish-in-the-uslci.md#data-formatting) section of this handbook, NREL uses [openLCA](http://www.openlca.org/download/) as its platform for receiving, reviewing, and publishing LCI data. [openLCA](https://www.openlca.org/) is a free, open source LCA software platform that can import data from many commercial LCA software applications including GaBi and SimaPro.


<a id="overview-digital-curation"></a>
## Overview of the Digital Curation Process

NREL uses a Digital Curation Process for receiving, reviewing, publishing, and preserving data and metadata submitted to the USLCI Database. The process is divided into five phases:

1. [Appraisal](#appraisal)  
2. [Ingest & Onboarding](#ingest-and-onboarding)  
3. [Review](#review)  
4. [Publication](#publication)  
5. [Preservation](#preservation)

Each of the five phases is discussed in detail below but a quick overview of the entire procedure for submitting data to the USLCI is as follows:

- [ ] Submit preliminary data sets
- [ ] Appraisal Meeting with NREL
- [ ] Acquire a [GitHub account](https://help.github.com/articles/signing-up-for-a-new-github-account/)
- [ ] Watch the first 1 minute and 15 seconds of [this video](https://www.youtube.com/watch?v=w3jLJU7DT5E) about GitHub
- [ ] Watch [this video](https://www.youtube.com/watch?v=TJlYiMp8FuY) about using GitHub’s ‘Issues’ feature (3 min)
- [ ] Download the openLCA software and install it on your computer
- [ ] Download the current [FLCAC Starter database](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-H.md) and [US LCI database version](https://github.com/uslci-admin/private-uslci-content/blob/dev/docs/release_info/release-downloads.md) and import into openLCA
- [ ] Kick-off Meeting with NREL
- [ ] Edit your unit processes/product system in openLCA
- [ ] Export ONLY your edited datasets as a zipped JSON-LD file and submit to NREL on GitHub
- [ ] Reconcile issues identified by NREL during the [Review](#review) Process
- [ ] Approve final version
- [ ] NREL publishes the dataset(s) in the USLCI
- [ ] NREL preserves the final dataset files


<a id="appraisal"></a>
### Appraisal
The objectives of the Appraisal phase are to:
  * Verify the fitness of your data for publication in the USLCI
  * If appropriate, develop a plan for the [Ingest](#ingest-and-onboarding) and [Review](#review) phases of the Digital Curation Process.

The Appraisal phase is composed of the following elements:
  * Preliminary data review by the Data Curator
  * (If appropriate) An Appraisal Meeting

The Appraisal phase begins by submitting your data to the USLCI Database Admin for preliminary review. EcoSpold (v1 and v2) and ILCD submissions generated by SimaPro, GaBi, ecoEditor, the ILCD editor, or any other editor are sufficient for the Appraisal phase. However, these file formats may not support required metadata fields. For this reason, the [Ingest & Onboarding](#ingest-and-onboarding) phase will guide you to reproduce your datasets in the required file format.

Following this review, a 30-60 minute Appraisal Meeting may be scheduled. This meeting is an opportunity to evaluate the data at a deeper level and, if appropriate, develop a plan Ingest & Onboarding and Review phases of the Digital Curation Process. The Appraisal Meeting results in one of two outcomes:

1. Data approved
2. Revise and resubmit



<a id="ingest-and-onboarding"></a>
### Ingest & Onboarding
The Ingest & Onboarding phase is concerned with entering a data submission into the USLCI Database's file management system and establishing norms of collaboration between the Data Provider and the Data Curator.

To begin this phase, a Kick-off Meeting is scheduled between you and NREL’s Data Curator. Before the Kick-off Meeting, you will be asked to [acquire a GitHub account](https://help.github.com/articles/signing-up-for-a-new-github-account/) (if not already a member), briefly familiarize yourself with the platform concepts, and obtain a few resources that will be used throughout the curation process.


The following is a list of pre-meeting activities to facilitate the data curation process:

- [ ]	Acquire a [GitHub account username](https://help.github.com/articles/signing-up-for-a-new-github-account/). The NREL Data Curator will invite you to collaborate on the repository(ies) created for the curation of your data.
- [ ]	Watch the first 1 minute and 15 seconds of [this video](https://www.youtube.com/watch?v=w3jLJU7DT5E) about GitHub.
- [ ]	Watch [this video](https://www.youtube.com/watch?v=TJlYiMp8FuY) about using GitHub’s ‘Issues’ feature (3 min).
- [ ]	Download the openLCA software and install it on your computer.
- [ ]	Download the current [FLCAC Starter database](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-H.md) and [US LCI database version](https://github.com/uslci-admin/private-uslci-content/blob/dev/docs/release_info/release-downloads.md) and import both into openLCA.
- [ ]	Review the use of the [US EPA’s data quality system](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-G.md) in openLCA.

Prior to the Kick-off Meeting, you will receive an invitation to the [NREL GitHub repository(ies)](https://github.com/uslci-admin) created expressly for the curation of your data.

[GitHub](https://github.com/) is a full-featured web application designed for managing projects with version control requirements (e.g., software development). For the data curation process, you will not need to utilize most of GitHub’s features. However, this platform’s issues tracker will be used to help the Data Curator identify, assign, track, and resolve issues that arise during the curation process. This tool will make the process more efficient and ensure that all pertinent correspondence is in a single location.

During the Kick-off Meeting, NREL’s Data Curator will guide you through using these resources, provide you with an overview of the curation process, and discuss your data in the context of the USLCI. Whether you have existing data formats you import into openLCA, or you compile them from scratch in openLCA, NREL’s Data Curator will guide you through the compilation of your data and supporting metadata in the openLCA software.

As mentioned in the [Expectations](./01-should-i-publish-in-the-uslci.md#expectations) section and the [Overview of the Digital Curation Process](#overview-digital-curation), the LCA Commons is structured upon the [openLCA](http://www.openlca.org/download/) database schema to facilitate compliance with [ISO 14048:2002](https://www.iso.org/standard/29872.html) – LCA Data Documentation Format standards. To minimize data formatting efforts and ensure all metadata elements persist throughout submission, unit process and product system datasets submitted to the LCA Commons should be edited in openLCA (see below the [Guidance on Data Compilation in openLCA](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/02-how-to-publish-in-the-uslci.md#gudance-on-data-compilation-in-openlca) section of this Chapter). If you are already using openLCA, discuss which version with the Data Curator during the Appraisal Meeting to ensure compatability. It may or may not be necessary for you to update to a newer software version. Once you edit your Unit Processes or product systems in openLCA, you may share them through your institutional GitHub repository hosted by NREL as exported [JSON-LD files](https://json-ld.org/).


<a id="review"></a>
### Review

Once the JSON-LD files are received by NREL, the Data Curator begins the Review phase of the data curation process. Upon culmination of the internal review, NREL will collaborate with you to reconcile issues identified in the internal dataset documentation review (i.e., metadata review). _It is important to note this process does not include a technical review of the inventory data._ Typically, the most significant tasks for publishing data in the US LCI are resolving the flow nomenclature and connectivity and completing the process metadata. This phase is specific to the dataset(s) being curated and NREL’s Data Curator will guide you through this process.

Name all original Unit Processes and intermediate (i.e., product) flows that you submit to NREL according to the ILCD naming convention (see [Guidance on Data Compilation in openLCA](#guidance-data-compilation-openlca). The name should reflect the process or activity as follows: base name; treatment, routes, standards; production type, location type; quantitative flow properties. If you have modified or customized a unit process from a commercial database, NREL requests that you submit the process named exactly as it is in the original process with an indication (i.e., in the comment field) that it is a modified version of the original. For example, the comment for the modified ecoinvent process _“carbon dioxide liquid, at plant/RER U”_ might read: _‘adapted to reflect US average electricity grid.’_

Elementary flow names must correspond directly to the impact method used in the Life Cycle Impact Assessment (LCIA). This protocol assures users that your dataset can connect your elementary flows to the associated LCIA method. Document LCIA methods used in the ‘Intended Application’ field of the Administrative Information tab in openLCA. If data being submitted have NOT been used in an LCIA, please use flows from the openLCA reference list. If you used SimaPro or GaBi modeling software and an impact method that is also provided for in the [openLCA suite of LCIA methods](https://www.openlca.org/download/), please run your inventory and impact results in openLCA and compare them to those obtained in SimaPro or GaBi to confirm that openLCA is reading flows correctly.

With these issues in mind, the general Review phase workflow is as follows:

1. **Flow nomenclature/connectivity**
  **_Small datasets (< 10 unit processes) are manually curated as described below:_**
    * NREL provides an Excel file that suggests one of the following options for each submitted flow:
      * _Replace the flow with a surrogate from the USLCI Database_
      * _Add the flow to the USLCI Database as a CUTOFF_
      * _Add the flow to the USLCI Database as a connected flow (e.g., the Quantitative Reference for the submitted unit processes)_
    * NREL updates the flows in openLCA based on the Excel file referenced above
    * You review and approve the flow substitutions
  * **_Large datasets (> 10 unit processes) are curated using a semi-automated process as described below:_**
    * NREL uses a custom Structured Query Language (SQL) script to generate an Excel file that suggests one or more of the following options for each submitted flow:
      * _Replace the flow with a surrogate from the USLCI Database_
      * _Add the flow to the USLCI Database as a CUTOFF_
      * _Add the flow to the USLCI Database as a connected flow (e.g. the Quantitative Reference for the submitted unit processes)_
    * You review the proposed list and recommend changes as appropriate
    * NREL uses the SQL script to update flows based on the Excel file referenced above; this script may also update metadata elements
2. **You use openLCA to manually update/insert metadata for each process** (See: [Metadata Guidance Tables](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/02-how-to-publish-in-the-uslci.md#metadata-guidance-tables))
3. **NREL reviews the metadata for completeness**

The Review phase can involve iterative communications via the Issues tracker on your NREL GitHub repository and often requires the most time in the data curation process. You must play an active role in this collaborative effort for this phase of the process to be completed.

<a id="publication"></a>
### Publication
Once your data have been reviewed and completed, the dataset(s) are ready for publication. NREL will publish the data to its repository on the [Federal LCA Commons Collaboration Server](https://www.lcacommons.gov/). The USLCI Database is updated with new and revised data on a quarterly basis. Thus, the publication timeline of your data depends on its size and when your [Ingest & Onboarding](#ingest-and-onboarding) phase begins. The timeframe is heavily dependent on the response times between you and NREL during the iterative communications of the [Review](#review) phase and how many processes are being submitted. 

The USLCI is updated with new and revised data on a quarterly basis:
  * March 31
  * June 30
  * September 30
  * December 31

<a id="preservation"></a>
### Preservation

NREL will preserve the final dataset files according to [ISO 14721](https://www.iso.org/standard/57284.html) standards for long-term digital information preservation (see: [Working with NREL](#working-with-nrel)). That is, the final dataset file versions are stabilized, checked for fixity (i.e., verifying no digital file corruption), and stored such that the original and published datasets and their supporting metadata are archived. Only the initial dataset submission and the version final dataset as published are archived. These datasets will be saved until the next update is submitted and published. Older datasets may not be saved in the Federal LCA Data Commons but NREL retains the older datasets on their servers. Updates to previously published datasets shall contain a relevant note in the [‘Intended Application’](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/field-conventions/admin-info.md#administrative-information) metadata field of the unit process Administrative Information. If a user needs an older dataset, they may access the archived [USLCI Database Downloads](https://github.com/uslci-admin/uslci-content/blob/dev/docs/release_info/release-downloads.md) or [contact NREL](https://www.nrel.gov/lci/contacts.html) for a copy.


<a id="guidance-data-compilation-openlca"></a>
## Gudance on Data Compilation in openLCA

The Formatting phase is concerned with entering your datasets into the openLCA software. To minimize data formatting efforts and ensure all metadata elements persist throughout submission, unit process and product system datasets submitted to the LCA Commons should be edited using this modelling application.

The navigation scheme in openLCA contains the following elements:

1. **Projects:** can be created to compare product system variants
2. **Product systems:** can be created to link processes into process networks (necessary to calculate inventory results and impact assessment)
3. **Processes:** production or modification of products, materials, or transformation of land; services
4. **Flows:** intermediate and elementary flows
5. **Indicators and parameters:** influence the LCIA and data quality definitions
    * **Impact assessment methods:** method suite and individual LCIA methods area available via openLCA but must be downloaded and imported for each database
    * **Social indicators:** same as LCIA methods; used for social LCA
    * **Global parameters** : where database parameters are created and defined; a default value and uncertainty values may be assigned
    * **Data quality systems:** database defaults have the ecoinvent data quality system; other data quality systems are available via openLCA but must be downloaded and imported for each database
6. **Background data:** includes definitions for objects that populate pull-down menus used in the processes and LCIA methods
    * **Flow properties** : properties of flows (e.g., length, mass, etc.)
    * **Unit groups:** groups of units (e.g., units of area include m2, ft2, sq.yd, etc.)
    * **Currencies:** cost can be assigned to flows and Life Cycle Costing (LCC) can be performed
    * **Actors:** people who have provided data or modified models
    * **Sources:** literature referenced; can contain URL references
    * **Locations:** provides geographic specificity; particularly, important for regionalized LCA
    



### Intermediate Flow Names
Intermediate flows are are either products or processes from the technosphere (i.e., not elementary flows). Detailed guidance on process and technosphere flow nomenclature is provided in [General Information Field Conventions](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/field-conventions/general-info.md#general-information)  in the Metadata Guidance and [ILCD Nomenclature Rules](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-D.md).


#### Product Names

Intermediate product flows are technosphere flows that are a product of one or more processes and have flowable names and flow properties. Technosphere or product flows are the result of a process (or processes) and flow as exchanges between processes (unlike elementary flows that flow as exchanges to and from environmental compartments). All intermediate product flow names should be decoupled from their associated activity flow names (i.e., process name) for transparency and clarity. That is, a product name should not contain metadata that is specific to the activity context such as the location or year. The intermediate product name should be generic to any activity context so as to avoid unnecessary duplication of product flow names. Likewise, product flow properties such as units, formulas, synonyms, infrastructural flow designation, etc. may be defined in the metadata and should also not be included in the flowable name.

#### Process Names

An intermediate process is an activity containing at least one intermediate product flow. Activities are exchanges containing at least one input flow and one output flow (i.e., defining a relationship between flows). The intermediate process flow name should reflect the product or service it represents; the product reference output is often given the same name as the process name; the naming conventions are as follows: Base name; treatment, routes, standards; production type, location type; quantitative flow properties. The base name is a general descriptive name of the process using technical language. The technical name should be given as it is used in the respective industry or toward their customers. 

Name all original data sets that you submit to USLCI according to the ILCD naming convention. The standards include qualitative information about the process in technical terms (see Rules 1-19 in [ILCD Nomenclature Rules](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-D.md) or the full [ILCD Nomenclature Handbook](https://eplca.jrc.ec.europa.eu/uploads/MANPROJ-PR-ILCD-Handbook-Nomenclature-and-other-conventions-first-edition-ISBN-fin-v1.0-E.pdf) for a list of potential descriptive terms). The quantitative process properties further specify information on process in technical quantitative term(s).

If you have modified or customized a unit process from a commercial database, you should submit the process named exactly as it is in the original process with an indication (i.e., in the comment field) that it is a modified version of the original. For example, the modified ecoinvent® process _“carbon dioxide liquid, at plant/RER U”_ might be renamed _"carbon dixodie liquid, at plant/US"_ and the comment might read: ‘adapted from ecoinvent to reflect US average electricity grid.’

To link processes in your datasets, use the exact nomenclature of the intermediate flow. If the process to be linked only exists in another database or FLCAC repository, the exact nomenclature used and the repository noted in the _‘Input Flow, Description’_ field. Processes from other databases (i.e., already existing outside the FLCAC) should not be submitted as datasets. Therefore, a technosphere flow that is not being submitted as a dataset and is not already in the USLCI or another FLCAC repository should be categorized in the _Technosphere Flows>CUTOFF Flows_ folder or a reasonable proxy from the USLCI or another FLCAC repository should be identified with a note in the ‘Input Flow, Description’ field regarding the flow origin (database and flow name).



### Elementary Flow Names
Elementary flows are data components of LCA data that describe common physical items that move from the technosphere into nature or vice versa. They are used in exchanges in life cycle inventory (LCI) data to represent these movements into and out of processes, and they are used in Life Cycle Impact Assessment (LCIA) methods to match inventory data with impact characterization factors. Hence, they serve a critical role in LCA modeling and are essential in achieving LCA data interoperability.

The US EPA has developed a master elementary flow list (the FEDEFL), which is available in CSV and openLCA schema JSON-LD formats, and provides resources to help with mappings. The current release version is available via the [FLCAC portal](https://www.lcacommons.gov/). The [FEDEFL wiki](https://github.com/USEPA/Federal-LCA-Commons-Elementary-Flow-List/wiki) provides guidance on converting an established flow list in a standard openLCA format to FEDEFL flows. Please see the US EPA report, The [Federal LCA Commons Elementary Flow List: Background, Approach, Description and Recommendations for Use](https://cfpub.epa.gov/si/si_public_record_Report.cfm?Lab=NRMRL&dirEntryId=347251) report for more information regarding the FEDEFL requirements and nomenclature.

Elementary flow names in LCI must correspond directly to the elementary flow names used in the LCIA method. Usage of the FEDEFL protocol for both LCI and LCIA datasets on the FLCAC ensures interoperability between these different types of datasets. NOTE: the USLCI Database is phasing out specific ambiguous elementary flows that should be avoided in data submission. Please see [Guidance on Avoiding Ambiguous Elementary Flows](https://github.com/uslci-admin/uslci-content/wiki/unmappable_flows) for a list of these flows and the issues with their presence in public LCI databases.

<br>


<a id="metadata-guidance-tables"></a>
## Metadata Guidance
As FLCAC interagency coordination increases, the new standard for data formats and documentation is being advanced. In order to move toward interoperability and transparency, FLCAC harmonization of digital data access and preservation will increase collaboration potential and the reviewability of the LCA data exchange process. These efforts will significantly reduce not only data acquisition costs but also computer- and human-based misinterpretation errors, and thus, data misuse. As such, and to be more aligned with international protocols for all newly developed data, the current FLCAC repository standardization is to strive for 100 percent metadata completion. 

The links below correspond to tables with the conventions for each field of the elements in the openLCA software. The tables are arranged by the field sections as displayed in the tabs of the openLCA process window views. Each field has guidance and examples recommended by NREL for completing the metadata for processes submitted to the USLCI Database. Some of these fields are mandatory (marked **'M'**), a few are automatically populated (marked **'A'**), and some are optional (marked **'O'**).

### Metadata Guidance Tables


Click the links below to see guidance for the fields of each of the openLCA tabs (i.e., conventions and examples). Each table has a link to return to this list or to the main guidelines table of contents:
#### [General Information Tab](./field-conventions/general-info.md)
- [General Information](./field-conventions/general-info.md#general-information)
- [Quantitative Reference](./field-conventions/general-info.md#quantitative-reference)
- [Time](./field-conventions/general-info.md#time)
- [Geography](./field-conventions/general-info.md#geography)
- [Technology](./field-conventions/general-info.md#technology)
- [Data Quality](./field-conventions/general-info.md#data-quality)
#### [Inputs Tab](./field-conventions/inputs.md)
#### [Outputs Tab](./field-conventions/outputs.md)
#### [Administrative Information Tab](./field-conventions/admin-info.md)
#### [Modeling and Validation Tab](./field-conventions/modeling-and-validation.md)
- [Modeling and Validation](./field-conventions/modeling-and-validation.md#modeling-and-validation)
- [Data Source Information](./field-conventions/modeling-and-validation.md#data-source-information)
- [Process Evaluation and Validation](./field-conventions/modeling-and-validation.md#process-evaluation-and-validation)
- [Sources](./field-conventions/modeling-and-validation.md#sources)
#### [Global Parameters Tab](./field-conventions/global-parameters.md)
- [General Information](./field-conventions/global-parameters.md#general-information)
- [Additional information](./field-conventions/global-parameters.md#additional-information)
#### [Process Parameters Tab](./field-conventions/process-parameters.md)
- [Input & Dependent Parameters](./field-conventions/process-parameters.md#input-and-dependent-parameters)
- [Additional Information](./field-conventions/process-parameters.md#additional-information)
#### [Allocation Tab](./field-conventions/allocation.md)
- [Physical & Economic Allocation](./field-conventions/allocation.md#physical-and-economic)
- [Causal Allocation](./field-conventions/allocation.md#causal)

<br>

**NOTE: Social aspects are not addressed in this handbook.**

<br><br>
The key sources for the guidance are the:

- _Federal LCA Commons (FLCAC) Data Submission Guidelines_
- _FLCAC Unit Process Template_
- _GreenDelta: Class Data Set Information_ ( [http://greendelta.github.io/olca-modules/olca-ilcd/apidocs/org/openlca/ilcd/flowproperties/DataSetInformation.html](http://greendelta.github.io/olca-modules/olca-ilcd/apidocs/org/openlca/ilcd/flowproperties/DataSetInformation.html))
- _ILCD Handbook: Nomenclature and other conventions_ ( [http://eplca.jrc.ec.europa.eu/uploads/MANPROJ-PR-ILCD-Handbook-Nomenclature-and-other-conventions-first-edition-ISBN-fin-v1.0-E.pdf](http://eplca.jrc.ec.europa.eu/uploads/MANPROJ-PR-ILCD-Handbook-Nomenclature-and-other-conventions-first-edition-ISBN-fin-v1.0-E.pdf))
- _Chalmers University Guide to LCA Data Documentation_ ( [http://cpmdatabase.cpm.chalmers.se/Document/CPM\_Report\_2003\_3\_Introduction\_and\_guide.pdf](http://cpmdatabase.cpm.chalmers.se/Document/CPM_Report_2003_3_Introduction_and_guide.pdf))
- _UNEP SETAC's Shonan Guidelines – Global Guidance Principles for LCA Databases: A Basis for Greener Processes. United Nations Environment Programme (UNEP) – Society of Environmental Toxicology and Chemistry (SETAC). © United Nations Environment Programme, 2011._ Accessed at: ( [https://www.lifecycleinitiative.org/wp-content/uploads/2012/12/2011%20-%20Global%20Guidance%20Principles.pdf](https://www.lifecycleinitiative.org/wp-content/uploads/2012/12/2011%20-%20Global%20Guidance%20Principles.pdf))


<br><br>




[**_Return to TOC_**](./00-sub-handbook-landing.md)
<br>

[Return to USLCI Content Wiki](https://github.com/uslci-admin/uslci-content/wiki)

