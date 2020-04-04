# COMP 7944 Project

This project involves applying data mining techniques on COVID-19 data to extract association rules and visualize these rules as a network. The datasets we are using are:

* Original data: [nCoV2019/original][]
  * Cleaned data for further analysis: [nCoV2019/for_use][]

# Software

To extract data and perform cleaning we used Python and [Jupyter](https://jupyter.org/). To reproduce this analysis you can do the following:

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
