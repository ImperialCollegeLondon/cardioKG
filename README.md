## CardioKG - A multi-modal vision knowledge graph of cardiovascular disease
Knowledge graph (KG) is a structured representation of knowledge in a graph format, consisting of nodes, which represent entities or concepts, and edges, which represent the relationships between those entities. It’s a way of organizing and representing information to facilitate machine understanding and reasoning. In a knowledge graph, entities are represented as nodes, relationships as edges, and attributes as properties of nodes or edges. This structure allows for flexible querying and inference, making it useful for various applications such as semantic search, data integration, recommendation systems, and more. Knowledge graphs are particularly valuable in capturing complex relationships and semantics inherent in data, enabling more advanced forms of artificial intelligence and knowledge discovery. In healthcare, a knowledge graph serves as a powerful tool for organising, integrating, and analysing vast amounts of medical information. It enables healthcare professionals, researchers, and AI systems to efficiently access, understand, and utilize complex medical knowledge and relationships such as gene-disease association. 

### Data extraction and preparation:
To build the knowledge graph, we extracted the data (including entities/nodes, relationships/edges and properties/features) from 19 different databses including the UK biobank database. The figure below shows the databases names. Six cardiovascular diseases have been considered and extracted from the UK Biobank including 1) Hypertrophic cardiomyopathy (HCM) , 2) Dilated cardiomyopathy (DCM), 3) Heart failure (HF), 4) Myocardial infarction (MI), 5) Atrial fibrillation (AF), 6) Rheumatic heart disease (RHD).
<br/>
### Installation:
TO run the code properly, we need to install the following software:
<br/>
1. neo4j Desktop v 5.20.0
2. Python v 3.12.1
3. Anaconda3 2023.09-0
4. In Jupyter notebook, install ne4j and neo4jupyter libraries:
   
```bash
!pip install neo4j
!pip install neo4jupyter
```
### Connecting Jupyter notebook to neo4j:
1. Run neo4j desktop.
2. Run Jupyter notebook from Anaconda.
3. In Jupyter notebook, run the follwing code:
 ```python
from graphdatascience import GraphDataScience
from neo4j import GraphDatabase
uri = "bolt://localhost:7687"
user = "neo4j"
password= "*********"
gds = GraphDataScience(uri, auth=(user, password))

```

### Predicting novel gene-disease association:
#### 1.Heart Failure:
##### A.Using CMR features:
1. We need to run the cypher code ```plaintext cypher_for_creating_nodes.txt``` in the ```Building KG``` folder using ```neo4j``` browser. Then, we need to add the edges between the created nodes by running the cypher code in ```Cypher_to_add_edges_between_nodes.txt```. After running the two cypher codes, the KG will be created.
2. To generate he embeddings, we need to run the Jupyter notebook ```Generate_embeddings_aftre_adding_CMR_as_nodes_shared.ipynb``` in ```Predicting gene-disease association (HF)\Using CMR features``` folder.
3. To predict the gene-diases association, run ```Predicting_gene_diseas_assoc_aftre_adding_CMR.ipynb``` in ```Predicting gene-disease association (HF)\Using CMR features``` folder.
4. After predicting the genes, we pick the top ten predicted genes and perform the enrichment analysis using ```g:profiler```.

### Citation:
Rjoob K, McGurk KA, Zheng SL, Curran L, Ibrahim M, Zeng L, Kim V, Tahasildar S, Kalaie S, Senevirathne DS, Gifani P, Losev V, Zheng J, Bai W, de Marvao A, Ware JS, Bender C, O’Regan DP. A multi-modal vision knowledge graph of cardiovascular disease. _medRxiv_. 2025
   
