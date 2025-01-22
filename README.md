# OVERVIEW:
Built a dataframe for the TikTok dataset using Python packages - **NumPy and Pandas** 

# Case Study 1: TikTok 🎵
## Link here: [Case_study_1: TikTok](https://github.com/amy941/Google_Advanced_Module-2_Python/blob/main/Case%20Study%202_TikTok.ipynb)

## Scenario:
Constructing a dataframe in Python for data learning and future Exploratory Data Analysis (EDA) and statistical activities.

## What I Learned:
**1) Imports and data loading:**
```python
import numpy as np
import pandas as pd
```

```python
data = pd.read_csv("tiktok_dataset.csv")
```
✍️ Importing NumPy and Panda packages, then load dataset from CSV file to a dataframe.

---
**2) Inspect the data:**
```python
data.head(10)
data.info()
data.describe()
```

![head()](https://github.com/user-attachments/assets/77200b7a-3eca-486b-af2e-1171fc5f1b65)

✍️ *.head()* is used to display a few first rows of df. Reviewing the first few rows, we can tell **df contains different data types (str, int, floats).** Each row represents a distinct TikTok video with comments and statuses. 


![info()](https://github.com/user-attachments/assets/145e3092-8493-4ed5-969a-2dcd6c8ed669)

✍️ *.info()* is for summary info. The output shows df contains **5 floats, 3 integers, and 4 objects.** Total video counts is **19382 videos**. There are some **missing values** in variables as 'claim_status', 'video_transcription_text', and all 'count' variables.


![describe()](https://github.com/user-attachments/assets/2c234a9d-8059-45f4-b39a-8381b3be542a)

✍️ .describe()* is for descriptive statistics summary. **Many 'count' variables have outliers.**

---
**3) Investigate the variables:**


# Case Study 3: Automatidata 🚕
## Link here: [Case_study_2: Automatidata](https://github.com/amy941/Google_Advanced_Module-2_Python/blob/main/Case%20Study%201_Automatidata.ipynb)
