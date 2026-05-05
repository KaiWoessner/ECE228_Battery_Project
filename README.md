Initial code from https://github.com/rdbraatz/data-driven-prediction-of-battery-cycle-life-before-capacity-degradation \
Data used from the “Data-driven prediction of battery cycle life before capacity degradation” publication: 
- Severson et al. Data-driven prediction of battery cycle life before capacity degradation. Nature Energy volume 4, pages 383–391 (2019)

# Setup Steps
1. Download initial .mat data: 
- Batch1: https://data.matr.io/1/projects/5c48dd2bc625d700019f3204/batches/5c86c0b5fa2ede00015ddf67
- Batch2: https://data.matr.io/1/projects/5c48dd2bc625d700019f3204/batches/5c86bf14fa2ede00015ddd83
- Batch3: https://data.matr.io/1/projects/5c48dd2bc625d700019f3204/batches/5c86bd64fa2ede00015ddbb3
2. Place data files in ```data``` folder
3. Run ```build_pkl.ipynb```. This will create the batch pkl files.
4. Run ```load_df.ipynb```. This will create the bat_df.pkl (WILL PROBABLY COMBINE THE TWO SCRIPTS LATER)

Now have the dataframe needed to run the ```analysis_graphs.ipynb``` file
