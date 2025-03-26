# League of Legends Dataset Analysis

## Setup

This analysis uses the cuDF library, which is a GPU-boosting data science library.\
 From their website: cuDF (pronounced “KOO-dee-eff”) is a Python GPU DataFrame library (built on the Apache Arrow columnar memory format) for loading, joining, aggregating, filtering, and otherwise manipulating data. cuDF also provides a pandas-like API that will be familiar to data engineers & data scientists, so they can use it to easily accelerate their workflows without going into the details of CUDA programming.

Usage of this library requires a Linux environment. The analysis was done on a Windows operating system using [WSL2 Conda](https://docs.rapids.ai/install/#wsl2-conda) to download the RAPIDS framework to a local Linux installation.  

In addition, [DVC](https://dvc.org/doc/install) is used to manage data versions for different use cases. Versions evolve as the scope of a research question is explored, and data will change as it is molded for machine learning algorithms. The file `initial_EDA.ipynb` begins the construction of a lakeFS client using the Python API, allowing for clarity on the content of different versions.

## Data

This data is sourced from [Huggingface](https://huggingface.co/datasets/renecotyfanboy/leagueData), and contains 300k individual matches gathered from the RiotAPI across all ranked divisions. The data was gathered on April 9th, 2024. 

## Types of Analysis

The analyses contained in this repository will cover multiple research questions, including:

- What are the main factors that contribute to a team's win?
- What are the key player performance differences across ranked divisions?
- Can a player's ranked division be predicted by their game performance?
- What are the most popular items that players build? 
- What determines a 'meta' pick for champions?
- How does vision control of the map contribute to wins?
