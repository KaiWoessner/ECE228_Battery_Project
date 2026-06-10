# ECE228 Battery Health Prediction Project 

This repository contains the data processing, data analysis, and model code for our ECE 228 Battery Health Prediction project. The project follows Track 1: Reproduce Results and builds on the data and methodology from:

> Severson et al. Data-driven prediction of battery cycle life before capacity degradation. Nature Energy volume 4, pages 383–391 (2019)

The Severson paper's GitHub repository can be found here: https://github.com/rdbraatz/data-driven-prediction-of-battery-cycle-life-before-capacity-degradation. It provided the scaffolding for the data preprocessing and the train, primary test, and secondary test splits used for each model

## Models
- Linear Model (ElasticNet)
- Multilayer Perceptron (MLP)
- Gated Recurrent Unit (GRU)
- Fourier Neural Operator (FNO)

## Repo Strucutre
The home directory contains the data analysis folder (`data_analysis`), the folder to load the dataset as a pandas dataframe (`data_loading`), the 4 different models that were tested (Linear, MLP, GRU, FNO), and the final model results across all models (`final_model_results.ipynb`)

## Data Source
The initial data comes from a public dataset developed for and used in the Severson paper:
- Batch1: https://data.matr.io/1/projects/5c48dd2bc625d700019f3204/batches/5c86c0b5fa2ede00015ddf67
- Batch2: https://data.matr.io/1/projects/5c48dd2bc625d700019f3204/batches/5c86bf14fa2ede00015ddd83
- Batch3: https://data.matr.io/1/projects/5c48dd2bc625d700019f3204/batches/5c86bd64fa2ede00015ddbb3

Download the `.mat` file from each of the links above (they are about 2-3 GB each) and place them into a local `data` folder in the root of this repository.

## Setup Steps
1. Clone this repository: `git clone https://github.com/KaiWoessner/ECE228_Battery_Project.git`. Then create a virtual environment and download any depedencies that are required.
2. Create the `data` folder and add the batch files as instructed above
3. Run `data_loading/build_pkl.ipynb`. This notebook will convert the raw `.mat` data files in batch `pkl` files. 
4. Run `data_loading/load_df.ipynb`. This will combine and process the batch `pkl` files into a final `pkl` file called `bat_df.pkl` used by the models.

Now the environment and model dataset is setup and can be used to run the various models and dataset analysis graphs

### AI Disclosure
AI was used to help convert the outdated code used in the original paper, give coding syntax, and help provide general PyTorch code for the models
