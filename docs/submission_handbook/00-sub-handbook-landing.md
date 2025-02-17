# :books:  USLCI DATA SUBMISSION HANDBOOK
![](../../images/site_hpphoto_buildings_lci.png)

[Return to USLCI Content Wiki](https://github.com/uslci-admin/uslci-content/wiki)


This Data Submission Handbook for the [U.S. Life Cycle Inventory Database (USLCI)][uslci] is part of the [USLCI Content Repository](https://github.com/uslci-admin/uslci-content/wiki) and is intended to support the USLCI data submission process. The National Renewable Energy Lab (NREL), in partnership with the USDA National Agricultural Library (NAL), has developed this comprehensive LCI data documentation and publication handbook and implemented a streamlined, transparent, user-focused publication workflow. This handbook outlines how to prepare your data for publication on the USLCI, including: metadata descriptors, nomenclature, categorization, and the representation of flows and processes. There are detailed descriptions on how to use openLCA to prepare your data, and how NREL will support the publication of your work. The USLCI data handbook and publication tools are fully aligned and compliant with the emerging [Federal LCA Commons (FLCAC)](https://www.lcacommons.gov/) data guidelines.  **Note this is a living document and is being updated as the FLCAC data submission process evolves.**

:tv: :sound: <br>

For video guidance on accessing, navigating, versioning, using, and submitting data to the USLCI Database (and more), please see the [USLCI Quick Help Video Series](https://www.youtube.com/playlist?list=PLmIn8Hncs7bFUOyXZNGXwG4LtdoTfLz6Q) on NREL's Learning YouTube channel.
<br> 
:tv: :sound: 

<br>



To return to this welcome and navigation page from any page in the handbook, click [**"Return to TOC"**](#toc) at the top or bottom of any of the pages.


The handbook is divided into four major sections.  
1. [Should I publish my data in the USLCI?](./01-should-i-publish-in-the-uslci.md)
1. [How do I publish my data in the USLCI?](./02-how-to-publish-in-the-uslci.md)
1. [Frequently Asked Questions](./03-frequently-asked-questions.md)
1. [Resources](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-resources.md)

[Section 1](./01-should-i-publish-in-the-uslci.md) helps potential data Providers decide if publishing their data in the USLCI Database of the FLCAC is a good fit for their publication goals. This section includes information on the benefits of publishing in the USLCI Database and dataset standards and formatting requirements.  [Section 2](./02-how-to-publish-in-the-uslci.md) contains a detailed guidance for publishing data in the USLCI. This section includes information on the data curation process, information on data forms (e.g., nomenclature, units, metadata, peer review), and submission instructions.  [Section 3](./03-frequently-asked-questions.md) provides answers to frequently asked questions.  [Section 4](./04-resources/04-resources.md) contains links to templates, tools, licensing information, an openLCA example, and other files which support the data submission process.  

Here is a detailed [TABLE OF CONTENTS](#toc).

<a id="toc"></a>
# TABLE OF CONTENTS


### [Preface](./00-preface.md)
### [Acronyms & Abbreviations](./00-acronyms-abbreviations.md)
### [Section 1: Should I publish my data in the US LCI?](./01-should-i-publish-in-the-uslci.md)
  * [Benefits](./01-should-i-publish-in-the-uslci.md#benefits)
  * [Expectations](./01-should-i-publish-in-the-uslci.md#expectations)
    * [_Placing your data in the public domain_](./01-should-i-publish-in-the-uslci.md#placing-your-data-in-the-public-domain)
    * [_Dataset citations_](./01-should-i-publish-in-the-uslci.md#dataset-citations)
    * [_Data formatting_](./01-should-i-publish-in-the-uslci.md#data-formatting)
  * [Data requirements](./01-should-i-publish-in-the-uslci.md#data-requirements)
    * [_Data reliability and reproducibility_](./01-should-i-publish-in-the-uslci.md#data-reliability-and-reproducibility)
    * [_Categorization_](./01-should-i-publish-in-the-uslci.md#categorization)
    * [_Nomenclature_](./01-should-i-publish-in-the-uslci.md#nomenclature)
### [Section 2: How do I publish my data in the US LCI?](./02-how-to-publish-in-the-uslci.md)
  * [Working with NREL](./02-how-to-publish-in-the-uslci.md#working-with-nrel)
  * [Overview of the Digital Curation process](./02-how-to-publish-in-the-uslci.md#overview-digital-curation)
    * [_Appraisal_](./02-how-to-publish-in-the-uslci.md#appraisal)
    * [_Ingest & Onboarding_](./02-how-to-publish-in-the-uslci.md#ingest-and-onboarding)
    * [_Review_](./02-how-to-publish-in-the-uslci.md#review)
    * [_Publication_](./02-how-to-publish-in-the-uslci.md#publication)
    * [_Preservation_](./02-how-to-publish-in-the-uslci.md#preservation)
  * [Guidance on data compilation in OpenLCA](./02-how-to-publish-in-the-uslci.md#guidance-data-compilation-openlca)
  * [Metadata guidance tables](./02-how-to-publish-in-the-uslci.md#metadata-guidance-tables)
### [Section 3: Frequently asked questions](./03-frequently-asked-questions.md)
  * [What is the USLCI Database?](./03-frequently-asked-questions.md#what-is-uslci)
  * [Why should I publish my data in the USLCI Database?](./03-frequently-asked-questions.md#why-publish-in-uslci)
  * [How long does the publication process take?](./03-frequently-asked-questions.md#how-long-to-publish)
  * [When will my data be published?](./03-frequently-asked-questions.md#when-data-published)
  * [What is my role in the publication process?](./03-frequently-asked-questions.md#my-role-in-publishing)
  * [Do I have to go through the publication process alone?](./03-frequently-asked-questions.md#go-through-publishing-alone)
  * [Who owns my data after it is published?](./03-frequently-asked-questions.md#who-owns-published-data)
  * [How is my data used after it is published?](./03-frequently-asked-questions.md#how-published-data-used)
### [Section 4: Resources](./04-resources/04-resources.md)
  * [Links to useful resources](./04-resources/04-resources.md)
  * [Data Use Disclaimer Agreement](./04-resources/04-App-A.md)
  * [Data Provider's Content License Agreement](./04-resources/04-App-B.md)
  * [Creative Commons Legal Code](./04-resources/04-App-C.md)
  * [ILCD Nomenclature Rules](./04-resources/04-App-D.md)
  * [2017 NAICS United States Structure](./04-resources/04-App-E.md)
  * [Example openLCA Element Addition](./04-resources/04-App-F.md)
  * [Using the EPA Data Quality Pedigree Matrix in openLCA](./04-resources/04-App-G.md)
  * [Downloading Repositories for Import to openLCA](./04-resources/04-App-H.md)
  * [FEDEFL Nomenclature Highlights](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/05-FEDEFL%20Guidelines%20-%20Appendix%20Fork.md)
  * [Contact the USLCI Webmaster](https://www.nrel.gov/lci/contacts.html)
  
  <br>
  <br>
  
  [Return to USLCI Content Wiki](https://github.com/uslci-admin/uslci-content/wiki)
  
    
[uslci]: https://uslci.lcacommons.gov/uslci/search   
