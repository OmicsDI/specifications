PRIDE Example
=========

Contents
----------

1. [Full pride xml](#1-full-pride-xml)  
2. [Comments by Sections](#2-comments-by-sections)    


#1. Full PRIDE XML

```xml 

<database>
  <name>PRIDE Archive</name>
  <description/>
  <release>3</release>
  <release_date>2015-05-13</release_date>
  <entry_count>1</entry_count>
  <entries>
    <entry id="PRD000123">
      <name>Large scale qualitative and quantitative profiling of tyrosine phosphorylation using a combination of phosphopeptide immuno-affinity purification and stable isotope dimethyl labeling</name>
      <description>Triplex stable isotope dimethyl labeling of phosphotyrosine peptides after EGF stimulation</description>
      <cross_references>
        <ref dbkey="9606" dbname="TAXONOMY"/>
        <ref dbkey="19770167" dbname="pubmed"/>
        <ref dbkey="P60323" dbname="uniprot"/>
        <ref dbkey="ENSP00000243501" dbname="ensembl"/>
        <ref dbkey="P01130" dbname="uniprot"/>
        <ref dbkey="ENSP00000316578" dbname="ensembl"/>
        <ref dbkey="ENSP00000297056" dbname="ensembl"/>
        <ref dbkey="ENSP00000341289" dbname="ensembl"/>
        <ref dbkey="ENSP00000233047" dbname="ensembl"/>
        <ref dbkey="Q9NYY3" dbname="uniprot"/>
        <ref dbkey="ENSP00000295033" dbname="ensembl"/>
        <ref dbkey="ENSP00000364212" dbname="ensembl"/>
        <ref dbkey="ENSP00000295974" dbname="ensembl"/>
        <ref dbkey="ENSP00000379901" dbname="ensembl"/>
        <ref dbkey="ENSP00000325905" dbname="ensembl"/>
        <ref dbkey="Q8NBS9" dbname="uniprot"/>
        <ref dbkey="Q99426" dbname="uniprot"/>
      </cross_references>
      <dates>
        <date type="submission" value="2009-07-14"/>
        <date type="publication" value="2010-07-09"/>
      </dates>
      <additional_fields>
        <field name="omics_type">Proteomics</field>
        <field name="full_dataset_link">http://www.ebi.ac.uk/pride/archive/projects/PRD000123</field>
        <field name="repository">pride</field>
        <field name="sample_protocol">Not available</field>
        <field name="data_protocol">Not available</field>
        <field name="instrument_platform">LTQ Orbitrap</field>
        <field name="instrument_platform">instrument model</field>
        <field name="species">Homo sapiens (Human)</field>
        <field name="cell_type">Not available</field>
        <field name="disease">Not available</field>
        <field name="tissue">HeLa cell</field>
        <field name="modification">2x(13)C,6x(2)H labeled dimethylated L-arginine</field>
        <field name="modification">monohydroxylated residue</field>
        <field name="modification">dimethylated residue</field>
        <field name="modification">phosphorylated residue</field>
        <field name="modification">iodoacetamide - site C</field>
        <field name="modification">4x(2)H labeled dimethylated residue</field>
        <field name="technology_type">Bottom-up proteomics</field>
        <field name="technology_type">Mass Spectrometry</field>
        <field name="submitter_keywords">Not available</field>
        <field name="quantification_method">Not available</field>
        <field name="submission_type">PRIDE</field>
        <field name="software">Not available</field>
        <field name="publication">Boersema PJ, Foong LY, Ding VM, Lemeer S, van Breukelen B, Philp R, Boekhorst J, Snel B, den Hertog J, Choo AB, Heck AJ; In-depth qualitative and quantitative profiling of tyrosine phosphorylation using a combination of phosphopeptide immunoaffinity purification and stable isotope dimethyl labeling., Mol Cell Proteomics, 2010 Jan, 9, 1, 84-99, </field>
        <field name="submitter">Paul Boersema</field>
        <field name="submitter_mail">p.j.boersema@uu.nl</field>
        <field name="submitter_affiliation">Beta faculty</field>
        <field name="dataset_file">ftp://ftp.pride.ebi.ac.uk/pride/data/archive/2010/07/PRD000123/PRIDE_Exp_Complete_Ac_9777.xml.gz</field>
        <field name="dataset_file">ftp://ftp.pride.ebi.ac.uk/pride/data/archive/2010/07/PRD000123/PRIDE_Exp_Complete_Ac_9779.xml.gz</field>
        <field name="dataset_file">ftp://ftp.pride.ebi.ac.uk/pride/data/archive/2010/07/PRD000123/PRIDE_Exp_Complete_Ac_9780.xml.gz</field>
      </additional_fields>
    </entry>
  </entries>
</database>

```

#2. Comments by Sections

**Database header**

This example provides some interesting sections that will allow us to explain in details the **key-value** schema. 
As we explain in the [xml specification](https://github.com/BD2K-DDI/specifications/blob/master/docs/schema/README.md) the
database entry should be wrote with the _name_ , _description_ , _release_ tag , _release_date_ , _entry_count_ the number of entries in the current xml file. In this case because 
the xml can be juge, the distribution can be  done using single xml files _<\entry\_count\>1\<\/entry\_count\>_


```xml
<database>
  <name>PRIDE Archive</name>
  <description/>
  <release>3</release>
  <release_date>2015-05-13</release_date>
  <entry_count>1</entry_count>
    ....
    
```

 **Entry Information**
 
Using the _cross\_references_ the providers can link two biological entities to different databases. For example some datasets in PRIDE identified proteins in 
ENSEMBL and UNIPROT. Then, the list of cross-references can be done to the individual resources using the cross-references. 
This cross-references system allows other databases and third-party applications to find the complete information from other databases. 

 
```xml
...
  <cross_references>
      <ref dbkey="P60323" dbname="uniprot"/>
      <ref dbkey="ENSP00000243501" dbname="ensembl"/>
....
```

In the PRIDE example the pubmed id and the taxonomy are known. In this case the cross-references to those databases can be use:

```xml
...
  <cross_references>
      <ref dbkey="9606" dbname="TAXONOMY"/>
      <ref dbkey="19770167" dbname="pubmed"/>
....
```

**Not available information**

If some information is not present the providers can use the value **not available** in the specific field. 

```xml
     <field name="cell_type">Not available</field>
     <field name="disease">Not available</field>
```

**Defining more metadata**

In the [xml specification](https://github.com/BD2K-DDI/specifications/blob/master/docs/schema/README.md) we defined a two main protocols as RECOMMENDED **data_protocol** and **sample_protocol**.
However, additional information can be provided related with the protocols as **key-value** pairs. The proteomics databases can explort the information of modifications using key-value 
pairs like: 

```xml
....
<additional_fields>
     <field name="modification">2x(13)C,6x(2)H labeled dimethylated L-arginine</field>
     <field name="modification">monohydroxylated residue</field>
     <field name="modification">dimethylated residue</field>
     <field name="modification">phosphorylated residue</field>
     <field name="modification">iodoacetamide - site C</field>
     <field name="modification">4x(2)H labeled dimethylated residue</field>
</addtional_fields>
....
```


**Data Fields**
 
For the data files associated with the dataset, the providers can annotate the complete url of the files: 

```xml
 <additional_fields>
    <field name="dataset_file">ftp://ftp.pride.ebi.ac.uk/pride/data/archive/2010/07/PRD000123/PRIDE_Exp_Complete_Ac_9777.xml.gz</field>
    <field name="dataset_file">ftp://ftp.pride.ebi.ac.uk/pride/data/archive/2010/07/PRD000123/PRIDE_Exp_Complete_Ac_9779.xml.gz</field>
    <field name="dataset_file">ftp://ftp.pride.ebi.ac.uk/pride/data/archive/2010/07/PRD000123/PRIDE_Exp_Complete_Ac_9780.xml.gz</field>
</additional_fields>
```

This annotation is important for third-party tools to download the files or reprocess the original results. 
