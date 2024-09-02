# Neo4j GenAI Workshop

Please see [`genai-workshop.ipynb`](genai-workshop.ipynb) which serves as the self-contained workshop. 

The other companion notebooks contain code for staging data, building the Neo4j Graph, and providing easy access to demos:
1. [`data-prep.ipynb`](data-prep.ipynb) stages the workshop data, sampling and formatting data sourced from the [H&M Personalized Fashion Recommendations Dataset](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data).
2. [`data-load.ipynb`](data-load.ipynb) loads the staged data into Neo4j, performs text embedding, and creates a vector index.
3. [`genai-example-app-only.ipynb`](genai-example-app-only.ipynb) is a copy of [`genai-workshop.ipynb`](genai-workshop.ipynb)  that contains only the final section: the demo LLM GraphRAG app for content generation. It assumes you have already run [`genai-workshop.ipynb`](genai-workshop.ipynb), and exists only for instructor demo purposes.


## Changelog

### v4 (Sep 2nd, 2024 - Present)

------------
- Transition from using Neo4j Sandbox to AuraDS


- Split out data loading
  - Split out data load into separate notebook
    - Live workshops now begin with the dataset pre-loaded to cut down on time and spend more of the course walking through GraphRAG. the data-load.ipynb is kept for reference and replication. 
    - Remove `neo4j_tools` Python package. the functions/utilities are now included in data-load.ipynb


- Added more query exploration & improved explainer queries
  - Add Browser-based graph exploration in beginning of workshop
  - Include database tips & more Cypher queries in multiple steps
  - Update explainer markdown and code cells for graph patterns and GDS for clarity
  - Various other minor adjustments to markdown and code to improve course quality

### [v3 (June 25th, 2024 - Sep 1st, 2024)](https://github.com/neo4j-product-examples/genai-workshop/releases/tag/v3.0)

------------
- improve LLM response quality and cleaned up code for LLM chains and vector stores
  - parameterizing customer id so don't need to recreate chains & stores for each customer
  - updated prompts to better account for seasonality and use all retrieved data
  - update to use gpt-4o


- Improve text embedding speed and reduce code by transitioning to native `genai.vector` Cypher functions


- Updated slides


- Various other minor adjustments to markdown and code to improve course quality

### [v2 (Feb 20th, 2024 - June 24th, 2024)](https://github.com/neo4j-product-examples/genai-workshop/releases/tag/v2.0)

------------

- (fix) Add `langchain_community` to the libraries that are pip installed in the notebooks


- Simplify and Shorten Course
  - Shortened GDS section to just three cells to run 
  - Condensed Vector Search Section
  - Condensed Loading to Single Notebook Cell
  - Switched Recommendation Retriever to a Simple KG Query
  - Adding `neo4j_tools` Package to hold convenience functions for loading data and reduce code footprint in main workshop notebook
  - Updated to GPT-4 throughout
  - General Notebook Cleaning - Removed duplicate load statements, updating to newest llm packages, etc. 


- Provide Better Explainers & Examples
  - Add A Chain for Printing Final Prompt to LLM with retrieval data to better explain process. 
  - Added Differentiated Names for Customer Examples in Demo App.


- Added Additional Resources
  - Added workshop slides
  - Added "demo only" notebook


### [v1 (Nov 13th, 2023 - Feb 19th, 2024)](https://github.com/neo4j-product-examples/genai-workshop/releases/tag/v1.0)

------------

- Initial 5-part course with
  - Building the knowledge graph
  - Vector search & text embedding
  - Graph patterns to improve semantic search
  - knowledge graph inference & ML
  - Building the LLM chain and demo app for generating content
