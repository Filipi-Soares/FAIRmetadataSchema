# Accessing the FAIRness of Metadata Schemas

This assessment evaluates the main FAIR-related concepts addressed in Table 1 of the referenced paper and the conceptual model. The goal is to identify the FAIR components listed in Table 1 and in the conceptual model to determine the schema FAIRness level.

We assed the FAIRness level of three metadata schemas: Darwin Core, D-CAT, and Almes Core. However, this analysis was preliminary and superficial. A more detailed assessment should be performed by the authority managing these schemas.

## Methodology
The concepts from the conceptual model representing FAIR enabling resources (FERs) were associated with one of the Refined FAIR principles presented in Table 1. The FAIR principles were assessed based on the presence or absence of specific FERs, with each FER receiving a score from 0.25 to 1. The scores for each FER within a principle were then summed to calculate the total score for that principle. Details on the scores of each element are shown in Table 1A. 

| Ref. FAIR | FAIR P. | Concept Score                                                                 | 
|-----------|---------|----------------------------------------------------------------------------------|
| RF1       | F       | Namespace (0.5); version unique identifier (0.5)                                  |    
| RF2       | F       | Landing page (0.5); metadata record for humans (0.25); metadata record for machines (0.25) |
| RF3       | F       | Indexing in vocabulary catalog (1)                                                                                 |  
| RF4       | A       | URLs use universally accessible protocols (1)                                    |   
| RF5       | A       | Backup (1)                                                                       |  
| RF6       | I       | Machine-actionable serialization (1)                                             |      
| RF7       | I       | Schema Conceptual model (1)                                                      |                
| RF8       | I       | Data Properties (0.5); Range and Domain (0.5)                                    |                            
| RF9       | I       | Object Properties (0.5); Range and Domain (0.5)                                  |                        
| RF10      | R       | Term name (0.5); Definition (0.5)                                                |                            
| RF11      | R       | Open License (1)                                                                 |                           
| RF12      | R       | Documentation of Modifications (1)                                               |                             
| RF13      | I (50%) R (50%) | Schema reuse (1)                                                                  |      

*Table 1A – Template for calculating the FAIRness level of the Almes Core schema.*


