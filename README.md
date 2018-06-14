# python_cheatsheet

# NUMPY:
## Converting list into numpy array:
```python
import numpy as np
break_check=np.asarray(accuray_threshlod)
values=(break_check >=97).sum()
```

===============================================================================
# Pandas:
## Concatenating Data Frames to bottom of another data frame
```python
pd.concat([df_a, df_b])
```
### Stripping and splitting the data frame column into two:
```python
df['Train_Skills_'+str(i)+'_Acc_For S_1'].astype(str).str.strip('{}').str.split(':', expand=True)
```
### Checking the Dataframe for Null or NAN Values
```python
data.isnull().sum()
```
### Filling na with 0
```python
data['square_feet'].fillna(0)
```
### Replacing null values with the mean
```python
data['column']=data['column'].fillna(data['column'].mean())
```
### Replacing dollar before any price $60 to 60
```python
data['price']=data['price'].replace( '[\$,)]','', regex=True ).astype(float)
```
### merging columns in dataframe
```python
df['combined_description'] = df.apply(lambda x: '{} {} {} {}'.format(x['name'], x['space'], x['description'], x['neighborhood_overview']), axis=1)
```
### Filtering Column in pandas dataframe
```python
Square_foot[Square_foot['square_feet']<=3000]
```
### Group by column then into a dataframe
```python
pd.DataFrame(Square_foot.groupby('square_feet',as_index=False).mean())
```
### Changing type of column
```python
reviews['review_scores_rating'].astype(float)
```
### unique value in Column to list
```python
Final_Evaluation['zipcode'].unique().tolist()
```
### Selecting only specific indexes in dataframe
```python
select_indicies=[2,3,4,5]
data['latitude'].iloc[select_indices]
```
### Deleting Column in pandas dataframe
```python
del(df['columnname'])
```
### Deleting Column in pandas dataframe
```python
del(df['columnname'])
```
### Deleting Column in pandas dataframe
```python
del(df['columnname'])
```
================================================================================
# List:
#### List of Lists into Pandas Data frame: (Need to run both the below lines in the case of list of lists)
```python
        df = pd.DataFrame(accuracy_collection)
        df = df.transpose()
```      
-------------------------------------------------------------------------

### CREATE N DYNAMIC LISTS
```python
for i in range(len(train_classes)):
    command = "" # this line is here to clear out the previous command
    command = "list" + str(i) + " = []"

    exec(command)
```
### MERGING LISTS
```python
>>> import itertools
>>> list2d = [[1,2,3],[4,5,6], [7], [8,9]]
>>> merged = list(itertools.chain(*list2d))

```
================================================================================
# List of Lists :
```python
accuracy_collection=[[] for _ in range(0,len(task_samples))]

Appending Dictionary to a list in list of lists:
accuracy_collection[i].append({int(s))
```
