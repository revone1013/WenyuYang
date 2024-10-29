Filter the dataset to find required information

After confirming the tools and datasets, the next step is to filter the dataset. Since the datasets are all h5 file that is designed to store single-cell RNA-seq data, it is suitable to use R or python to handle this task. Considering saving the room for local computer, we use Golab at first to test if the analysis will cause crash to this platform. The potential solutions are two. The first one is to run these codes locally for efficiency as well as preventing the crash. However, this method need adequate room for the computer, which is opposite against the primary design. The second one is to apply the High Performance Computing (HPC) system to run the codes with a huge workload. Fortunately, current analysis does not cause crash to hamper our progress, but we still need to prepare for future multiple dataset comparison.
When scanning the data, the key information we find are in feature section including the species (mm10), gene ID (Ensemble ID) and names of genes, which is absolutely inspiring as it satisfies our need to collect necessary information to downloading related sequences from ID mapping section in Uniprot.

Prediction

Since we hope to generate a relative high quality prediction, we tend to set the cutoff (threshold) as a ‘high’ option. After finish prediction from over 10,000 samples, we filter the results and select the protein that are predicted to interact with ERK1 or ERK2, saving them for further analysis.

Further Analysis

When finishing the task of generating list of target protein, we want to define their properties in terms of biological processes, molecular functions and signal pathways. Therefore, it is important selecting a proper ontology knowledgebase. After searching, we find that the Database for Annotation, Visualization and Integrated Discovery (DAVID) knowledgebase is a good option for providing a comprehensive set of functional annotation tools for investigators to understand the biological meaning behind large lists of genes (Huang DW, et al. 2009; B.T. Sherman, et al.2022). Necessary steps including selecting the species, type of gene ID and necessary databases for downloaded.

