# Fields currently use in OmicsDI

| Category Type  |   Type       | Field Name               |                   Description                    | 
|:--------------:|:------------:|:------------------------:|:------------------------------------------------:|
|       -        |   Mandatory  | id                       | Unique id of the dataset withing the database    |
|       -        |   Mandatory  | name                     | Title of the dataset                             |
|       -        |   Mandatory  | description              | Description of the dataset                       | 
|     dates      |   Mandatory  | publication              | Date of data published                           |
|     dates      |   Optional   | updated                  | Date of Updated the data                         | 
|     dates      |   Optional   | submission               | Date of submission of the data                   |
|     dates      |   Optional   | creation                 | Date of creation                                 |  
|     dates      |   Optional   | last_modification        | Date of last modification                        | 
|   additional   |   Optional   | data_protocol            | A general description of the data processing     | 
|   additional   |   Optional   | sample_protocol          | A general description of the sample procol       | 
|   additional   |   Mandatory  | omics_type               | Type of the omics, important for the integration | 
|   additional   |   Mandatory  | repository               | Name of the repository, it is important because some systems agrregate data here we capture the actual database |
|   additional   |   Mandatory  | full_dataset_link        | The url where the dataset can be found           | 
|   additional   |   Optional   | instrument_platform      | Instrument used to generate the data             |
|   additional   |   Optional   | species                  | Species on **Free Text** to be index and search  | 
|   additional   |   Optional   | cell_type                | Cell type on **Free Text** to be index and search| 
|   additional   |   Optional   | disease                  | Disease type on **Free Text** to be index and search|
|   additional   |   Optional   | tissue                   | Tissue type on **Free Text** to be index and search | 
|   additional   |   Optional   | software                 | Software type on **Free Text** to be index and search | 
|   additional   |   Mandatory  | submitter                | Submitter of the dataset to the original database | 
|   additional   |   Mandatory  | submitter_mail           | Submitter mail                                    | 
|   additional   |   Optional   | submitter_affiliation    | Submitter Affiliation                             | 
|   additional   |   Optional   | submitter_keywords       | Submitter keywords                                |  
|   additional   |   Optional   | labhead                  | Name of the PI or Head of the Lab                 |
|   additional   |   Optional   | labhead_mail             | Email of the PI or Head of the Lab                | 
|   additional   |   Optional   | labhead_affiliation      | Affiliation of the PI or Head of the Lab          | 
|   additional   |   Optional   | publication              | Free text describing the publications, citation, title | 
|   additional   |   Optional   | dataset_file             | Dataset supplementary files                        | 
