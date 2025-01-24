# OVERVIEW:
Built a dataframe for the TikTok dataset using Python packages - **NumPy and Pandas** 

# Case Study 1: TikTok 🎵
## Link here: [Case_study_1: TikTok](https://github.com/amy941/Google_Advanced_Module-2_Python/blob/main/Case%20Study%202_TikTok.ipynb)

## Scenario:
Constructing a dataframe in Python for data learning, future Exploratory Data Analysis (EDA), and statistical activities.

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

✍️ *.describe()* is for descriptive statistics summary. **Many 'count' variables have outliers.**

---
**3) Investigate the variables:**

```python
claims = data[data['claim_status'] == 'claim']

print('MEAN view count claims: ', claims['video_view_count'].mean())
print('MEDIAN view count claims: ', claims['video_view_count'].median())
```

![claims](https://github.com/user-attachments/assets/9c3f075f-6e51-424e-af13-a277696481fd)

✍️ First, examine the amount of videos for each different claim status (claims vs. opinions).
Next, create **BOOLEAN masking** to *filter* the data according to claim status, then determine **MEAN** and **MEDIAN** view counts for each claim status. 

**- Step 1:** Assign a **dataframe** called 'claims'.
**- Step 2:** Use selector brackets [] to select a specific column, in this case, 'claim_status' column. **BOOLEAN masking** '[data['claim_status'] == 'claim']' will apply *a filter* to a df, selecting only the rows that align with TRUE values of the BOOLEAN condition.
**- Step 3:** After filtering df to include only the 'claims', output the statistical values using *.mean()* and *.median()* method.
  
🔁 Repeat the same steps for 'opinions' status.

```python
opinions = data[data['claim_status'] == 'opinion']

print('MEAN view count opinions: ', opinions['video_view_count'].mean())
print('MEDIAN view count opinions: ', opinions['video_view_count'].median())
```

![opinions](.....................)

**4) Grouping and Aggregation:**

```python
data.groupby(['claim_status', 'author_ban_status']).agg({
    'likes_per_view': ['count', 'mean', 'median'],
    'comments_per_view': ['count', 'mean', 'median'],
    'shares_per_view': ['count', 'mean', 'median']
})
```

![groupby](https://github.com/user-attachments/assets/d722f2bf-ad36-4ba8-a568-84e8faf21183)

✍️ **groupby()** was called directly on df. The data was grouped first by **claim_status**, then by **author_ban_status**. Then, the **agg()** function was applied to calculate the **count**, **mean**, and **median** for the three newly created columns: *likes_per_view*, *comments_per_view*, and *shares_per_view*.



---
# Case Study 3: Automatidata 🚕
## Link here: [Case_study_2: Automatidata](https://github.com/amy941/Google_Advanced_Module-2_Python/blob/main/Case%20Study%201_Automatidata.ipynb)
