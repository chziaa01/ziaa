# Project: Serious Fraud Analysis

## Description
This README summarizes the steps, code, and outputs from the Jupyter notebook provided.

## # **Project**

## # *Name: Zia Ahmad*
# *Roll No: 073*

## Topic = DataSets

```python
import pandas as pd
```

```python
df =pd.read_csv("Serious Fraud.csv.csv")
```

## Checking Rows and Columns

```python
df.shape
```

## Checking some items from Start and End

```python
df.head(4)
```

```python
df.tail(4)
```

```python
df.sample(4)
```

## Informations and Description of Data

```python
df.info()
```

```python
df.describe()
```

## Extracting a specific column storing it in a variable

```python
df['Year']
```

```python
df[["Year", "Loss_of_Property_1_10_Crores", "Loss_of_Property_10_25_Crores"]]
```

## Ploting of Data

```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="bar")
```

```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="barh")
```

```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="pie")
```

```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="density")
```

```python
df["Loss_of_Property_10_25_Crores"].value_counts().plot(kind="hist")
```

## Cleaning of Dataset

```python
df.dropna()
```

```python
df.drop_duplicates()
```

```python
df.isnull()
```

## Data Preprocessing

```python
df.select_dtypes(include=['object']).columns
```

## Data Augmentation

