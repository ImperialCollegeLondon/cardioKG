### Predicting novel gene-disease association using knowledge graph:
Knowledge graph (KG) is a structured representation of knowledge in a graph format, consisting of nodes, which represent entities or concepts, and edges, which represent the relationships between those entities. It’s a way of organizing and representing information to facilitate machine understanding and reasoning. In a knowledge graph, entities are represented as nodes, relationships as edges, and attributes as properties of nodes or edges. This structure allows for flexible querying and inference, making it useful for various applications such as semantic search, data integration, recommendation systems, and more. Knowledge graphs are particularly valuable in capturing complex relationships and semantics inherent in data, enabling more advanced forms of artificial intelligence and knowledge discovery. In healthcare, a knowledge graph serves as a powerful tool for organising, integrating, and analysing vast amounts of medical information. It enables healthcare professionals, researchers, and AI systems to efficiently access, understand, and utilize complex medical knowledge and relationships such as gene-disease association. 

### Data extarctiona and preparation:
To build the knowledge graph, we extracted the data (including entities/nodes, relationships/edges and properties/features) from 19 different databses including the UK biobank database. The figure below shows the databases names. Six cardiovascular diseases have been considered and extracted from the UK Biobank including 1) Hypertrophic cardiomyopathy (HCM) , 2) Dilated cardiomyopathy (DCM), 3) Heart failure (HF), 4) Myocardial infarction (MI), 5) Atrial fibrillation (AF), 6) Rheumatic heart disease (RHD).
<br/>
### Installation:
TO run the code properly, we need to install the following software:
<br/>
1. neo4j Desktop v 5.20.0
2. Python v 3.12.1
3. Anacnda3 2023.09-0
4. In Jupyter notebook, install ne4j and neo4jupyter libraries:
   
```bash
!pip install neo4j
!pip install neo4jupyter
```
### Predicting novel gene-disease association:

#### 1.Heart Filaure:
##### A.Using CMR features:
The CMR features were integratd as nodes in the KG and the value of the CMR features were used as properties on the relationships. To bu 
