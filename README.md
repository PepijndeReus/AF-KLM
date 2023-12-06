# AF-KLM
This repo contains the code for my research project as an intern at Air France-KLM. We aimed to create realistic synthetic data to expand the CMAPSS data set with manual insertion of errors. The methods DataSynthesizer and Synthetic Data Vault were not able to do so, both lacking the ability to model linear patterns over time. For the manual insertion of errors, the impact of the introduced error should be known such that the synthetic data can be labelled accordingly. This implies that the impact on RUL must be known for each error, which is exactly what we are trying to examine. Various related papers show problems with infrequent, rare events in synthetic data. More research should aim to create synthetic data in timeseries or sequential settings with rare events.

## Structure
To keep the repository compact, both the CMAPSS data as well as the synthetic data are in this repository. Instructions to reproduce the code follow later in this file.
* [Exploratory data analysis](https://github.com/PepijndeReus/AF-KLM/blob/main/RUL-baseline.ipynb) contains the notebook for the exploratory data analysis and RUL prediction with the original data.
* [DataSynthesizer](https://github.com/PepijndeReus/AF-KLM/blob/main/DataSynthesizer.ipynb) contains the notebook to generate synthetic data using DataSynthesizer.
* [SDV](https://github.com/PepijndeReus/AF-KLM/blob/main/SDV.ipynb) contains the notebook to generate synthetic data using DataSynthesizer.

For each RUL prediction on synthetic data we have a separate notebook as RUL-"name method".

## Dependencies
.yml file for conda

## Running the code
1. First, download the C-MAPSS data from [Kaggle](https://www.kaggle.com/datasets/behrad3d/nasa-cmaps).
2. Unzip the data in a folder named 'CMAPSS'
3. Install the conda using the command "conda env create -f environment.yml"
4. Activate the environment using "conda activate KLM"
5. Run the Jupyter notebooks for each given task using "Jupyter Notebook"
6. Create the synthetic data using "DataSynthesizer.ipynb" and "SDV.ipynb"
7. Perform RUL predictions using the three RUL prediction notebooks

## Closing remark
All files should have sufficient documentation for reproduction and understanding. Any remaining questions or comments may be sent to [my e-mail](mailto:pepijn.dereus@proton.me).
