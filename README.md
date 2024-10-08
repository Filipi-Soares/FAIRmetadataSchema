# Accessing the FAIRness of Metadata Schemas

This assessment evaluates the FAIRness of metadata schemas based on the FAIR-related concepts addressed in the paper's conceptual model. 

We assessed the FAIRness level of three metadata schemas: [Darwin Core](https://dwc.tdwg.org/list/), [D-CAT](https://www.w3.org/TR/vocab-dcat-3/), and [Almes Core](https://w3id.org/AlmesCore#). However, this analysis was preliminary. A more detailed assessment should be performed by the authority managing these schemas.

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

*Table 1A – Template for calculating the FAIRness level of metadata schemas.*

Each component related to a principle was scored based on its presence (true) or absence (false). If a component is present, it contributes its full score; if absent, it contributes zero. For example, for Principle F (Findability):

``RF1 = Namespace (0.5) (true) + version unique identifier (0.5) (true)``
``RF1 = 0.5 + 0.5 = 1``

``RF2 = Landing page (0.5) (true) + metadata record for humans (0.25) (true) + metadata record for machines (0.25) (true)``
``RF2 = 0.5 + 0.25 + 0.25 = 1``

``RF3 = Indexing in vocabulary catalog (1) (false) = 0``
``RF3 = 0``

The total score for each principle is the sum of its components' scores:

``Total Score for F = RF1 + RF2 + RF3 = 1 + 1 + 0 = 2``

The fulfillment percentage for each principle (PF%) is calculated by dividing the total score (TS) by the maximum possible score (MPS) for that principle, then multiplying by 100.

``PF% = (TS / MPS) * 100``
``PF% = (2 / 3) * 100``
``PF% = 66.67%``


The overall FAIR compliance score (OFC%) is the average of the fulfillment percentages of all principles.

## Validation
To validate the FAIR assessment proposed, we evaluated three metadata schemas: [Darwin Core](https://dwc.tdwg.org/), [D-CAT](https://www.w3.org/TR/vocab-dcat-3/), and [Almes Core](https://w3id.org/AlmesCore/). 

## FAIRness assessment of the Darwin Core schema

| Ref. FAIR Principle | FAIR Principle | Concept present                                           | Concept absent                     | Score |
|---------------------|----------------|-----------------------------------------------------------|------------------------------------|-------|
| RF1                 | F              | Namespace (0.5); version unique identifier (0.5)          |                                    | 1     |
| RF2                 | F              | Landing page (0.5); metadata record for humans (0.25)     | metadata record for machines (0.25)| 0.75  |
| RF3                 | F              | Indexing in vocabulary catalog (1)                        |                                    | 1     |
| RF4                 | A              | URLs use universally accessible protocols (1)             |                                    | 1     |
| RF5                 | A              | Backup (1)                                                |                                    | 1     |
| RF6                 | I              |                                                           | Machine-actionable serialization (1)| 0     |
| RF7                 | I              | Schema Conceptual model (1)                               |                                    | 1     |
| RF8                 | I              | Data Properties (0.5)                                     | Range and Domain (0.5)             | 0.5   |
| RF9                 | I              | Object Properties (0.5)                                   | Range and Domain (0.5)             | 0.5   |
| RF10                | R              | Term name (0.5); Definition (0.5)                         |                                    | 1     |
| RF11                | R              | Open License (1)                                          |                                    | 1     |
| RF12                | R              | Documentation of Modifications (1)                        |                                    | 1     |
| RF13                | I (50%) R (50%)| Schema reuse (1)                                          |                                    | 1     |

### Calculation:

| Principle F | Principle A | Principle I | Principle R |
|-------------|-------------|-------------|-------------|
| **F = 1 + 0.75 + 1** | **A = 1 + 1** | **I = 0 + 1 + 0.5 + 0.5 + 0.5** | **R = 1 + 1 + 1 + 0.5** |
| F = 2.75 | A = 2 | I = 2.5 | R = 3.5 |
| PF% = (2.75 / 3) * 100 | PF% = (2 / 2) * 100 | PF% = (2.5 / 4.5) * 100 | PF% = (3.5 / 3.5) * 100 |
| PF% ≅ 92% | PF% = 100% | PF% ≅ 55.5% | PF% = 100% |

![chart (2)](https://github.com/user-attachments/assets/04beb1b9-4309-4b24-b9aa-07da2411380d)

### Overall FAIR compliance score (OFC%): 

OFC% = (92 + 100 + 55.5 + 100) / 4

OFC% ≅ 87%

### Comments:
For the F principle, the standard lacks a machine-actionable serialization of the metadata record on the landing page, although it provides a very detailed record in HTML format. Regarding the I principle, the schema is not available in semantic web formats such as RDF or OWL, despite documentation suggesting how to use Darwin Core as RDF. As noted on [their page](https://dwc.tdwg.org/rdf/), "No terms defined within the Darwin Core namespace have range or domain declarations.” This omission hinders the creation of OWL or RDF serializations of the schema. Additionally, the lack of semantic annotations impedes automated data integration and interoperability across different systems, which are critical to achieving the I principle in the FAIR framework.

Overall, the schema performed well in most aspects of FAIR, reflecting the intense and diligent efforts of the managing authority. This demonstrates a strong commitment to ensuring that the schema meets high standards of findability, accessibility, interoperability, and reusability. Such performance highlights the authority's dedication to maintaining and improving the quality and usability of the schema, which is crucial for supporting diverse data management and integration needs within the community.

## FAIRness assessment of the Data Catalog Vocabulary (DCAT) - Version 3

| Ref. FAIR Principle | FAIR Principle | Concept present                                           | Concept absent                     | Score |
|---------------------|----------------|-----------------------------------------------------------|------------------------------------|-------|
| RF1                 | F              | Namespace (0.5); version unique identifier (0.5)          |                                    | 1     |
| RF2                 | F              | Landing page (0.5); metadata record for humans (0.25); metadata record for machines (0.25)     | | 1  |
| RF3                 | F              | Indexing in vocabulary catalog (1)                        |                                    | 1     |
| RF4                 | A              | URLs use universally accessible protocols (1)             |                                    | 1     |
| RF5                 | A              | Backup (1)                                                |                                    | 1     |
| RF6                 | I              |  Machine-actionable serialization (1)                                                          || 1    |
| RF7                 | I              | Schema Conceptual model (1)                               |                                    | 1     |
| RF8                 | I              | Data Properties (0.5); Range and Domain (0.5)                                     |              | 1   |
| RF9                 | I              | Object Properties (0.5); Range and Domain (0.5)                                   |              | 1   |
| RF10                | R              | Term name (0.5); Definition (0.5)                         |                                    | 1     |
| RF11                | R              | Open License (1)                                          |                                    | 1     |
| RF12                | R              | Documentation of Modifications (1)                        |                                    | 1     |
| RF13                | I (50%) R (50%)| Schema reuse (1)                                          |                                    | 1     |

### Calculation:

| Principle F | Principle A | Principle I | Principle R |
|-------------|-------------|-------------|-------------|
| **F = 1 + 1 + 1** | **A = 1 + 1** | **I = 1 + 1 + 1 + 1 + 0.5** | **R = 1 + 1 + 1 + 0.5** |
| F = 3 | A = 2 | I = 4.5 | R = 3.5 |
| PF% = (3 / 3) * 100 | PF% = (2 / 2) * 100 | PF% = (4.5 / 4.5) * 100 | PF% = (3.5 / 3.5) * 100 |
| PF% = 100% | PF% = 100% | PF% = 100% | PF% = 100% |

![image](https://github.com/user-attachments/assets/5d34669e-39b1-4529-9bf8-c4cf1bab8ff9)


### Overall FAIR compliance score (OFC%): 

OFC% = (100 + 100 + 100 + 100) / 4

OFC% = 100%

### Comments:

DCAT Version three is a 100% FAIR metadata schema. All the concepts included in this metrics have been found in the schema documentation. 

## FAIRness assessment of the Almes Core schema

| Ref. FAIR | FAIR P. | Concept present | Concept absent | Score |
|-----------|---------|-----------------|----------------|-------|
| RF1       | F       | Namespace (0.5); version unique identifier (0.5) |                | 1     |
| RF2       | F       | Landing page (0.5); metadata record for humans (0.25); metadata record for machines (0.25) |                | 1     |
| RF3       | F       |                 | Indexing in vocabulary catalog (1) | 0     |
| RF4       | A       | URLs use universally accessible protocols (1) |                | 1     |
| RF5       | A       | Backup (1)      |                | 1     |
| RF6       | I       | Machine-actionable serialization (1) |                | 1     |
| RF7       | I       | Schema Conceptual model (1) |                | 1     |
| RF8       | I       | Data Properties (0.5); Range and Domain (0.5) |                | 1     |
| RF9       | I       | Object Properties (0.5); Range and Domain (0.5) |                | 1     |
| RF10      | R       | Term name (0.5); Definition (0.5) |                | 1     |
| RF11      | R       | Open License (1) |                | 1     |
| RF12      | R       | Documentation of Modifications (1) |                | 1     |
| RF13      | I (50%) R (50%) | Schema reuse (1) |                | 1     |




### Calculation:

| Principle F | Principle A | Principle I | Principle R |
|-------------|-------------|-------------|-------------|
| **F = 1 + 1 + 0** | **A = 1 + 1** | **I = 1 + 1 + 1 + 1 + 0.5** | **R = 1 + 1 + 1 + 0.5** |
| F = 2 | A = 2 | I = 4.5 | R = 3.5 |
| PF% = (2 / 3) * 100 | PF% = (2 / 2) * 100 | PF% = (4.5 / 4.5) * 100 | PF% = (3.5 / 3.5) * 100 |
| PF% ≅ 67% | PF% = 100% | PF% = 100% | PF% = 100% |

![image](https://github.com/user-attachments/assets/2bb3a9bb-64cd-4de4-8ff7-1460f3d6c1d0)

### Overall FAIR compliance score (OFC%): 

OFC% = (67 + 100 + 100 + 100) / 4

OFC% = 91.75%

### Comments:

The only principle that he almes core schema did not reach 100\% was principle F, due to the schema currently not being indexed by any vocabulary catalog, which is crucial for findability.






