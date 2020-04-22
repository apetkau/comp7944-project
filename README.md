# COMP 7944 Project

This project involves applying data mining techniques on COVID-19 data to extract association rules and visualize these rules as a network. This repository includes code and supplementary materials for the project.

# Authors

Prepared for COMP 7944 at the University of Manitoba on April 23, 2020 by:

* Aaron Petkau
* Hosne Al Walid Shaiket
* Rahatul Amin Ananto

# Interative visualizations

Below lists all the interactive versions of our visualization of association rules (as a network). For each dataset we produced two networks, one where nodes are colored by **confidence** and the other where nodes are colored by **lift**.

1. Symptoms rules network
  1. [Symptoms rules (confidence)](https://apetkau.github.io/comp7944-project/symptoms-rules-confidence.html)
  2. [Symptoms rules (lift)](https://apetkau.github.io/comp7944-project/symptoms-rules-lift.html)
2. Geographic date network
  1. [Geographic date rules (confidence)](https://apetkau.github.io/comp7944-project/geo-date-rules-confidence.html)
  2. [Geographic date rules (lift)](https://apetkau.github.io/comp7944-project/geo-date-rules-lift.html)
3. Geographic age network
  1. [Geographic age rules (confidence)](https://apetkau.github.io/comp7944-project/geo-age-rules-confidence.html)
  2. [Geographic age rules (lift)](https://apetkau.github.io/comp7944-project/geo-age-rules-lift.html)
4. SNV/Genomics network
  1. [Single Nucleotide Variant rules (confidence)](https://apetkau.github.io/comp7944-project/snv-rules-confidence.html)
  2. [Single Nucleotide Variant rules (lift)](https://apetkau.github.io/comp7944-project/snv-rules-lift.html)

# Data sources

Copies of the two datasets we are using can be found at:

1. Epidemiological dataset: [data/nCoV2019/original](data/nCoV2019/original)
  2. Cleaned data for further analysis: [data/nCoV2019/for_use](data/nCoV2019/for_use)
2. Genomics (SNV) dataset: [data/snv-data/original](data/snv-data/original)

# Defining transaction datasets for mining

We processed the above datasets to define sets of items (transactions) for use with the Apriori algorithm for finding frequent itemsets and association rules. We constructed 4 separate transactional itemsets for further processing. Jupyter notebooks for processing this data is given below.

1. [Epidemiological dataset (code)](data/nCoV2019/for_use/extract-transactions.ipynb)
  1. Used to define the **Symptoms**, **Geographic date**, and **Geographic age** transactional itemsets for processing.
2. [Genomics/SNV dataset (code)](data/snv-data/for_use/snv-extract-transactions.ipynb)
  1. Used to define the SNV/genomics dataset transactions.
    
# Association rule mining and visualization

We next applied data mining techniques to find association rules in the above datasets and visualize the rules. Jupyter notebooks for this process are given below.

1. [Symptoms dataset (code)](analysis/symptom/symptoms-mining.ipynb)
2. [Geographic date dataset (code)](analysis/geo-date/geo_date_mining.ipynb)
3. [Geographic age dataset (code)](analysis/geo-age/geo_age_mining.ipynb)
4. [Genomics/SNV dataset (code)](analysis/snv-data/snv-mining.ipynb)
  1. [Phylogenetic tree construction (code)](analysis/snv-data/phylo-tree.ipynb)

# Software

To reproduce this analysis you can use the following instructions to install dependencies using conda (though we note some additional R packages may need to be installed manually).

1. Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) used for software dependency management.
2. Install dependencies (from `dependencies.conda` file) using the command:

   ```bash
   conda create --name datamining --file dependencies.conda
   ```

3. Activate the conda environment with installed software:

   ```bash
   conda activate datamining
   ```

4. Run Jupyter lab.

   ```bash
   jupyter lab
   ```

You should now be able to load up the Juptyer notebooks and work with them.

# License

The source data for this project (under the `data/` directory) is redistributed under the respective licenses of the original providers. The code in this project is distributed under the Apache 2.0 license.
