# Ex02-Outlier

# AIM:

To read a given dataset and remove outliers and save a new dataframe.

# ALGORITHM:

(1) Remove outliers using IQR

(2) After removing outliers in step 1, you get a new dataframe.

(3) use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result

(4) for the data set height_weight.csv find the following

(i) Using IQR detect weight outliers and print them

(ii) Using IQR, detect height outliers and print them

# PROGRAM:
```
import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

df = pd.read_csv("/content/heights.csv")

sns.boxplot(data=df)

sns.scatterplot(data=df)

max =df['height'].quantile(0.90)

min =df['height'].quantile(0.15)

max

min

dq = df[((df['height']>=min)&(df['height']<=max))]

dq

low = min-1.5*iqr

high = max+1.5*iqr

dq = df[((df['height']>=min)&(df['height']<=max))]

dq
```

# ZSCORE
```
import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

data = {'weight':[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}

df = pd.DataFrame(data)

df

sns.boxplot(data=df)

z = np.abs(stats.zscore(df))

print(df[z['weight']>3])

val = [12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]

out=[]

def d_o(val):

ts=3

m=np.mean(val)

sd=np.std(val)

for i in val:

z=(i-m)/sd

if np.abs(z)>ts:

  out.append(i)

return out

op = d_o(val)

op

```
# OUTPUT:

<img width="510" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/4baeb615-0cab-4f01-ac0a-f31d46f9a692">




<img width="510" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/c2e40600-8daf-4115-8ab7-aa8f962e0fd6">




<img width="510" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/6a99428f-811a-4aa1-ad4b-3ad034976e21">




<img width="510" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/e3c4a36c-c75a-48e3-8e49-fc28316a3560">




<img width="510" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/dfa970d8-e514-4e42-8da4-b40eebf23116">


<img width="510" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/e20c783f-567e-45ea-be09-3151b2dc53d0">

<img width="510.9" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/b799f75e-5c87-4cee-aca2-72add680f666">



<img width="510" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/4d303037-253e-45a6-b28a-7ac026a44aa4">




<img width="510" alt="image" src="https://github.com/Vineesha29031970/ODD2023---Datascience---Ex-02/assets/133136880/8c8b908c-dee0-4805-b0e3-535e9b52402a">




# RESULT:
Thus, the given data is read,remove outliers and save a new dataframe was created and executed successfully.








