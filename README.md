# **Project**

# *Name: Zia Ahmad*
# *Roll No: 073*

### Topic = DataSets

#### 1. Import Libararies.


```python
import pandas as pd
```


```python
df =pd.read_csv("Serious Fraud.csv.csv")
```

#### 2. Load the Dataset.


```python
def load_data(file_path):
    df = pd.read_csv('Serious Fraud.csv.csv')
    print("Data Loaded Successfully!")
    return df
```


```python
df = load_data('file_path')
```

    Data Loaded Successfully!


#### **Checking Numbers of rows and columns**


```python
df.shape
```




    (448, 9)



#### **Checking some items from Start and End**


```python
df.head(4)
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Andhra Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Arunachal Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Assam</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bihar</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.tail(4)
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>444</th>
      <td>Punjab</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>2.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Tamil Nadu</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>9.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Uttar Pradesh</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>West Bengal</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.sample(4)
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>6</th>
      <td>Delhi</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>2.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>399</th>
      <td>Sikkim</td>
      <td>2008</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>434</th>
      <td>Jammu &amp; Kashmir</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>177</th>
      <td>West Bengal</td>
      <td>2008</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>25.0</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
</div>



#### **Informations and Description of Data**


```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 448 entries, 0 to 447
    Data columns (total 9 columns):
     #   Column                             Non-Null Count  Dtype  
    ---  ------                             --------------  -----  
     0   Area_Name                          448 non-null    object 
     1   Year                               448 non-null    int64  
     2   Group_Name                         448 non-null    object 
     3   Sub_Group_Name                     448 non-null    object 
     4   Loss_of_Property_1_10_Crores       444 non-null    float64
     5   Loss_of_Property_10_25_Crores      386 non-null    float64
     6   Loss_of_Property_25_50_Crores      382 non-null    float64
     7   Loss_of_Property_50_100_Crores     379 non-null    float64
     8   Loss_of_Property_Above_100_Crores  377 non-null    float64
    dtypes: float64(5), int64(1), object(3)
    memory usage: 31.6+ KB



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
      <th>Year</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>448.000000</td>
      <td>444.000000</td>
      <td>386.000000</td>
      <td>382.000000</td>
      <td>379.000000</td>
      <td>377.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2005.629464</td>
      <td>19.569820</td>
      <td>0.450777</td>
      <td>0.238220</td>
      <td>0.105541</td>
      <td>0.058355</td>
    </tr>
    <tr>
      <th>std</th>
      <td>2.841247</td>
      <td>183.022608</td>
      <td>1.890210</td>
      <td>1.180909</td>
      <td>0.835360</td>
      <td>0.337056</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2001.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2003.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>2006.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2008.000000</td>
      <td>4.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2010.000000</td>
      <td>3131.000000</td>
      <td>23.000000</td>
      <td>15.000000</td>
      <td>15.000000</td>
      <td>5.000000</td>
    </tr>
  </tbody>
</table>
</div>



#### **Extracting a specific column storing it in a variable**


```python
df['Year']
```




    0      2001
    1      2001
    2      2001
    3      2001
    4      2001
           ... 
    443    2010
    444    2010
    445    2010
    446    2010
    447    2010
    Name: Year, Length: 448, dtype: int64




```python
df[["Year", "Loss_of_Property_1_10_Crores", "Loss_of_Property_10_25_Crores"]]
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
      <th>Year</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2001</td>
      <td>4.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2001</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2001</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2001</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2001</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>443</th>
      <td>2010</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>444</th>
      <td>2010</td>
      <td>2.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>445</th>
      <td>2010</td>
      <td>9.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>2010</td>
      <td>3.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>2010</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>448 rows × 3 columns</p>
</div>



#### **Ploting of Data**


```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```


```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="bar")
```




    <Axes: xlabel='Loss_of_Property_10_25_Crores'>




    
![png](output_23_1.png)
    



```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="barh")
```




    <Axes: ylabel='Loss_of_Property_10_25_Crores'>




    
![png](output_24_1.png)
    



```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="pie")
```




    <Axes: ylabel='count'>




    
![png](output_25_1.png)
    



```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="density")
```




    <Axes: ylabel='Density'>




    
![png](output_26_1.png)
    



```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="hist")
```




    <Axes: ylabel='Frequency'>




    
![png](output_27_1.png)
    


#### **Cleaning of Dataset**


```python
df.dropna()
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Andhra Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Arunachal Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Assam</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bihar</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Chandigarh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>441</th>
      <td>Meghalaya</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>442</th>
      <td>Nagaland</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>10.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Odisha</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Tamil Nadu</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>9.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>West Bengal</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>375 rows × 9 columns</p>
</div>




```python
df.drop_duplicates()
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Andhra Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Arunachal Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Assam</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bihar</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Chandigarh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Odisha</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Punjab</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>2.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Tamil Nadu</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>9.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Uttar Pradesh</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>West Bengal</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>448 rows × 9 columns</p>
</div>




```python
df.isnull()
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>443</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>444</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>True</td>
      <td>True</td>
      <td>True</td>
    </tr>
    <tr>
      <th>445</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>446</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>447</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>448 rows × 9 columns</p>
</div>



#### 4. Data Preprocessing

#### **For missing values**


```python
df.isnull().sum()
```




    Area_Name                             0
    Year                                  0
    Group_Name                            0
    Sub_Group_Name                        0
    Loss_of_Property_1_10_Crores          4
    Loss_of_Property_10_25_Crores        62
    Loss_of_Property_25_50_Crores        66
    Loss_of_Property_50_100_Crores       69
    Loss_of_Property_Above_100_Crores    71
    dtype: int64



#### **Remove rows with any missing value**


```python
df.dropna()
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Andhra Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Arunachal Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Assam</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bihar</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Chandigarh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>441</th>
      <td>Meghalaya</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>442</th>
      <td>Nagaland</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>10.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Odisha</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Tamil Nadu</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>9.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>West Bengal</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>375 rows × 9 columns</p>
</div>



#### **Remove columns with missing values**


```python
df.dropna(axis=1)
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Andhra Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Arunachal Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Assam</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bihar</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Chandigarh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Odisha</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Punjab</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Tamil Nadu</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Uttar Pradesh</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
    </tr>
    <tr>
      <th>447</th>
      <td>West Bengal</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
    </tr>
  </tbody>
</table>
<p>448 rows × 4 columns</p>
</div>



#### **Fill missing values**


```python
df.fillna(0)
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Andhra Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>4.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Arunachal Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Assam</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bihar</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Chandigarh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>2. Cheating</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Odisha</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Punjab</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Tamil Nadu</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>9.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Uttar Pradesh</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>West Bengal</td>
      <td>2010</td>
      <td>Serious Fraud - Criminal Breach of Trust</td>
      <td>1. Criminal Breach of Trust</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>448 rows × 9 columns</p>
</div>




```python
df.select_dtypes(include=['object']).columns
```




    Index(['Area_Name', 'Group_Name', 'Sub_Group_Name'], dtype='object')



#### 5. Data Augmentation


```python
def augment_data(df):
    noise = np.random.normal(0, 0.01, df.shape)
    df_noisy = df + noise
    return df_noisy
```


```python
df.aggregate(['sum', 'min'])
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
      <th>Area_Name</th>
      <th>Year</th>
      <th>Group_Name</th>
      <th>Sub_Group_Name</th>
      <th>Loss_of_Property_1_10_Crores</th>
      <th>Loss_of_Property_10_25_Crores</th>
      <th>Loss_of_Property_25_50_Crores</th>
      <th>Loss_of_Property_50_100_Crores</th>
      <th>Loss_of_Property_Above_100_Crores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>sum</th>
      <td>Andhra PradeshArunachal PradeshAssamBiharChand...</td>
      <td>752097</td>
      <td>Serious Fraud - CheatingSerious Fraud - Cheati...</td>
      <td>2. Cheating 2. Cheating 2. Cheating 2. Cheatin...</td>
      <td>5967.0</td>
      <td>137.0</td>
      <td>67.0</td>
      <td>39.0</td>
      <td>21.0</td>
    </tr>
    <tr>
      <th>min</th>
      <td>Andhra Pradesh</td>
      <td>2001</td>
      <td>Serious Fraud - Cheating</td>
      <td>1. Criminal Breach of Trust</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>



#### **Calculating Average**
#### **Finds the average of a numerical column**


```python
df['Loss_of_Property_1_10_Crores'].mean()
```




    15.912



#### **Counts the number of non-null values**


```python
df['Area_Name'].count()
```




    375



#### 6. Save the Processed Data.


```python

df = load_data(file_path)
df = clean_data(df)

```

    Data Loaded Successfully!
    Before Cleaning:
    Area_Name                             0
    Year                                  0
    Group_Name                            0
    Sub_Group_Name                        0
    Loss_of_Property_1_10_Crores          4
    Loss_of_Property_10_25_Crores        62
    Loss_of_Property_25_50_Crores        66
    Loss_of_Property_50_100_Crores       69
    Loss_of_Property_Above_100_Crores    71
    dtype: int64
    After Cleaning:
    Area_Name                            0
    Year                                 0
    Group_Name                           0
    Sub_Group_Name                       0
    Loss_of_Property_1_10_Crores         0
    Loss_of_Property_10_25_Crores        0
    Loss_of_Property_25_50_Crores        0
    Loss_of_Property_50_100_Crores       0
    Loss_of_Property_Above_100_Crores    0
    dtype: int64

