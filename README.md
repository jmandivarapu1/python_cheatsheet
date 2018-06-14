# python_cheatsheet
```python
NUMPY:

Converting list into numpy array:
break_check=np.asarray(accuray_threshlod)

No of values in numpy array greater than certain value:
values=(break_check >=97).sum()

==================================================================================================================================
Pandas:
Concatenating Data Frames to bottom of another data frame
pd.concat([df_a, df_b])

Stripping and splitting the data frame column into two:
df['Train_Skills_'+str(i)+'_Acc_For S_1'].astype(str).str.strip('{}').str.split(':', expand=True)

==================================================================================================================================
List:
List of Lists into Pandas Data frame: (Need to run both the below lines in the case of list of lists)
        df = pd.DataFrame(accuracy_collection)
        df = df.transpose()
        
-------------------------------------------------------------------------

CREATE N DYNAMIC LISTS
for i in range(len(train_classes)):
    command = "" # this line is here to clear out the previous command
    command = "list" + str(i) + " = []"

    exec(command)
 
MERGING LISTS
>>> import itertools
>>> list2d = [[1,2,3],[4,5,6], [7], [8,9]]
>>> merged = list(itertools.chain(*list2d))


==============================================================================================================================
List of Lists :
accuracy_collection=[[] for _ in range(0,len(task_samples))]

Appending Dictionary to a list in list of lists:
accuracy_collection[i].append({int(s))
```
