OmicsDI XML Schema
=========

Contents
----------

1. [Omics Discovery Index: Metadata](#1-omics-discovery-index:-metadata)  
 1.1. [OmicsDI database section](#11-file-sections)    
 1.2. [Field Types](#12-field-types) 
 1.3. [Example](#13-examples)  
* [Databases](#2-databases)  
  2.1. [Major Partners?](#21-major-partners)  
  2.2. [Which databases are part of OmicsDI](#22-which-databases-are-part-of-omicsdi)  
  2.3. [OmicsDI Architecture?](#23-Omicsdi-architecture)  
  2.4. [OmicsDI XML](#24-omicsDI-xml)
* [Web services and Web Application](#3-web-services-and-web-application) 
  3.1. [Access to the web-services](#31-access-to-the-web-services)
  3.2. [Web Application](#32-web-application)
* [Support](#4-support)  
  3.1  [Get involved](#41-get-involved)  
  3.2. [Contact](#42-contact)   
* [License](#5-license)  

1. Omics Discovery Index: Metadata
--------------

The metadata of a dataset is a well-know problem in the biomedical community and information science.  In contrast with publications where a common structure is provided
and the manuscripts describe the results and data, datasets are normally more heterogonous and complex to describe. Different guidelines, standards and protocols have been
created to standardize the metadata that needs to be provided by researchers to deposit their data and describe their experiments. However, many repositories only provide
a subset of this guidelines and metadata, and information and still the data they storage, and provides is valuable and accessible. 

To overcome this challenge, OmicsDI define a hierarchical metadata schema for each dataset divided in three main categories: (i) mandatory, (ii) recommended and (iii) additional.
The scoring system in the OmicsDI search engine boost those datasets that provides more metadata, rewarding those groups and researchers that annotate in a better way the results.
The following tables described the metadata fields for each category, with examples and description in each case. This document described the structure of OmicsDI Schema version 1.0
and the corresponding metadata fields and the type of the fields. For each field in OmicsDI we have defined three type of categories:
  
*   **Mandatory   (M)**  : These fields should be provided in the omicsDI schema to be valid, it also represent the fields that needed to be defined for an OmicsDI dataset. 
*   **Recommended (R)**: These fields should be provided to be searched and displayed properly by OmicsDI infrastructure, web, web-services. 
*   **additional  (A)** : These fields should be provided to add value to the dataset, if the dataset contains more metadata the omicsDI infrastructure can make more sence out of the data. For example.
if the proteins, genes or metabolites are provided for each dataset; omicsdi would be able to find the datasets were those proteins has been found.   
          

## 1.1 OmicsDI database section

The OmicsDI XML 1.0 is integrated by different sections. Here we will explain each section in details with the fields, the type of the fields and the structure of the sections. 
  
General header for the database and provider. The database contains all the information that would be included inside OmicsDI. Because each database can select to provide all their data in single 
XML files (1 dataset per file) or multiple entries _\<entries\>_ by XML a short information about the provider should be provided.  
 
```xml
 <database>
   <name>Database Name</name>
   <description>This database contains proteomics information<description/>
   <release>3</release>
   <release_date>2015-05-13</release_date>
   <entry_count>1</entry_count>
   <entries>
   </entries>
```


Fields: 

| Field        | Comment                                                                                                                                                                                                | Example                                                                                                          | Type  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|-------|
| name         | Name of the database or provider                                                                                                                                                                       | ``` <name>PRIDE</name> ```                                                                                    | **M** |
| description  | A short description of the provider. This description can be use in the future to search for different databases and also is  show in the omicsdi web to provide the information about the  providers. | ``` <description> The proteomics identification database is an EBI resource for Proteomics </description> ``` | **R** |
| release      | This information provide information about the release base cycle.  Some databases are based on releases and would be interesting to know the  release tag.                                            | ``` <release>Release-May-2016</release>                                                                   ``` | **A** |
| release_date | This information contains the date of the release. **It can be use as also as the date for the data generation in some cases.**                                                                        | ``` <release_date> 2015-05-13 <release_date>                                                              ``` | **R** |
| entry_count  | This field contains the number of entries in the current XML file. Tis field is used for validation purposes.                                                                                          | ``` <entry_count>2</entry_count>                                                                          ``` | **M** |