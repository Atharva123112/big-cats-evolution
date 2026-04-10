# big-cats-evolution
# Evolutionary Divergence of the Panthera Genus

## Project Overview
This project maps the evolutionary lineage of big cats (Lion, Tiger, Leopard, Jaguar, and Cheetah) using mitochondrial DNA. It features a complete computational biology pipeline, from fetching raw genomic data via API to rendering a custom, interactive phylogenetic tree in the browser.

🔗 **[Click here to view the interactive web visualization!]([https://atharva123112.github.io/big-cats-evolution])**

## The Tech Stack
* **Data Retrieval & Processing:** Python, Biopython (`Entrez` API)
* **Multiple Sequence Alignment (MSA):** Clustal Omega
* **Distance Matrix & Tree Calculation:** UPGMA Algorithm, PhyloXML / Newick parsing
* **Interactive Visualization:** JavaScript, D3.js, HTML/CSS Flexbox
* ## 💻 Run the Data Pipeline
You can view and run the exact Python backend used to fetch the FASTA sequences, perform the Clustal Omega alignment, and calculate the UPGMA matrix by opening the Jupyter Notebook below:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Atharva123112/big-cats-evolution/blob/main/data_processing_pipeline.ipynb)

## The Workflow
1. **Data Collection:** Extracted complete mitochondrial genomes (approx. 16,000 base pairs each) for five species from the NCBI Nucleotide database.
2. **Alignment:** Processed the raw FASTA files through Clustal Omega to identify genetic mutations, insertions, and deletions.
3. **Mathematical Clustering:** Calculated the genetic distance matrix and constructed a hierarchical dendrogram using UPGMA.
4. **Web Rendering:** Built a custom D3.js parser to translate the Newick tree data into a dynamic, interactive web dashboard.

## Key Finding: The Outgroup Anomaly
Biologically, the Cheetah (*Acinonyx*) is the true outgroup of this dataset. However, because the UPGMA algorithm assumes a strict molecular clock (constant mutation rate), variations in the Lion's mutation rate caused the algorithm to place the Lion at the base of the tree. This project highlights the critical importance of testing multiple algorithmic models (like Neighbor-Joining or Maximum Likelihood) against biological reality in data science.
