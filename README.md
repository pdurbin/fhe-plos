![logo](logo.png)

# Reproduction code for: How much research shared on Facebook is hidden from public view?

> A comparison of public and private online activity around PLOS ONE papers

*Authors: Asura Enkhbayar, Stefanie Haustein, Germana Barata, Juan Pablo Alperin*

| Resource | Link |
|-|-|
| Preprint | TBD |
| Article | TBD |
| Code | [Zenodo (doi:10.5281/zenodo.3381821)](https://doi.org/10.5281/zenodo.3381821)|
| Data | [Dataverse (doi:10.7910/DVN/3CS5ES)](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/3CS5ES)|

---

This repository contains all figures and tables present in the manuscript for "How much research shared on Facebook is hidden from public view?". Output files can be found in:

- `figures/` - contains all figures used in the manuscript
- `tables/` - contains all programmatically created tables used in the manuscript

Furthermore, all the input data and code required to reproduce results are provided with instructions. Provided scripts include:

- `download_data.sh` - to download input data
- `prepare_data.py` - data preprocessing
- `analysis.py` - data analysis and outputs

This article is part of a broader investigation of the hidden engagement on Facebook. More information about the project can be found [here](https://github.com/ScholCommLab/facebook-hidden-engagement).

## Initial Data Collection

The data used in this paper was collected using our own methods. The data collection method is described in [Enkhbayar and Alperin (2018)(https://arxiv.org/abs/1809.01194)]. Code & instructions can be found [here](https://github.com/ScholCommLab/fhe-plos).

## Reproduce results

All scripts have been written with Python 3.x. To explore results interactively a working instance of Jupyter Notebooks/Labs is required.

Packages specified in `requirements.txt` can be installed via

```pip install -r requirements.txt```

1. Clone this repository and cd into the scripts folder

    ```
    git clone git@github.com:ScholCommLab/fhe-plos-paper.git
    cd fhe-plos-paper/scripts
    ```

2. Download data from Dataverse.

    All the data is hosted on dataverse: [Dataverse repository](https://dataverse.harvard.edu/privateurl.xhtml?token=58246dfc-bdf8-454d-8edc-60d5918dedfc)

    Using the helper script provided, you can download all files into the respective locations. Make the script executable and ensure that you have `wget` installed.

    ```
    chmod +x download_data.sh
    ./download_data.sh
    ```

3. Preprocess data

    Run the preprocessing script to apply transformations on the input dataset. This step creates the file `data/articles.csv`

    ```python process_data.py```

4. (Re)produce results

    Run the analysis script to produce figures and tables.

    ```python analysis.py```

    Optionally, you can also open the notebook `analysis.ipynb` with Jupyter to explore the dataset and results.
