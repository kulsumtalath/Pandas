```python
import pandas as pd
```


```python
df=pd.read_csv("Titanic_R.csv")
```


```python
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>pclass</th>
      <th>survived</th>
      <th>Residence</th>
      <th>name</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>ticket</th>
      <th>fare</th>
      <th>cabin</th>
      <th>embarked</th>
      <th>boat</th>
      <th>body</th>
      <th>home.dest</th>
      <th>Gender</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>Abbing, Mr. Anthony</td>
      <td>42</td>
      <td>0</td>
      <td>0</td>
      <td>C.A. 5547</td>
      <td>7.55</td>
      <td></td>
      <td>S</td>
      <td></td>
      <td></td>
      <td></td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>Abbott, Master. Eugene Joseph</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
      <td>C.A. 2673</td>
      <td>20.25</td>
      <td></td>
      <td>S</td>
      <td></td>
      <td></td>
      <td>East Providence, RI</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>Abbott, Mr. Rossmore Edward</td>
      <td>16</td>
      <td>1</td>
      <td>1</td>
      <td>C.A. 2673</td>
      <td>20.25</td>
      <td></td>
      <td>S</td>
      <td></td>
      <td>190</td>
      <td>East Providence, RI</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>1</td>
      <td>0</td>
      <td>Abbott, Mrs. Stanton (Rosa Hunt)</td>
      <td>35</td>
      <td>1</td>
      <td>1</td>
      <td>C.A. 2673</td>
      <td>20.25</td>
      <td></td>
      <td>S</td>
      <td>A</td>
      <td></td>
      <td>East Providence, RI</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>3</td>
      <td>1</td>
      <td>2</td>
      <td>Abelseth, Miss. Karen Marie</td>
      <td>16</td>
      <td>0</td>
      <td>0</td>
      <td>348125</td>
      <td>7.65</td>
      <td></td>
      <td>S</td>
      <td>16</td>
      <td></td>
      <td>Norway Los Angeles, CA</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
type(df)
```




    pandas.core.frame.DataFrame




```python
df.shape
```




    (1309, 15)




```python
df.info
```




    <bound method DataFrame.info of       pclass  survived  Residence                              name   age  \
    0          3         0          0               Abbing, Mr. Anthony    42   
    1          3         0          0     Abbott, Master. Eugene Joseph    13   
    2          3         0          0       Abbott, Mr. Rossmore Edward    16   
    3          3         1          0  Abbott, Mrs. Stanton (Rosa Hunt)    35   
    4          3         1          2       Abelseth, Miss. Karen Marie    16   
    ...      ...       ...        ...                               ...   ...   
    1304       3         0          2              Zabour, Miss. Hileni  14.5   
    1305       3         0          2             Zabour, Miss. Thamine         
    1306       3         0          2         Zakarian, Mr. Mapriededer  26.5   
    1307       3         0          2               Zakarian, Mr. Ortin    27   
    1308       3         0          2                Zimmerman, Mr. Leo    29   
    
          sibsp  parch     ticket     fare cabin embarked boat body  \
    0         0      0  C.A. 5547     7.55              S             
    1         0      2  C.A. 2673    20.25              S             
    2         1      1  C.A. 2673    20.25              S       190   
    3         1      1  C.A. 2673    20.25              S    A        
    4         0      0     348125     7.65              S   16        
    ...     ...    ...        ...      ...   ...      ...  ...  ...   
    1304      1      0       2665  14.4542              C       328   
    1305      1      0       2665  14.4542              C             
    1306      0      0       2656    7.225              C       304   
    1307      0      0       2670    7.225              C             
    1308      0      0     315082    7.875              S             
    
                       home.dest  Gender  
    0                                  0  
    1        East Providence, RI       0  
    2        East Providence, RI       0  
    3        East Providence, RI       1  
    4     Norway Los Angeles, CA       1  
    ...                      ...     ...  
    1304                               1  
    1305                               1  
    1306                               0  
    1307                               0  
    1308                               0  
    
    [1309 rows x 15 columns]>




```python
df.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>pclass</th>
      <th>survived</th>
      <th>Residence</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>Gender</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>1309.000000</td>
      <td>1309.000000</td>
      <td>1309.000000</td>
      <td>1309.000000</td>
      <td>1309.000000</td>
      <td>1309.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2.294882</td>
      <td>0.381971</td>
      <td>1.375095</td>
      <td>0.498854</td>
      <td>0.385027</td>
      <td>0.355997</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.837836</td>
      <td>0.486055</td>
      <td>0.793142</td>
      <td>1.041658</td>
      <td>0.865560</td>
      <td>0.478997</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>3.000000</td>
      <td>0.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>3.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>3.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>8.000000</td>
      <td>9.000000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df['age'][0:10]
```




    0    42
    1    13
    2    16
    3    35
    4    16
    5    25
    6    30
    7    28
    8    20
    9    18
    Name: age, dtype: object




```python
df.age[0:10]
```




    0    42
    1    13
    2    16
    3    35
    4    16
    5    25
    6    30
    7    28
    8    20
    9    18
    Name: age, dtype: object




```python
df['survived'].mean()
```




    0.3819709702062643




```python
df['survived'].median()
```




    0.0




```python
df['survived'].std()
```




    0.48605517086648126




```python
df[['Gender']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Gender</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>1304</th>
      <td>1</td>
    </tr>
    <tr>
      <th>1305</th>
      <td>1</td>
    </tr>
    <tr>
      <th>1306</th>
      <td>0</td>
    </tr>
    <tr>
      <th>1307</th>
      <td>0</td>
    </tr>
    <tr>
      <th>1308</th>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>1309 rows × 1 columns</p>
</div>




```python
df['age'].dtypes
```




    dtype('O')




```python
print (df.dtypes)
```

    pclass        int64
    survived      int64
    Residence     int64
    name         object
    age          object
    sibsp         int64
    parch         int64
    ticket       object
    fare         object
    cabin        object
    embarked     object
    boat         object
    body         object
    home.dest    object
    Gender        int64
    dtype: object
    


```python
df["age"] = df["age"].astype(str).astype(int)
print(df.dtypes)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-33-7d4949bb496b> in <module>
    ----> 1 df["age"] = df["age"].astype(str).astype(int)
          2 print(df.dtypes)
    

    ~\AppData\Roaming\Python\Python38\site-packages\pandas\core\generic.py in astype(self, dtype, copy, errors)
       5544         else:
       5545             # else, only a single dtype is given
    -> 5546             new_data = self._mgr.astype(dtype=dtype, copy=copy, errors=errors,)
       5547             return self._constructor(new_data).__finalize__(self, method="astype")
       5548 
    

    ~\AppData\Roaming\Python\Python38\site-packages\pandas\core\internals\managers.py in astype(self, dtype, copy, errors)
        593         self, dtype, copy: bool = False, errors: str = "raise"
        594     ) -> "BlockManager":
    --> 595         return self.apply("astype", dtype=dtype, copy=copy, errors=errors)
        596 
        597     def convert(
    

    ~\AppData\Roaming\Python\Python38\site-packages\pandas\core\internals\managers.py in apply(self, f, align_keys, **kwargs)
        404                 applied = b.apply(f, **kwargs)
        405             else:
    --> 406                 applied = getattr(b, f)(**kwargs)
        407             result_blocks = _extend_blocks(applied, result_blocks)
        408 
    

    ~\AppData\Roaming\Python\Python38\site-packages\pandas\core\internals\blocks.py in astype(self, dtype, copy, errors)
        593             vals1d = values.ravel()
        594             try:
    --> 595                 values = astype_nansafe(vals1d, dtype, copy=True)
        596             except (ValueError, TypeError):
        597                 # e.g. astype_nansafe can fail on object-dtype of strings
    

    ~\AppData\Roaming\Python\Python38\site-packages\pandas\core\dtypes\cast.py in astype_nansafe(arr, dtype, copy, skipna)
        970         # work around NumPy brokenness, #1987
        971         if np.issubdtype(dtype.type, np.integer):
    --> 972             return lib.astype_intsafe(arr.ravel(), dtype).reshape(arr.shape)
        973 
        974         # if we have a datetime/timedelta array of objects
    

    pandas\_libs\lib.pyx in pandas._libs.lib.astype_intsafe()
    

    ValueError: invalid literal for int() with base 10: '.8333'



```python
df[df['age'].isnull()]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>pclass</th>
      <th>survived</th>
      <th>Residence</th>
      <th>name</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>ticket</th>
      <th>fare</th>
      <th>cabin</th>
      <th>embarked</th>
      <th>boat</th>
      <th>body</th>
      <th>home.dest</th>
      <th>Gender</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
my_series=df['pclass']
```


```python
my_series.value_counts()
```




    3    709
    1    323
    2    277
    Name: pclass, dtype: int64




```python
pd.crosstab(df['Gender'],df['pclass'])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>pclass</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>179</td>
      <td>171</td>
      <td>493</td>
    </tr>
    <tr>
      <th>1</th>
      <td>144</td>
      <td>106</td>
      <td>216</td>
    </tr>
  </tbody>
</table>
</div>




```python
df['pclass']=df['sibsp']+df['parch']
```


```python
df['pclass']

```




    0       0
    1       2
    2       2
    3       2
    4       0
           ..
    1304    1
    1305    1
    1306    0
    1307    0
    1308    0
    Name: pclass, Length: 1309, dtype: int64




```python
import numpy as np
data=pd.DataFrame(np.arange(16).reshape((4,4)),index=['india','china','newyork','srilanka'],columns=['one','two','three','four'])
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>two</th>
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>india</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>china</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>newyork</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <th>srilanka</th>
      <td>12</td>
      <td>13</td>
      <td>14</td>
      <td>15</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.drop(['srilanka'])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>two</th>
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>india</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>china</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>newyork</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.drop('two',axis=1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>india</th>
      <td>0</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>china</th>
      <td>4</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>newyork</th>
      <td>8</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <th>srilanka</th>
      <td>12</td>
      <td>14</td>
      <td>15</td>
    </tr>
  </tbody>
</table>
</div>




```python
string_data=(['apple','boy',np.nan,'cat','dog'])
```


```python
string_data1 =pd.Series(['aardvark', 'artichoke', np.nan, 'avocado']) 
```


```python
string_data1.dropna(inplace=True)
```


```python
string_data1 
```




    0     aardvark
    1    artichoke
    3      avocado
    dtype: object




```python
string_data1[0]=None
```


```python
string_data1 
```




    0         None
    1    artichoke
    3      avocado
    dtype: object




```python
string_data1 .isnull()
```




    0     True
    1    False
    3    False
    dtype: bool




```python
string_data1 .dropna()
```




    1    artichoke
    3      avocado
    dtype: object




```python
string_data1[string_data1.notnull()]
```




    1    artichoke
    3      avocado
    dtype: object




```python
cleaned=string_data1 .dropna()
```


```python
cleaned
```




    1    artichoke
    3      avocado
    dtype: object




```python
df1=pd.DataFrame({'key':['b','b','a','c','b','a'],'data1':range(6)})
df1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>key</th>
      <th>data1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>b</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>b</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>a</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>c</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>b</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>a</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2=pd.DataFrame({'key':['a','b','d'],'data2':range(3)})
df2
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>key</th>
      <th>data2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>a</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>b</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>d</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.merge(df1,df2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>key</th>
      <th>data1</th>
      <th>data2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>b</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>b</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>b</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>a</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>a</td>
      <td>5</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3=pd.DataFrame({'key':['a','b','d'],'data2':range(3)})
```


```python
df4=pd.DataFrame({'key':['a','b','c'],'data2':range(3)})
```


```python
pd.merge(df3,df4,how="inner")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>key</th>
      <th>data2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>a</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>b</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.merge(df3,df4,how="outer")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>key</th>
      <th>data2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>a</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>b</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>d</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>c</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>




```python
c=0
num=int(input("enter the number:"))
while(num>0):
    r=num%10
    num=num//10
    c=c+1
print("total count:",c)    
```

    enter the number:123
    


```python
num=int(input("Enter a number:"))
temp=num
rev=0
while(num>0):
    dig=num%10
    rev=rev*10+dig
    num=num//10
if(temp==rev):
    print("The number is palindrome!")
else:
    print("Not a palindrome!")

```


```python

```
