OmicsDI XML Schema
=========

Contents
----------

1. [Omics Discovery Index](#1.-omics-discovery-index)  
2. [OmicsDI database section](#2-omicsdi-database-section)    
3. [Field Types](#12-field-types) 
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

#1. Omics Discovery Index


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
          

#2. OmicsDI database section

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


**Fields**: 

| Field        | Comment                                                                                                                                                                                                | Example                                                                                                          | Type  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|-------|
| name         | Name of the database or provider                                                                                                                                                                       | ``` <name> PRIDE </name> ```                                                                                     | **M** |
| description  | A short description of the provider. This description can be use in the future to search for different databases and also is  show in the omicsdi web to provide the information about the  providers. | ``` <description> The proteomics identification database is an EBI resource for Proteomics </description> ```    | **R** |
| release      | This information provide information about the release base cycle.  Some databases are based on releases and would be interesting to know the  release tag.                                            | ``` <release>Release-May-2016</release>                                                                   ```    | **A** |
| release_date | This information contains the date of the release. It can be use as also as the date for the data generation in some cases.*                                                                           | ``` <release_date> 2015-05-13 <release_date>                                                              ```    | **R** |
| entry_count  | This field contains the number of entries in the current XML file. Tis field is used for validation purposes.                                                                                          | ``` <entry_count>2</entry_count>                                                                          ```    | **M** |

*Please not that for all dates you should check the **section general types**. 

The providers can add more information to the _database_ information but they will not be considered during the indexing process. Some providers use these additional posibility to add for example 
licenses requirements. Example: 

```xml 
<license> Apache 2.0 </license>
```

**Multiple datasets** _vs_ **Full repository** Files:

The data in OmicsDI can be distributed a Full repository XML file for those databases that do not contains to many datasets. In those cases make sense to create only 
one file for the complete resource. However, most of omics resources contains a huge number of datasets making difficult to exchange the data in a single file. For those cases 
the resources can export their data to **multiple datasets files**, example:

* PRIDE_FILE_1_SIZE_2.xml:

```xml
 <database>
   <name>Database Name</name>
   <description>This database contains proteomics information<description/>
   <release>3</release>
   <release_date>2015-05-13</release_date>
   <entry_count>2</entry_count>
   <entries>
      <entry>
      ...
     </entry>
     <entry>
      ...
     </entry>
   </entries>
 </database>   
```

* PRIDE_FILE_2_SIZE_2.xml

```xml
 <database>
   <name>Database Name</name>
   <description>This database contains proteomics information<description/>
   <release>3</release>
   <release_date>2015-05-13</release_date>
   <entry_count>2</entry_count>
   <entries>
      <entry>
      ...
     </entry>
     <entry>
      ...
     </entry>
   </entries>
 </database>   
```


##3. OmicsDI Entries (datasets)

The entry section contains all the datasets in the repository, provider. The _\<entries\>_ tag is used to listed all the entries. Each dataset is enclosed in a entry tag _\<entry\>_ . 

```xml
 ...
   <entries>
      <entry>
      ...
     </entry>
     <entry>
      ...
     </entry>
...
```

*It is important to note that the number of entries should correspond with the entry_count value. 

Each entry contains all the information in three different sections: (1) general information (root properties), (2) cross-references, (3) additional fields. 

##3.1 Entry (dataset)

The entry tag started with three attibutes and one mandatory sections (see Example): 

```xml 
<entry id="ST000004">
  <name>Lipidomics studies on NIDDK / NIST human plasma samples</name>
  <description>
           The National Institute of Diabetes and Digestive and Kidney Diseases (NIDDK) in collaboration with the National Institute of Standards (NIST) 
           recently produced a human plasma standard reference material (SRM 1950) for metabolite analysis.
  </description>
</entry>    
```


A dataset in omicsDI is compulsory to have three different attributes: and **identifier**, a **name**, and a definition or abstract:
 
**Fields**: 
 
| Field        | Comment                                                                                                         | Example                                                                            | Type  |
|--------------|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------|
| id           | Original and UNIQUE identifier across the repository, database or provider                                      | ``` <entry id="PXD000001">```                                                      | **M** |
| name         | Name, title of the dataset, can be considered as the title of the publication                                   | ``` <name>TMT spikes</name> ```                                                    | **M** |
| description  | This a a short description or abstract of the dataset. It can be considered similar to a "publication abstract" | ``` <description> Expected reporter ion ratios: Erwinia peptides</description> ``` | **M** |

Another **mandatory** field related with each dataset is the date of the publication. Each providers can be define if the dates of the publication is the date of release, creation, submission, etc. 
However for OmicsDI a date value with the type **publication** should be provided. The structure to provide all types of dates is defined as:

```xml 
<entry id="ST000004">
  <name>Lipidomics studies on NIDDK / NIST human plasma samples</name>
  <description>
           The National Institute of Diabetes and Digestive and Kidney Diseases (NIDDK) in collaboration with the National Institute of Standards (NIST) 
           recently produced a human plasma standard reference material (SRM 1950) for metabolite analysis.
  </description>
  <dates>
      <date type="publication" value="13-02-22" /> 
      <date type="submission"  value="13-02-20" />
      <date type="updated"     value="14-05-21" />
      ..
  </dates>
</entry>    
```

Each date entry is composed by a **type** that represent the name of the date and can be amount other: publication **(M)**, submission **(A)**, updated **(A)**, creation **(A)**, others. It also
contains a value attribute which is the value of the date, please you should check the **section general types** to see the format for the value.
 
##3.2 Dataset Fields 

All the information of the dataset is handled using a key value pair structure under the the tag _\<additional_fields\>_ . Key value pairs struture allow you to store in the XML waht ever information the
user/provider would like to provide to OmicsDI infrastructure. Some major advantages of key-value pair representation:
 
>A name–value pair, key–value pair, field–value pair or attribute–value pair is a fundamental data representation in computing systems and applications.
>Designers often desire an open-ended data structure that allows for future extension without modifying existing code or data. In such situations, all or part of the
>data model may be expressed as a collection of tuples <attribute name, value>; each element is an attribute–value pair. Depending on the particular application and the
>implementation chosen by programmers, attribute names may or may not be unique.
 
**It is important to note that the tag _\<additional_fields\>_ do not means that the fields are Additional fields, some of then are mandatory or recommended fields.**
 
 
```xml 
<entry id="ST000004">
  <name>Lipidomics studies on NIDDK / NIST human plasma samples</name>
  <description>
           The National Institute of Diabetes and Digestive and Kidney Diseases (NIDDK) in collaboration with the National Institute of Standards (NIST) 
           recently produced a human plasma standard reference material (SRM 1950) for metabolite analysis.
  </description>
  <dates>
      <date type="publication" value="13-02-22" /> 
      <date type="submission"  value="13-02-20" />
      <date type="updated"     value="14-05-21" />
  </dates>
  <additional_fields>
    ...
  </additional_fields>
  
</entry>    
```

As key value pair the user can define what ever they one and wants to be search. However we have some fields and guidelines from omics committee about the fields that are already standarize. These
fields where agree by the majority of the providers and would be always wrote in the same way. It is important to note that every **key-value** pair is a single representation of the value.
If the user one to reprsent multiple values for the same **key** it should repeat the same tag, for example:

```xml
   ...
   <additional_fields>
     <field name="species">Homo sapiens</field>
     <field name="species">Mus musculus</field>
   </additional_fields>
   ...
```

**Standarized Fields in OmicsDI:**
 
| Field                 | Comment                                                                                                                  | Example                                                                                               | Type  | Cardinality |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------|-------------|
| omics_type            | Omics_Type is a category for the type of omics dataset, it is controlled by OmicsDI infrastructure                       | ``` <field name="omics_type">Proteomics</field>```                                                    | **M** |    [1..n]   |
| data_protocol         | An overview of the data protocol. Description about the software, pipeline and tools that was used to process the data.  | ``` <field name="data_protocol"></field>```                                                           | **R** |    [0..n]   |  
|                       | This can be seen as a abstract of the data handling protocols. Databases used, etc.                                      |                                                                                                       |       |             |
| sample_protocol       | An overview of the sample procol. Description about the general smaple handling and protocol.                            | ``` <field name="sample_protocol"></field>```                                                         | **R** |    [0..n]   |
| repository            | The name of the repository or provider should be specifed at dataset level **(see comments below)**                      | ``` <field name="repository">PRIDE</field>```                                                         | **M** |      [1]    |
| species               | Specie related with the dataset experiment **(Free Text)**                                                               | ``` <field name="species">Homo sapiens</field>```                                                     | **A** |    [0..n]   |
| disease               | Disease related with the dataset and the sample under study (Free Text)                                                  | ``` <field name="disease">Cancer</field>```                                                           | **A** |    [0..n]   |
| tissue                | Tissue related with the dataset and samples under study (Free Text)                                                      | ``` <field name="tissue">Liver</field>```                                                             | **A** |    [0..n]   |
| cell_type             | The cell type annotations for the samples under study (Free Text)                                                        | ``` <field name="cell_type">brain cortex glial cell</field>```                                        | **A** |    [0..n]   |
| full_dataset_link     | The original link of the dataset in the provider, it should be a universal URL that can be to find the original data     | ``` <field name="full_dataset_link">http://www.ebi.ac.uk/pride/archive/projects/PRD000123</field> ``` | **M** |      [1]    |                              
| submitter             | Submitter name, Can be the full name of the person Who provided or submitted the data into the original repository       | ``` <field name="submitter">Yasset Perez-Riverol</field>```                                           | **A** |    [0..n]   |                                       
| submitter_mail        | Submitter contact email is important to have a direct contact with the person Who submit the data                        | ``` <field name="submitter_mail">yperez@ebi.ac.uk</field> ```                                         | **A** |    [0..n]   |
| submitter_affiliation | Submitter affiliation, Institution, Department, etc.                                                                     | ``` <field name="submitter_affiliation">European Bioinformatics Institute</field> ```                 | **A** |    [0..n]   |
| instrument_platform   | This information is realted with all instrument used to analyze the sample and related with the dataset                  | ``` <field name="instrument_platform">LTQ Orbitrap</field> ```                                        | **R** |    [0..n]   | 
| technology_type       | Technology type can be use to describe the experiment type or category, for example: MS/MS proteomics or SRM             | ``` <field name="technology_type">Tandem MS/MS</field> ```                                            | **A** |    [0..n]   |
| modification          | Post-translational Modifications used mainlty in Proteomics experiments                                                  | ``` <field name="modification">Oxidation</field>       ```                                            | **A** |    [0..n]   |          
| submitter_keywords    | Keywords related with the dataset, in this case their added by the submitter of the data                                 | ``` <field name="submitter_keywords">ProteoGenomics</fields> ```                                      | **A** |    [0..n]   |
| quantification_method | Free text describing the quantitative method for example, ITRAQ, SILAC                                                   | ``` <field name="quantification_method">SILAQ</fields> ```                                            | **A** |    [0..n]   |
| submission_type       | In ProteomeXChange this field is used to classify the type of submissions                                                | ``` <field name="quantification_method">COMPLETE</fields> ```                                         | **A** |    [0..n]   |
| software              | Software used in the experiment                                                                                          | ``` <field name="software">Trans-Proteomics Pipeline</fields> ```                                     | **A** |    [0..n]   |
| publication           | Free text describing the publications, citation, title, (see further explanation)                                        | ``` <field name="software">Effect of Obesity on the Preovulatory Follicle.</fields> ```               | **A** |    [0..n]   |

