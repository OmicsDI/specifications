Metabolights Example
=========

Contents
----------

1. [Full metabolights xml](#1-full-metabolights-xml)  
2. [Comments by Sections](#2-comments-by-sections)    


#1. Full Metabolights XML

```xml 

<database>
    <name>MetaboLights</name>
    <description>MetaboLights is a database for Metabolomics experiments and derived information</description>
    <release>3</release>
    <release_date>2015-10-06</release_date>
    <entry_count>2</entry_count>
    <entries>
        <entry id="MTBLS67">
            <name>Metabolomic Analysis of Fission Yeast at the Onset of Nitrogen Starvation</name>
            <description>
                       Microorganisms naturally respond to changes in nutritional conditions by adjusting their morphology and physiology.
                       The cellular response of the fission yeast S. pombe to nitrogen starvation has been extensively studied.
            </description>
            <cross_references>
                <ref dbkey="CHEBI:16551" dbname="ChEBI"/>
                <ref dbkey="MTBLC16551" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16810" dbname="ChEBI"/>
                <ref dbkey="MTBLC16810" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:30031" dbname="ChEBI"/>
                <ref dbkey="MTBLC30031" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16264" dbname="ChEBI"/>
                <ref dbkey="MTBLC16264" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:17677" dbname="ChEBI"/>
                <ref dbkey="MTBLC17677" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16695" dbname="ChEBI"/>
                <ref dbkey="MTBLC16695" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:18333" dbname="ChEBI"/>
                <ref dbkey="MTBLC18333" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:58553" dbname="ChEBI"/>
                <ref dbkey="MTBLC58553" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:15713" dbname="ChEBI"/>
                <ref dbkey="MTBLC15713" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:29062" dbname="ChEBI"/>
                <ref dbkey="MTBLC29062" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:15996" dbname="ChEBI"/>
                <ref dbkey="MTBLC15996" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16863" dbname="ChEBI"/>
                <ref dbkey="MTBLC16863" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16761" dbname="ChEBI"/>
                <ref dbkey="MTBLC16761" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:32551" dbname="ChEBI"/>
                <ref dbkey="MTBLC32551" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16176" dbname="ChEBI"/>
                <ref dbkey="MTBLC16176" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:61304" dbname="ChEBI"/>
                <ref dbkey="MTBLC61304" dbname="MetaboLights"/>
            </cross_references>
            
            <dates>
                <date type="submission" value="2013-11-19"/>
                <date type="publication" value="2013-11-26"/>
                <date type="last_modification" value="2013-11-26"/>
            </dates>
            <additional_fields>
                <field name="repository">MetaboLights</field>
                <field name="omics_type">Metabolomics</field>
                
                <field name="sample_protocol">
                        The fission yeast S. pombe heterothallic haploid 972 h- wild-type strain was used for the experiments.
                        Cells were incubated in the EMM2 liquid medium at 26 °C in a water bath with shaking. Cell concentration in the culture was measured by the CDA-500 particle counter (Sysmex, Kobe, Japan). 
                        For metabolome analysis, cells were grown to the log phase and at the concentration of 5 × 106 cells/ml, 40 ml of culture was taken as 0 min sample. 
                </field>
                
                <field name="extraction_protocol">
                      Cells from cultures (40 ml/sample) were collected by vacuum filtration and immediately quenched in 25 ml of –40 °C methanol. 
                </field>
                <field name="chromatography_protocol">
                         LC-MS data were acquired using a Paradigm MS4 HPLC system (Michrom Bioresources, Auburn, AL, USA) coupled to an LTQ Orbitrap mass spectrometer (Thermo Fisher Scientific, Waltham, MA, USA).
                         LC separation was performed on a ZIC-pHILIC column (Merck SeQuant, Umeå, Sweden; 150 × 2.1 mm, 5 µm particle size). 
                         Acetonitrile (A) and 10 mM ammonium carbonate buffer, pH 9.3 (B) were used as the mobile phase, with gradient elution from 80% A to 20% A in 30 min and 100 µl/min flow rate.
                </field>
                <field name="mass_spec_protocol">
                         Mass spectrometer was operated in full scan mode with the scan range of 100-1,000 m/z. Each sample was analyzed twice, once in negative and once in positive 
                         ionization mode.
                </field>
                <field name="data_protocol">
                         Raw LC-MS data were analyzed by the MZmine 2 software. The complete workflow and processing parameters are summarized in the publication.
                </field>
                <field name="metabolite_id_protocol">
                         Metabolites were identified by comparing their m/z values and retention times with authentic pure standards, as described in the publication.
                </field>
                <field name="technology_type">mass spectrometry</field>
                <field name="instrument_platform">LTQ Orbitrap Classic (Thermo Scientific)</field>
                <field name="submitter">Tomas Pluskal</field>
                <field name="submitter_email">pluskal@oist.jp</field>
                <field name="submitter_affiliation">Okinawa Institute of Science and Technology Graduate University (OIST)</field>
                
                <field name="study_design">metabolomic profiling</field>
                <field name="study_design">cellular response to nitrogen starvation</field>
                <field name="study_design">liquid chromatography-mass spectrometry</field>
                
                <field name="study_factor">Time in nitrogen starvation</field>
                <field name="study_status">Public</field>
                <field name="full_dataset_link">http://www.ebi.ac.uk/metabolights/MTBLS67</field>
                
                <field name="dataset_file">ftp://ftp.ebi.ac.uk/pub/databases/metabolights/studies/public/MTBLS67</field>
                
                <field name="Organism">EFO:Schizosaccharomyces pombe 972h-</field>
                <field name="Organism Part">vegetative cell</field>
                
                <field name="publication">Metabolomic Analysis of Fission Yeast at the Onset of Nitrogen Starvation. 10.3390/metabo3041118.</field>
                
                <field name="metabolite_name">Trehalose </field>
                <field name="metabolite_name">2-Oxoglutarate </field>
                <field name="metabolite_name">Succinate </field>
                <field name="metabolite_name">UDP-N-acetyl-glucosamine </field>
                <field name="metabolite_name">CTP </field>
                <field name="metabolite_name">UMP </field>
                <field name="metabolite_name">D-Arabitol </field>
                <field name="metabolite_name">CDP </field>
                <field name="metabolite_name">UTP </field>
                <field name="metabolite_name">GDP-glucose </field>
                <field name="metabolite_name">GTP </field>
                <field name="metabolite_name">6-Phospho-gluconate </field>
                <field name="metabolite_name">ADP </field>
                <field name="metabolite_name">Lysine </field>
                <field name="metabolite_name">Ornithine </field>
                <field name="metabolite_name">Phospho-glycerate</field>
                <field name="metabolite_name">Inosine </field>
                <field name="metabolite_name">ATP </field>
                <field name="metabolite_name">GDP </field>
                <field name="metabolite_name">Citrate </field>
                <field name="metabolite_name">Ribose-phosphate </field>
                <field name="metabolite_name">Malate </field>
                <field name="metabolite_name">AMP</field>
            </additional_fields>
        </entry>
        
        <entry id="MTBLS125">
            <name>Distribution of RESV and its metabolite peaks in mouse tissues after oral and skin administration</name>
            <description>
                   RESV (1 mg in 200 ul saline) was orally administered to hairless mice or 1 mg RESV dissolved in ethanol was applied on the dorsal skin of hairless mice. 
                   After 4 h mice were sacrificed, metabolites were extracted from the tissues and analyzed by the LC-MS. 
                   Peak areas of metabolites were normalized by the peak areas of spiked internal standards (HEPES and PIPES).
            </description>
            <cross_references>
                <ref dbkey="CHEBI:16761" dbname="ChEBI"/>
                <ref dbkey="MTBLC16761" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16027" dbname="ChEBI"/>
                <ref dbkey="MTBLC16027" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:15422" dbname="ChEBI"/>
                <ref dbkey="MTBLC15422" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:17239" dbname="ChEBI"/>
                <ref dbkey="MTBLC17239" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:17677" dbname="ChEBI"/>
                <ref dbkey="MTBLC17677" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:17552" dbname="ChEBI"/>
                <ref dbkey="MTBLC17552" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:17345" dbname="ChEBI"/>
                <ref dbkey="MTBLC17345" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:15996" dbname="ChEBI"/>
                <ref dbkey="MTBLC15996" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:17202" dbname="ChEBI"/>
                <ref dbkey="MTBLC17202" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:17659" dbname="ChEBI"/>
                <ref dbkey="MTBLC17659" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16695" dbname="ChEBI"/>
                <ref dbkey="MTBLC16695" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:15713" dbname="ChEBI"/>
                <ref dbkey="MTBLC15713" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16020" dbname="ChEBI"/>
                <ref dbkey="MTBLC16020" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:19062" dbname="ChEBI"/>
                <ref dbkey="MTBLC19062" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16708" dbname="ChEBI"/>
                <ref dbkey="MTBLC16708" dbname="MetaboLights"/>
                <ref dbkey="CHEBI:16335" dbname="ChEBI"/>
                <ref dbkey="MTBLC16335" dbname="MetaboLights"/>   
            </cross_references>
            
            <dates>
                <date type="submission" value="2014-12-11"/>
                <date type="publication" value="2014-12-15"/>
                <date type="last_modification" value="2014-12-15"/>
            </dates>
            
            <additional_fields>
                <field name="repository">MetaboLights</field>
                <field name="omics_type">Metabolomics</field>
                <field name="sample_protocol">
                         Mice were anesthetized by pentobarbital and blood was collected from the right heart ventricle. 
                         Metabolome samples were prepared from blood (0.2ml) and liver, dorsal skin, leg skin and hind limb muscle (around 100mg of each tissue).
                </field>
                <field name="extraction_protocol">
                         Around 100 mg of each mouse tissue was cut out and weighted. Tissues were minced and homogenized for 3 min in 500 ul 50% methanol on ice 
                         using BioMasher II (Nippi, Tokyo, Japan). Next, 1 ml 50% methanol and internal standards (10 nmol HEPES and PIPES) were added to the samples.
                         HEPES and PIPES were used as internal standards to correct for the variation of sample preparation and different detection efficiency.
                         After brief vortexing samples were centrifuged at 500 g for 10 min at 4 °C. Supernatant was recovered for further processing.
                         For metabolite extraction 0.2 ml of blood were mixed with 1.8 ml 55% methanol pre-chilled to -40°C,  internal standards (HEPES and PIPES) 
                         added and samples kept until further processing.
                </field>
                <field name="chromatography_protocol">
                         LC separation was performed on a ZIC-pHILIC column (Merck SeQuant, 150 x 2.1 mm, 5 um particle size). 
                         Acetonitrile (A) and 10 mM ammonium carbonate buffer, pH 9.3 (B) were used as the mobile phase, with gradient elution from 80% A to 20% A in
                         30 min and 100 ul/min flow rate. Sample injection volume was 1 ul per run.
                </field>
                <field name="mass_spec_protocol">
                         Mass spectrometer was operated in full scan mode with the scan range of 100-1,000 m/z.
                         Each sample was analyzed twice, once in negative and once in positive ionization mode.
                </field>
                <field name="data_protocol">Raw LC-MS data were analyzed by the MZmine 2 software. 
                         The complete workflow and processing parameters are summarized in the publication.
                </field>
                <field name="metabolite_id_protocol">
                         Metabolites were identified by comparing their m/z values and retention
                         times with authentic pure standards. To assign the metabolites of which standards are not available, we performed a
                         careful MS/MS analysis, as described in the publication.</field>
                <field name="technology_type">mass spectrometry</field>
                <field name="instrument_platform">LTQ Orbitrap Classic (Thermo Scientific)</field>
                
                <field name="submitter">Romanas Chaleckis</field>
                <field name="submitter_email">romanas.chaleckis@gmail.com</field>
                <field name="submitter_affiliation">Kyoto university</field>
                
                <field name="study_design">metabolite profiling</field>
                <field name="study_design">Resveratrol</field>
                <field name="study_design">Nude Mouse</field>
                <field name="study_design">Mouse Skin</field>
                <field name="study_design">liquid chromatography-mass spectrometry</field>
                <field name="study_factor">Treatment</field>
                <field name="study_factor">Tissue</field>
                <field name="study_status">Public</field>
                
                <field name="full_dataset_link">http://www.ebi.ac.uk/metabolights/MTBLS125</field>
                <field name="dataset_file">ftp://ftp.ebi.ac.uk/pub/databases/metabolights/studies/public/MTBLS125</field>
                <field name="species">Nude Mouse</field>
                <field name="Organism Part">blood</field>
                
                <field name="publication">Metabolism of skin-absorbed resveratrol into its glucuronized form in mouse skin. 10.1371/journal.pone.0115359.</field>
                
                <field name="metabolite_name">ADP</field>
                <field name="metabolite_name">AMP</field>
                <field name="metabolite_name">ATP</field>
                <field name="metabolite_name">CDP</field>
                <field name="metabolite_name">CTP</field>
                <field name="metabolite_name">GDP</field>
                <field name="metabolite_name">GMP</field>
                <field name="metabolite_name">GTP</field>
                <field name="metabolite_name">IMP</field>
                <field name="metabolite_name">UDP</field>
                <field name="metabolite_name">UMP</field>
                <field name="metabolite_name">UTP</field>
                <field name="metabolite_name">1-Methyl-adenosine</field>
                <field name="metabolite_name">1-Methyl-guanosine</field>
                <field name="metabolite_name">Adenine</field>
                <field name="metabolite_name">Adenosine</field>
                <field name="metabolite_name">Cytidine</field>
                <field name="metabolite_name">Dimethyl-guanosine</field>
                <field name="metabolite_name">Guanosine</field>
                <field name="metabolite_name">Hypoxanthine</field>
                <field name="metabolite_name">Inosine</field>
                <field name="metabolite_name">Uracil</field>
                <field name="metabolite_name">Urate</field>
                <field name="metabolite_name">Uridine</field>
                <field name="metabolite_name">4-Aminobenzoate</field>
                <field name="metabolite_name">NAD+</field>
                <field name="metabolite_name">NADH</field>
                <field name="metabolite_name">NADP+</field>
                <field name="metabolite_name">NADPH</field>
                <field name="metabolite_name">Nicotinamide</field>
                <field name="metabolite_name">Pantothenate</field>
            </additional_fields>
            </entry>
         </entries>
 </database>

```

#2. Comments by Sections

**Database header**

This example provides some interesting sections that will allow us to explain in details the **key-value** schema. 
As we explain in the [xml specification](https://github.com/BD2K-DDI/specifications/blob/master/docs/schema/README.md) the
database entry should be wrote with the _name_ , _description_ , _release_ tag , _release_date_ , _entry_count_ the number of entries in the current xml file. 


```xml
<database>
   <name>MetaboLights</name>
    <description>MetaboLights is a database for Metabolomics experiments and derived information</description>
    <release>3</release>
    <release_date>2015-10-06</release_date>
    <entry_count>2</entry_count>
    ....
    
```

 **Entry Information**
 
Using the _cross\_references_ the providers can link the same biological entity to multiple databases. In this case the providers are linking the _α,α-trehalose_ to the ChEBI 
identifier and the Metaboligths identifier. This cross-references system allows other databases and third-party applications to find the complete information from other databases. 

 
```xml
  <cross_references>
      <ref dbkey="CHEBI:16551" dbname="ChEBI"/>
      <ref dbkey="MTBLC16551" dbname="MetaboLights"/>
....
```


**Defining more metadata**

In the [xml specification](https://github.com/BD2K-DDI/specifications/blob/master/docs/schema/README.md) we defined a two main protocols as RECOMMENDED **data_protocol** and **sample_protocol**.
However, additional information can be provided related with the protocols as **key-value** pairs. This open option is important for providers that for example implement [ISA format](http://www.isa-tools.org/).   
In the current example the Metaboligths database provides four new protocols.   

```xml

 <field name="sample_protocol">
    The fission yeast S. pombe heterothallic haploid 972 h wildtype strain was used for the experiments.
 </field>
 <field name="extraction_protocol">
      Cells from cultures (40 ml/sample) were collected by vacuum filtration and immediately quenched in 25 ml of –40 °C methanol. 
  </field>
  <field name="chromatography_protocol">
     LC-MS data were acquired using a Paradigm MS4 HPLC system (Michrom Bioresources, Auburn, AL, USA) coupled to an LTQ Orbitrap mass spectrometer (Thermo Fisher Scientific, Waltham, MA, USA).
  </field>
  <field name="mass_spec_protocol">
     Mass spectrometer was operated in full scan mode with the scan range of 100-1,000 m/z. 
  </field>
  <field name="data_protocol">
     Raw LC-MS data were analyzed by the MZmine 2 software. The complete workflow and processing parameters are summarized in the publication.
  </field>
  <field name="metabolite_id_protocol">
     Metabolites were identified by comparing their m/z values and retention times with authentic pure standards, as described in the publication.
  </field>
```


**Unreferenced data**
 
Some biological entities can't be found [amount referenced databases](https://www.ebi.ac.uk/ebisearch/). In those cases the user can try to annotate as ke-value pairs 
the data in the XML: 

```xml
 <additional_fields> 
   <field name="metabolite_name">4-Aminobenzoate</field>
 </additional_fields>
```

In this case Metaboligths annotated inside the XML the name of each metabolite as additional information. It also annotated information related with the study design"

```xml
 <additional_fields>
     <field name="study_design">metabolite profiling</field>
     <field name="study_design">Resveratrol</field>
     <field name="study_design">Nude Mouse</field>
     <field name="study_design">Mouse Skin</field>
</additional_fields>
```

