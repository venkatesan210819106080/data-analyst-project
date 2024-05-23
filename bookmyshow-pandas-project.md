pandas is an open source library for data manipulation and analysis in python


  . helps to perform EDA(exploratory Data Analysis) on large data.
  
  has inbuilt function for analyzing, cleaning, exploring, and manipulating data

  . has  2 datatpes
  
  . Series
  
     . A Pandas Series is like a Column in a table
     
     . it is a one-dimensional array holding data of any type
     
  . Data Frame
  
     . Data sets in pandas are usually multi-dimensional tables,called Dataframes
     
     . Series is like a cloumn , a DataFrame is the Whole table



 

Creating  a series


```python
import pandas as pd

movie =["leo","rolex","vikram"]
movie=pd.Series(movie)
movie
```




    0       leo
    1     rolex
    2    vikram
    dtype: object




```python
type(movie)
```




    pandas.core.series.Series




```python
movie.size
```




    3




```python
movie[1]
```




    'rolex'



Accessing data in a series


```python
movie[0:2]
```




    0      leo
    1    rolex
    dtype: object



Data Frame

   Loading the Dataset and Library


```python
# csv : "indian-movie-theatres.csv"
theater=pd.read_csv("indian-movie-theatres.csv")
type(theater)
```




    pandas.core.frame.DataFrame




```python
theater
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>theatre_chain</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ahmedabad</td>
      <td>AB Miniplex: Shivranjini Cross Road, Satellite</td>
      <td>125.619048</td>
      <td>302</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Ahmedabad</td>
      <td>Amber Cinema: Ahmedabad</td>
      <td>100.833333</td>
      <td>763</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Ahmedabad</td>
      <td>Anupam Cinema: Ahmedabad</td>
      <td>125.833333</td>
      <td>781</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ahmedabad</td>
      <td>Apsara Cinema, Behrampura</td>
      <td>NaN</td>
      <td>1117</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ahmedabad</td>
      <td>Aradhana Cinema, Behrampura</td>
      <td>NaN</td>
      <td>455</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
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
    </tr>
    <tr>
      <th>573</th>
      <td>Mumbai</td>
      <td>Silver Cinema, Ambewadi</td>
      <td>NaN</td>
      <td>636</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>574</th>
      <td>Mumbai</td>
      <td>Sterling Cineplex: Fort</td>
      <td>167.541667</td>
      <td>900</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>575</th>
      <td>Mumbai</td>
      <td>Sun City: Vile Parle</td>
      <td>180.208333</td>
      <td>615</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>576</th>
      <td>Mumbai</td>
      <td>Super Cinema, Bharat Nagar</td>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>577</th>
      <td>Mumbai</td>
      <td>Super Cinema: Grant Road</td>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>578 rows × 7 columns</p>
</div>



View first 5 records


```python
theater.head()
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>theatre_chain</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ahmedabad</td>
      <td>AB Miniplex: Shivranjini Cross Road, Satellite</td>
      <td>125.619048</td>
      <td>302</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Ahmedabad</td>
      <td>Amber Cinema: Ahmedabad</td>
      <td>100.833333</td>
      <td>763</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Ahmedabad</td>
      <td>Anupam Cinema: Ahmedabad</td>
      <td>125.833333</td>
      <td>781</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ahmedabad</td>
      <td>Apsara Cinema, Behrampura</td>
      <td>NaN</td>
      <td>1117</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ahmedabad</td>
      <td>Aradhana Cinema, Behrampura</td>
      <td>NaN</td>
      <td>455</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



View Last 5 records


```python
theater.tail()
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>theatre_chain</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>573</th>
      <td>Mumbai</td>
      <td>Silver Cinema, Ambewadi</td>
      <td>NaN</td>
      <td>636</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>574</th>
      <td>Mumbai</td>
      <td>Sterling Cineplex: Fort</td>
      <td>167.541667</td>
      <td>900</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>575</th>
      <td>Mumbai</td>
      <td>Sun City: Vile Parle</td>
      <td>180.208333</td>
      <td>615</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>576</th>
      <td>Mumbai</td>
      <td>Super Cinema, Bharat Nagar</td>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>577</th>
      <td>Mumbai</td>
      <td>Super Cinema: Grant Road</td>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



Get total rows and columns


```python
theater.shape
```




    (578, 7)



Get Total elments


```python
theater.size
```




    4046



Get Dataset columns details


```python
theater.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 578 entries, 0 to 577
    Data columns (total 7 columns):
     #   Column                Non-Null Count  Dtype  
    ---  ------                --------------  -----  
     0   city                  578 non-null    object 
     1   theatre_name          578 non-null    object 
     2   average_ticket_price  402 non-null    float64
     3   total_seats           578 non-null    int64  
     4   no_screens            578 non-null    int64  
     5   type                  578 non-null    object 
     6   theatre_chain         185 non-null    object 
    dtypes: float64(1), int64(2), object(4)
    memory usage: 31.7+ KB
    

Retrieve : Select rows 1-10


```python
theater.iloc[1:10]
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>theatre_chain</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Ahmedabad</td>
      <td>Amber Cinema: Ahmedabad</td>
      <td>100.833333</td>
      <td>763</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Ahmedabad</td>
      <td>Anupam Cinema: Ahmedabad</td>
      <td>125.833333</td>
      <td>781</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ahmedabad</td>
      <td>Apsara Cinema, Behrampura</td>
      <td>NaN</td>
      <td>1117</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ahmedabad</td>
      <td>Aradhana Cinema, Behrampura</td>
      <td>NaN</td>
      <td>455</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Ahmedabad</td>
      <td>Carnival: Himalaya Mall</td>
      <td>189.050926</td>
      <td>1110</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>Carnival</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Ahmedabad</td>
      <td>Cinemax: Dev Arc, Ahmedabad</td>
      <td>176.435185</td>
      <td>1047</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>PVR</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Ahmedabad</td>
      <td>Cinemax: Red Carpet, Ahmedabad</td>
      <td>152.052469</td>
      <td>991</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>PVR</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Ahmedabad</td>
      <td>Cinemax: Shiv, Ahmedabad</td>
      <td>176.277778</td>
      <td>637</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>PVR</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Ahmedabad</td>
      <td>Cinepolis: Alpha One Mall, Ahmedabad</td>
      <td>197.949495</td>
      <td>1136</td>
      <td>6</td>
      <td>Multiplex</td>
      <td>Cinepolis</td>
    </tr>
  </tbody>
</table>
</div>



Retrieve : Select Columns in Specific position


```python
theater.iloc[:,[2,3,4]]
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
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>125.619048</td>
      <td>302</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>100.833333</td>
      <td>763</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>125.833333</td>
      <td>781</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>1117</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NaN</td>
      <td>455</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>573</th>
      <td>NaN</td>
      <td>636</td>
      <td>1</td>
    </tr>
    <tr>
      <th>574</th>
      <td>167.541667</td>
      <td>900</td>
      <td>3</td>
    </tr>
    <tr>
      <th>575</th>
      <td>180.208333</td>
      <td>615</td>
      <td>2</td>
    </tr>
    <tr>
      <th>576</th>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
    </tr>
    <tr>
      <th>577</th>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>578 rows × 3 columns</p>
</div>



Retrieve : Select Columns With Specific tables


```python
theater[["city","no_screens"]]
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
      <th>city</th>
      <th>no_screens</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ahmedabad</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Ahmedabad</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Ahmedabad</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ahmedabad</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ahmedabad</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>573</th>
      <td>Mumbai</td>
      <td>1</td>
    </tr>
    <tr>
      <th>574</th>
      <td>Mumbai</td>
      <td>3</td>
    </tr>
    <tr>
      <th>575</th>
      <td>Mumbai</td>
      <td>2</td>
    </tr>
    <tr>
      <th>576</th>
      <td>Mumbai</td>
      <td>1</td>
    </tr>
    <tr>
      <th>577</th>
      <td>Mumbai</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>578 rows × 2 columns</p>
</div>



Retrieve : Select Columns between theatre_name : type


```python
theater.loc[:,"theatre_name": "type"]
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
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AB Miniplex: Shivranjini Cross Road, Satellite</td>
      <td>125.619048</td>
      <td>302</td>
      <td>3</td>
      <td>Multiplex</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Amber Cinema: Ahmedabad</td>
      <td>100.833333</td>
      <td>763</td>
      <td>1</td>
      <td>Single Screen</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Anupam Cinema: Ahmedabad</td>
      <td>125.833333</td>
      <td>781</td>
      <td>1</td>
      <td>Single Screen</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Apsara Cinema, Behrampura</td>
      <td>NaN</td>
      <td>1117</td>
      <td>1</td>
      <td>Single Screen</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Aradhana Cinema, Behrampura</td>
      <td>NaN</td>
      <td>455</td>
      <td>1</td>
      <td>Single Screen</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>573</th>
      <td>Silver Cinema, Ambewadi</td>
      <td>NaN</td>
      <td>636</td>
      <td>1</td>
      <td>Single Screen</td>
    </tr>
    <tr>
      <th>574</th>
      <td>Sterling Cineplex: Fort</td>
      <td>167.541667</td>
      <td>900</td>
      <td>3</td>
      <td>Multiplex</td>
    </tr>
    <tr>
      <th>575</th>
      <td>Sun City: Vile Parle</td>
      <td>180.208333</td>
      <td>615</td>
      <td>2</td>
      <td>Multiplex</td>
    </tr>
    <tr>
      <th>576</th>
      <td>Super Cinema, Bharat Nagar</td>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
    </tr>
    <tr>
      <th>577</th>
      <td>Super Cinema: Grant Road</td>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
    </tr>
  </tbody>
</table>
<p>578 rows × 5 columns</p>
</div>



Retrieve : Select Columns between theatre_name : type for rows between 2 - 4


```python
theater.loc[5:9,"theatre_name": "type"]
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
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5</th>
      <td>Carnival: Himalaya Mall</td>
      <td>189.050926</td>
      <td>1110</td>
      <td>5</td>
      <td>Multiplex</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Cinemax: Dev Arc, Ahmedabad</td>
      <td>176.435185</td>
      <td>1047</td>
      <td>4</td>
      <td>Multiplex</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Cinemax: Red Carpet, Ahmedabad</td>
      <td>152.052469</td>
      <td>991</td>
      <td>4</td>
      <td>Multiplex</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Cinemax: Shiv, Ahmedabad</td>
      <td>176.277778</td>
      <td>637</td>
      <td>3</td>
      <td>Multiplex</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Cinepolis: Alpha One Mall, Ahmedabad</td>
      <td>197.949495</td>
      <td>1136</td>
      <td>6</td>
      <td>Multiplex</td>
    </tr>
  </tbody>
</table>
</div>



Retrieve : single value by index


```python
theater.iat[1,1]
```




    'Amber Cinema: Ahmedabad'



Retrieve : single value by label


```python
theater.at[4,"total_seats"]
```




    455



get all column names


```python
theater.columns
```




    Index(['city', 'theatre_name', 'average_ticket_price', 'total_seats',
           'no_screens', 'type', 'theatre_chain'],
          dtype='object')



Rename a columns


```python
theater.rename(columns={"theatre_chain":"talkies_name"},inplace=True)
```


```python
theater.columns
```




    Index(['city', 'theatre_name', 'average_ticket_price', 'total_seats',
           'no_screens', 'type', 'talkies_name'],
          dtype='object')




```python
theater.iloc[1:10]
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>talkies_name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Ahmedabad</td>
      <td>Amber Cinema: Ahmedabad</td>
      <td>100.833333</td>
      <td>763</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Ahmedabad</td>
      <td>Anupam Cinema: Ahmedabad</td>
      <td>125.833333</td>
      <td>781</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ahmedabad</td>
      <td>Apsara Cinema, Behrampura</td>
      <td>NaN</td>
      <td>1117</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ahmedabad</td>
      <td>Aradhana Cinema, Behrampura</td>
      <td>NaN</td>
      <td>455</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Ahmedabad</td>
      <td>Carnival: Himalaya Mall</td>
      <td>189.050926</td>
      <td>1110</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>Carnival</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Ahmedabad</td>
      <td>Cinemax: Dev Arc, Ahmedabad</td>
      <td>176.435185</td>
      <td>1047</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>PVR</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Ahmedabad</td>
      <td>Cinemax: Red Carpet, Ahmedabad</td>
      <td>152.052469</td>
      <td>991</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>PVR</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Ahmedabad</td>
      <td>Cinemax: Shiv, Ahmedabad</td>
      <td>176.277778</td>
      <td>637</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>PVR</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Ahmedabad</td>
      <td>Cinepolis: Alpha One Mall, Ahmedabad</td>
      <td>197.949495</td>
      <td>1136</td>
      <td>6</td>
      <td>Multiplex</td>
      <td>Cinepolis</td>
    </tr>
  </tbody>
</table>
</div>



Add a Columns


```python
country_series=pd.Series(["India"]*len(theater))
country_series
```




    0      India
    1      India
    2      India
    3      India
    4      India
           ...  
    573    India
    574    India
    575    India
    576    India
    577    India
    Length: 578, dtype: object




```python
theater=pd.concat([theater,country_series],axis=1)
```


```python
theater.columns
```




    Index([                'city',         'theatre_name', 'average_ticket_price',
                    'total_seats',           'no_screens',                 'type',
                   'talkies_name',                      0],
          dtype='object')




```python
theater.rename(columns={0:"Country"},inplace=True)
```


```python
theater
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>talkies_name</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ahmedabad</td>
      <td>AB Miniplex: Shivranjini Cross Road, Satellite</td>
      <td>125.619048</td>
      <td>302</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Ahmedabad</td>
      <td>Amber Cinema: Ahmedabad</td>
      <td>100.833333</td>
      <td>763</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Ahmedabad</td>
      <td>Anupam Cinema: Ahmedabad</td>
      <td>125.833333</td>
      <td>781</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ahmedabad</td>
      <td>Apsara Cinema, Behrampura</td>
      <td>NaN</td>
      <td>1117</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ahmedabad</td>
      <td>Aradhana Cinema, Behrampura</td>
      <td>NaN</td>
      <td>455</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
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
    </tr>
    <tr>
      <th>573</th>
      <td>Mumbai</td>
      <td>Silver Cinema, Ambewadi</td>
      <td>NaN</td>
      <td>636</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>574</th>
      <td>Mumbai</td>
      <td>Sterling Cineplex: Fort</td>
      <td>167.541667</td>
      <td>900</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>575</th>
      <td>Mumbai</td>
      <td>Sun City: Vile Parle</td>
      <td>180.208333</td>
      <td>615</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>576</th>
      <td>Mumbai</td>
      <td>Super Cinema, Bharat Nagar</td>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>577</th>
      <td>Mumbai</td>
      <td>Super Cinema: Grant Road</td>
      <td>NaN</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
<p>578 rows × 8 columns</p>
</div>



Filtering : Using Logical operators =,<,>

Filtering theaters in chennai alone


```python
theater[theater["city"]=="Chennai"]
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>talkies_name</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>179</th>
      <td>Chennai</td>
      <td>Abirami Cinemas: Chennai</td>
      <td>113.583333</td>
      <td>1656</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>180</th>
      <td>Chennai</td>
      <td>Agasthiya, T.H Road</td>
      <td>NaN</td>
      <td>1004</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>181</th>
      <td>Chennai</td>
      <td>AGS Cinemas: T. Nagar</td>
      <td>82.700000</td>
      <td>884</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>AGS Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>182</th>
      <td>Chennai</td>
      <td>AGS Cinemas: Villivakkam</td>
      <td>82.700000</td>
      <td>1473</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>AGS Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>183</th>
      <td>Chennai</td>
      <td>Albert Complex</td>
      <td>NaN</td>
      <td>1200</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>184</th>
      <td>Chennai</td>
      <td>Anna Theatre: Chennai</td>
      <td>94.600000</td>
      <td>364</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>185</th>
      <td>Chennai</td>
      <td>Annai Karumari, Virugambakkam</td>
      <td>NaN</td>
      <td>196</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>186</th>
      <td>Chennai</td>
      <td>Arvind Theatre A/C dts</td>
      <td>NaN</td>
      <td>445</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>187</th>
      <td>Chennai</td>
      <td>AVM Rajeswari A/C dts</td>
      <td>NaN</td>
      <td>603</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>188</th>
      <td>Chennai</td>
      <td>Baby Albert Theatre, Whannels Road</td>
      <td>NaN</td>
      <td>242</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>189</th>
      <td>Chennai</td>
      <td>Bala Theatre, Anna Road</td>
      <td>NaN</td>
      <td>518</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>190</th>
      <td>Chennai</td>
      <td>Bharath Theatre Dolby AtmosDolby Atmos</td>
      <td>NaN</td>
      <td>963</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>191</th>
      <td>Chennai</td>
      <td>Casino Theatre: Chennai</td>
      <td>59.000000</td>
      <td>83</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Chennai</td>
      <td>Chandran Theatre, Ashoknagar</td>
      <td>NaN</td>
      <td>515</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>193</th>
      <td>Chennai</td>
      <td>Devi Karumari A/C</td>
      <td>NaN</td>
      <td>850</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>194</th>
      <td>Chennai</td>
      <td>Devicineplex</td>
      <td>NaN</td>
      <td>2462</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>195</th>
      <td>Chennai</td>
      <td>Ega Cinema</td>
      <td>NaN</td>
      <td>1168</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>196</th>
      <td>Chennai</td>
      <td>Ganapathy Ram Theatre: Chennai</td>
      <td>90.000000</td>
      <td>852</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>197</th>
      <td>Chennai</td>
      <td>GK Cinemas 2K Dolby Atmos: Porur</td>
      <td>116.190000</td>
      <td>557</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>198</th>
      <td>Chennai</td>
      <td>INOX National: Arcot Road</td>
      <td>153.600000</td>
      <td>1182</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>Inox</td>
      <td>India</td>
    </tr>
    <tr>
      <th>199</th>
      <td>Chennai</td>
      <td>INOX: Chennai Citi Centre, Dr. RK Salai</td>
      <td>153.600000</td>
      <td>528</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>Inox</td>
      <td>India</td>
    </tr>
    <tr>
      <th>200</th>
      <td>Chennai</td>
      <td>Jothi Theatre 4K A/c DTS: ST Thomas Mount</td>
      <td>0.000000</td>
      <td>805</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>201</th>
      <td>Chennai</td>
      <td>Kamala CinemasF&amp;B;</td>
      <td>NaN</td>
      <td>586</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>202</th>
      <td>Chennai</td>
      <td>Kasi4K Dolby Atmos</td>
      <td>NaN</td>
      <td>733</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>203</th>
      <td>Chennai</td>
      <td>Krishnaveni, South Usman Raod</td>
      <td>NaN</td>
      <td>898</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>204</th>
      <td>Chennai</td>
      <td>Kumaran Theatre QUBE A/C DTS: Madipakkam</td>
      <td>0.000000</td>
      <td>1008</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>205</th>
      <td>Chennai</td>
      <td>Luxe Cinemas: Chennai</td>
      <td>153.600000</td>
      <td>1844</td>
      <td>9</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>206</th>
      <td>Chennai</td>
      <td>Mahalakshmi Talkies, Strahans Road</td>
      <td>NaN</td>
      <td>1040</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>207</th>
      <td>Chennai</td>
      <td>Maharani Theatre 2K dts</td>
      <td>NaN</td>
      <td>910</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>208</th>
      <td>Chennai</td>
      <td>Mayura, Arakonam Road</td>
      <td>NaN</td>
      <td>474</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>209</th>
      <td>Chennai</td>
      <td>MM Theatre</td>
      <td>NaN</td>
      <td>772</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>210</th>
      <td>Chennai</td>
      <td>Murugan Cinemas - AmbatturDolby Atmos</td>
      <td>NaN</td>
      <td>960</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>211</th>
      <td>Chennai</td>
      <td>Nadhamuni Cinema</td>
      <td>NaN</td>
      <td>650</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>212</th>
      <td>Chennai</td>
      <td>Padmam, Poonamallee High Road</td>
      <td>NaN</td>
      <td>420</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>213</th>
      <td>Chennai</td>
      <td>Pandian, Moolakadai</td>
      <td>NaN</td>
      <td>1002</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>214</th>
      <td>Chennai</td>
      <td>PVR: Ampa, Chennai</td>
      <td>82.700000</td>
      <td>1794</td>
      <td>7</td>
      <td>Multiplex</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>215</th>
      <td>Chennai</td>
      <td>PVR: Velachery, Chennai</td>
      <td>82.700000</td>
      <td>1275</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>216</th>
      <td>Chennai</td>
      <td>Raj Theatre - A/C DTS: Chennai</td>
      <td>175.000000</td>
      <td>950</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>217</th>
      <td>Chennai</td>
      <td>Rakki Cinemas - Ambattur</td>
      <td>NaN</td>
      <td>361</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>218</th>
      <td>Chennai</td>
      <td>Rohini Silver Screens: Chennai</td>
      <td>104.030000</td>
      <td>3175</td>
      <td>7</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>219</th>
      <td>Chennai</td>
      <td>Roopam, Poonamallee High Road</td>
      <td>NaN</td>
      <td>288</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>220</th>
      <td>Chennai</td>
      <td>Sangam Cinemas</td>
      <td>NaN</td>
      <td>1662</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>221</th>
      <td>Chennai</td>
      <td>Saravana Theatre, Brick Kiln Road</td>
      <td>NaN</td>
      <td>600</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>222</th>
      <td>Chennai</td>
      <td>Sathyam Royapettah, Lloyds Estate</td>
      <td>NaN</td>
      <td>2283</td>
      <td>6</td>
      <td>Multiplex</td>
      <td>SPI Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>223</th>
      <td>Chennai</td>
      <td>SK-Marlen Cinemas 2K, Guindy: Alandur</td>
      <td>150.000000</td>
      <td>229</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>224</th>
      <td>Chennai</td>
      <td>Spectrum Mall, Perambur North</td>
      <td>NaN</td>
      <td>1395</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>225</th>
      <td>Chennai</td>
      <td>Sri Bhuvaneshwari Theatre A/C dts</td>
      <td>NaN</td>
      <td>565</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>226</th>
      <td>Chennai</td>
      <td>Sri Ganga Cinemas Dolby Atmos - KolathurDolby ...</td>
      <td>NaN</td>
      <td>772</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>227</th>
      <td>Chennai</td>
      <td>Sri Murugan, Ambattur</td>
      <td>NaN</td>
      <td>960</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>228</th>
      <td>Chennai</td>
      <td>Srinivasa Theatre</td>
      <td>NaN</td>
      <td>900</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>229</th>
      <td>Chennai</td>
      <td>The Forum Vijaya Mall, Vadapalani</td>
      <td>NaN</td>
      <td>3010</td>
      <td>9</td>
      <td>Multiplex</td>
      <td>SPI Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>230</th>
      <td>Chennai</td>
      <td>Thirumurugan, Ambattur</td>
      <td>NaN</td>
      <td>510</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>231</th>
      <td>Chennai</td>
      <td>Udhayam Complex</td>
      <td>NaN</td>
      <td>759</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>232</th>
      <td>Chennai</td>
      <td>Udhayam Theatre, Ashoknagar</td>
      <td>NaN</td>
      <td>759</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>233</th>
      <td>Chennai</td>
      <td>Vetrrivel Theatre 2K - Nanganallur</td>
      <td>NaN</td>
      <td>600</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>234</th>
      <td>Chennai</td>
      <td>Woodlands Complex: Chennai</td>
      <td>69.500000</td>
      <td>1713</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
</div>



Filtering theaters with seats less than 100


```python
theater[theater["total_seats"]<100]
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>talkies_name</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>36</th>
      <td>Bangalore</td>
      <td>7D Mastii: Element Mall, Nagwara</td>
      <td>150.000000</td>
      <td>18</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Mastiii 7D</td>
      <td>India</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Bangalore</td>
      <td>7D Mastiii: Forum Value Mall, Whitefield</td>
      <td>150.000000</td>
      <td>16</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Mastiii 7D</td>
      <td>India</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Bangalore</td>
      <td>7D Voyage: Central Mall, Bellandur</td>
      <td>180.000000</td>
      <td>8</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>7D Voyage</td>
      <td>India</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Bangalore</td>
      <td>7D VR Voyage: Garuda Mall</td>
      <td>190.000000</td>
      <td>8</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>7D Voyage</td>
      <td>India</td>
    </tr>
    <tr>
      <th>87</th>
      <td>Bangalore</td>
      <td>Maheshwari Digital 4K Cinema: Bannerghatta Road</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>109</th>
      <td>Bangalore</td>
      <td>PVR: Forum Gold, Bengaluru</td>
      <td>825.000000</td>
      <td>32</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>120</th>
      <td>Bangalore</td>
      <td>PVR: VR Gold, Bengaluru</td>
      <td>697.025000</td>
      <td>1</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>191</th>
      <td>Chennai</td>
      <td>Casino Theatre: Chennai</td>
      <td>59.000000</td>
      <td>83</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>235</th>
      <td>Delhi</td>
      <td>7D Mastiii: TDI Mall, Rajouri Garden, Delhi</td>
      <td>170.000000</td>
      <td>18</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>273</th>
      <td>Delhi</td>
      <td>PVR: Select City Walk (Gold), Delhi</td>
      <td>943.750000</td>
      <td>40</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>287</th>
      <td>Hyderabad</td>
      <td>Amba Theatre: Mehdipatnam</td>
      <td>100.000000</td>
      <td>64</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>321</th>
      <td>Hyderabad</td>
      <td>Kalyani Movie Max: Bowenpally</td>
      <td>70.000000</td>
      <td>84</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>323</th>
      <td>Hyderabad</td>
      <td>Kumar Theatre: Kachiguda</td>
      <td>90.000000</td>
      <td>74</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>386</th>
      <td>Hyderabad</td>
      <td>SSV Cine Park: Patancheru</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>419</th>
      <td>Kochi</td>
      <td>Padma Cinema Screen 2: Ernakulam</td>
      <td>110.000000</td>
      <td>98</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>424</th>
      <td>Kolkata</td>
      <td>11D Adventureplex: Quest Mall</td>
      <td>250.000000</td>
      <td>30</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>425</th>
      <td>Kolkata</td>
      <td>7D Adventure Plex: Mani Square Mall</td>
      <td>200.000000</td>
      <td>32</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>549</th>
      <td>Mumbai</td>
      <td>PVR ICON: Versova (Gold)</td>
      <td>616.666667</td>
      <td>86</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
</div>



Filtering theaters with average_ticket_price>1000


```python
theater[theater["average_ticket_price"]>1000]
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>talkies_name</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>265</th>
      <td>Delhi</td>
      <td>PVR: Director's Cut, Ambience Delhi</td>
      <td>1458.333333</td>
      <td>282</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
</div>



Grouping


```python
theater.groupby(['type']).sum()
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>talkies_name</th>
      <th>Country</th>
    </tr>
    <tr>
      <th>type</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Multiplex</th>
      <td>AhmedabadAhmedabadAhmedabadAhmedabadAhmedabadA...</td>
      <td>AB Miniplex: Shivranjini Cross Road, Satellite...</td>
      <td>37736.652568</td>
      <td>192764</td>
      <td>801</td>
      <td>CarnivalPVRPVRPVRCinepolisCity GoldCity GoldCi...</td>
      <td>IndiaIndiaIndiaIndiaIndiaIndiaIndiaIndiaIndiaI...</td>
    </tr>
    <tr>
      <th>Single Screen</th>
      <td>AhmedabadAhmedabadAhmedabadAhmedabadAhmedabadA...</td>
      <td>Amber Cinema: AhmedabadAnupam Cinema: Ahmedaba...</td>
      <td>30113.707407</td>
      <td>278433</td>
      <td>391</td>
      <td>Mastiii 7DMastiii 7D7D Voyage7D VoyagePVRPVRPV...</td>
      <td>IndiaIndiaIndiaIndiaIndiaIndiaIndiaIndiaIndiaI...</td>
    </tr>
  </tbody>
</table>
</div>



Grouping and Sorting


```python
theater.groupby(['type']).sum().sort_values(by="total_seats",ascending=False)
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>talkies_name</th>
      <th>Country</th>
    </tr>
    <tr>
      <th>type</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Single Screen</th>
      <td>AhmedabadAhmedabadAhmedabadAhmedabadAhmedabadA...</td>
      <td>Amber Cinema: AhmedabadAnupam Cinema: Ahmedaba...</td>
      <td>30113.707407</td>
      <td>278433</td>
      <td>391</td>
      <td>Mastiii 7DMastiii 7D7D Voyage7D VoyagePVRPVRPV...</td>
      <td>IndiaIndiaIndiaIndiaIndiaIndiaIndiaIndiaIndiaI...</td>
    </tr>
    <tr>
      <th>Multiplex</th>
      <td>AhmedabadAhmedabadAhmedabadAhmedabadAhmedabadA...</td>
      <td>AB Miniplex: Shivranjini Cross Road, Satellite...</td>
      <td>37736.652568</td>
      <td>192764</td>
      <td>801</td>
      <td>CarnivalPVRPVRPVRCinepolisCity GoldCity GoldCi...</td>
      <td>IndiaIndiaIndiaIndiaIndiaIndiaIndiaIndiaIndiaI...</td>
    </tr>
  </tbody>
</table>
</div>



Create a new dataframe From exising dataframe


```python
chennai= theater[theater["city"]=="Chennai"]
type(chennai)         
```




    pandas.core.frame.DataFrame



Check for missing values


```python
chennai
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>talkies_name</th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>179</th>
      <td>Chennai</td>
      <td>Abirami Cinemas: Chennai</td>
      <td>113.583333</td>
      <td>1656</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>180</th>
      <td>Chennai</td>
      <td>Agasthiya, T.H Road</td>
      <td>NaN</td>
      <td>1004</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>181</th>
      <td>Chennai</td>
      <td>AGS Cinemas: T. Nagar</td>
      <td>82.700000</td>
      <td>884</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>AGS Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>182</th>
      <td>Chennai</td>
      <td>AGS Cinemas: Villivakkam</td>
      <td>82.700000</td>
      <td>1473</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>AGS Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>183</th>
      <td>Chennai</td>
      <td>Albert Complex</td>
      <td>NaN</td>
      <td>1200</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>184</th>
      <td>Chennai</td>
      <td>Anna Theatre: Chennai</td>
      <td>94.600000</td>
      <td>364</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>185</th>
      <td>Chennai</td>
      <td>Annai Karumari, Virugambakkam</td>
      <td>NaN</td>
      <td>196</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>186</th>
      <td>Chennai</td>
      <td>Arvind Theatre A/C dts</td>
      <td>NaN</td>
      <td>445</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>187</th>
      <td>Chennai</td>
      <td>AVM Rajeswari A/C dts</td>
      <td>NaN</td>
      <td>603</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>188</th>
      <td>Chennai</td>
      <td>Baby Albert Theatre, Whannels Road</td>
      <td>NaN</td>
      <td>242</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>189</th>
      <td>Chennai</td>
      <td>Bala Theatre, Anna Road</td>
      <td>NaN</td>
      <td>518</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>190</th>
      <td>Chennai</td>
      <td>Bharath Theatre Dolby AtmosDolby Atmos</td>
      <td>NaN</td>
      <td>963</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>191</th>
      <td>Chennai</td>
      <td>Casino Theatre: Chennai</td>
      <td>59.000000</td>
      <td>83</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Chennai</td>
      <td>Chandran Theatre, Ashoknagar</td>
      <td>NaN</td>
      <td>515</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>193</th>
      <td>Chennai</td>
      <td>Devi Karumari A/C</td>
      <td>NaN</td>
      <td>850</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>194</th>
      <td>Chennai</td>
      <td>Devicineplex</td>
      <td>NaN</td>
      <td>2462</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>195</th>
      <td>Chennai</td>
      <td>Ega Cinema</td>
      <td>NaN</td>
      <td>1168</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>196</th>
      <td>Chennai</td>
      <td>Ganapathy Ram Theatre: Chennai</td>
      <td>90.000000</td>
      <td>852</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>197</th>
      <td>Chennai</td>
      <td>GK Cinemas 2K Dolby Atmos: Porur</td>
      <td>116.190000</td>
      <td>557</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>198</th>
      <td>Chennai</td>
      <td>INOX National: Arcot Road</td>
      <td>153.600000</td>
      <td>1182</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>Inox</td>
      <td>India</td>
    </tr>
    <tr>
      <th>199</th>
      <td>Chennai</td>
      <td>INOX: Chennai Citi Centre, Dr. RK Salai</td>
      <td>153.600000</td>
      <td>528</td>
      <td>4</td>
      <td>Multiplex</td>
      <td>Inox</td>
      <td>India</td>
    </tr>
    <tr>
      <th>200</th>
      <td>Chennai</td>
      <td>Jothi Theatre 4K A/c DTS: ST Thomas Mount</td>
      <td>0.000000</td>
      <td>805</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>201</th>
      <td>Chennai</td>
      <td>Kamala CinemasF&amp;B;</td>
      <td>NaN</td>
      <td>586</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>202</th>
      <td>Chennai</td>
      <td>Kasi4K Dolby Atmos</td>
      <td>NaN</td>
      <td>733</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>203</th>
      <td>Chennai</td>
      <td>Krishnaveni, South Usman Raod</td>
      <td>NaN</td>
      <td>898</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>204</th>
      <td>Chennai</td>
      <td>Kumaran Theatre QUBE A/C DTS: Madipakkam</td>
      <td>0.000000</td>
      <td>1008</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>205</th>
      <td>Chennai</td>
      <td>Luxe Cinemas: Chennai</td>
      <td>153.600000</td>
      <td>1844</td>
      <td>9</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>206</th>
      <td>Chennai</td>
      <td>Mahalakshmi Talkies, Strahans Road</td>
      <td>NaN</td>
      <td>1040</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>207</th>
      <td>Chennai</td>
      <td>Maharani Theatre 2K dts</td>
      <td>NaN</td>
      <td>910</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>208</th>
      <td>Chennai</td>
      <td>Mayura, Arakonam Road</td>
      <td>NaN</td>
      <td>474</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>209</th>
      <td>Chennai</td>
      <td>MM Theatre</td>
      <td>NaN</td>
      <td>772</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>210</th>
      <td>Chennai</td>
      <td>Murugan Cinemas - AmbatturDolby Atmos</td>
      <td>NaN</td>
      <td>960</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>211</th>
      <td>Chennai</td>
      <td>Nadhamuni Cinema</td>
      <td>NaN</td>
      <td>650</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>212</th>
      <td>Chennai</td>
      <td>Padmam, Poonamallee High Road</td>
      <td>NaN</td>
      <td>420</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>213</th>
      <td>Chennai</td>
      <td>Pandian, Moolakadai</td>
      <td>NaN</td>
      <td>1002</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>214</th>
      <td>Chennai</td>
      <td>PVR: Ampa, Chennai</td>
      <td>82.700000</td>
      <td>1794</td>
      <td>7</td>
      <td>Multiplex</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>215</th>
      <td>Chennai</td>
      <td>PVR: Velachery, Chennai</td>
      <td>82.700000</td>
      <td>1275</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>216</th>
      <td>Chennai</td>
      <td>Raj Theatre - A/C DTS: Chennai</td>
      <td>175.000000</td>
      <td>950</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>217</th>
      <td>Chennai</td>
      <td>Rakki Cinemas - Ambattur</td>
      <td>NaN</td>
      <td>361</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>218</th>
      <td>Chennai</td>
      <td>Rohini Silver Screens: Chennai</td>
      <td>104.030000</td>
      <td>3175</td>
      <td>7</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>219</th>
      <td>Chennai</td>
      <td>Roopam, Poonamallee High Road</td>
      <td>NaN</td>
      <td>288</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>220</th>
      <td>Chennai</td>
      <td>Sangam Cinemas</td>
      <td>NaN</td>
      <td>1662</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>221</th>
      <td>Chennai</td>
      <td>Saravana Theatre, Brick Kiln Road</td>
      <td>NaN</td>
      <td>600</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>222</th>
      <td>Chennai</td>
      <td>Sathyam Royapettah, Lloyds Estate</td>
      <td>NaN</td>
      <td>2283</td>
      <td>6</td>
      <td>Multiplex</td>
      <td>SPI Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>223</th>
      <td>Chennai</td>
      <td>SK-Marlen Cinemas 2K, Guindy: Alandur</td>
      <td>150.000000</td>
      <td>229</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>224</th>
      <td>Chennai</td>
      <td>Spectrum Mall, Perambur North</td>
      <td>NaN</td>
      <td>1395</td>
      <td>5</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>225</th>
      <td>Chennai</td>
      <td>Sri Bhuvaneshwari Theatre A/C dts</td>
      <td>NaN</td>
      <td>565</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>226</th>
      <td>Chennai</td>
      <td>Sri Ganga Cinemas Dolby Atmos - KolathurDolby ...</td>
      <td>NaN</td>
      <td>772</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>227</th>
      <td>Chennai</td>
      <td>Sri Murugan, Ambattur</td>
      <td>NaN</td>
      <td>960</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>228</th>
      <td>Chennai</td>
      <td>Srinivasa Theatre</td>
      <td>NaN</td>
      <td>900</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>229</th>
      <td>Chennai</td>
      <td>The Forum Vijaya Mall, Vadapalani</td>
      <td>NaN</td>
      <td>3010</td>
      <td>9</td>
      <td>Multiplex</td>
      <td>SPI Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>230</th>
      <td>Chennai</td>
      <td>Thirumurugan, Ambattur</td>
      <td>NaN</td>
      <td>510</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>231</th>
      <td>Chennai</td>
      <td>Udhayam Complex</td>
      <td>NaN</td>
      <td>759</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>232</th>
      <td>Chennai</td>
      <td>Udhayam Theatre, Ashoknagar</td>
      <td>NaN</td>
      <td>759</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>233</th>
      <td>Chennai</td>
      <td>Vetrrivel Theatre 2K - Nanganallur</td>
      <td>NaN</td>
      <td>600</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
    <tr>
      <th>234</th>
      <td>Chennai</td>
      <td>Woodlands Complex: Chennai</td>
      <td>69.500000</td>
      <td>1713</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>NaN</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
</div>



Check for missing values


```python
chennai.isnull().sum()
```




    city                     0
    theatre_name             0
    average_ticket_price    38
    total_seats              0
    no_screens               0
    type                     0
    talkies_name            48
    0                        0
    dtype: int64



Get columns names that have nan values


```python
nan_columns=chennai.isna().any()
nan_columns
```




    city                    False
    theatre_name            False
    average_ticket_price     True
    total_seats             False
    no_screens              False
    type                    False
    talkies_name             True
    0                       False
    dtype: bool



Drop a column


```python
theater.drop(["average_ticket_price","talkies_name"],axis=1,inplace=True)
```


```python
theater.columns
```




    Index(['city', 'theatre_name', 'total_seats', 'no_screens', 'type', 0], dtype='object')




```python
theater
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
      <th>city</th>
      <th>theatre_name</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Ahmedabad</td>
      <td>AB Miniplex: Shivranjini Cross Road, Satellite</td>
      <td>302</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>India</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Ahmedabad</td>
      <td>Amber Cinema: Ahmedabad</td>
      <td>763</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>India</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Ahmedabad</td>
      <td>Anupam Cinema: Ahmedabad</td>
      <td>781</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>India</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ahmedabad</td>
      <td>Apsara Cinema, Behrampura</td>
      <td>1117</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>India</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ahmedabad</td>
      <td>Aradhana Cinema, Behrampura</td>
      <td>455</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>India</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>573</th>
      <td>Mumbai</td>
      <td>Silver Cinema, Ambewadi</td>
      <td>636</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>India</td>
    </tr>
    <tr>
      <th>574</th>
      <td>Mumbai</td>
      <td>Sterling Cineplex: Fort</td>
      <td>900</td>
      <td>3</td>
      <td>Multiplex</td>
      <td>India</td>
    </tr>
    <tr>
      <th>575</th>
      <td>Mumbai</td>
      <td>Sun City: Vile Parle</td>
      <td>615</td>
      <td>2</td>
      <td>Multiplex</td>
      <td>India</td>
    </tr>
    <tr>
      <th>576</th>
      <td>Mumbai</td>
      <td>Super Cinema, Bharat Nagar</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>India</td>
    </tr>
    <tr>
      <th>577</th>
      <td>Mumbai</td>
      <td>Super Cinema: Grant Road</td>
      <td>822</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
<p>578 rows × 6 columns</p>
</div>



Use fillna to replace NaN values operation


```python
chennai["talkies_name"].fillna("Other",inplace=True)
```

    C:\Users\ASUS\AppData\Local\Temp\ipykernel_12440\3216618665.py:1: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame
    
    See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
      chennai["talkies_name"].fillna("Other",inplace=True)
    


```python
chennai["type"]=chennai["type"].apply(lambda x: "Multiscreen" if x == "Multiplex" else x)
```

    C:\Users\ASUS\AppData\Local\Temp\ipykernel_12440\2986600826.py:1: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame.
    Try using .loc[row_indexer,col_indexer] = value instead
    
    See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
      chennai["type"]=chennai["type"].apply(lambda x: "Multiscreen" if x == "Multiplex" else x)
    

Use Apply Function


```python
chennai
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
      <th>city</th>
      <th>theatre_name</th>
      <th>average_ticket_price</th>
      <th>total_seats</th>
      <th>no_screens</th>
      <th>type</th>
      <th>talkies_name</th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>179</th>
      <td>Chennai</td>
      <td>Abirami Cinemas: Chennai</td>
      <td>113.583333</td>
      <td>1656</td>
      <td>4</td>
      <td>Multiscreen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>180</th>
      <td>Chennai</td>
      <td>Agasthiya, T.H Road</td>
      <td>NaN</td>
      <td>1004</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>181</th>
      <td>Chennai</td>
      <td>AGS Cinemas: T. Nagar</td>
      <td>82.700000</td>
      <td>884</td>
      <td>4</td>
      <td>Multiscreen</td>
      <td>AGS Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>182</th>
      <td>Chennai</td>
      <td>AGS Cinemas: Villivakkam</td>
      <td>82.700000</td>
      <td>1473</td>
      <td>5</td>
      <td>Multiscreen</td>
      <td>AGS Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>183</th>
      <td>Chennai</td>
      <td>Albert Complex</td>
      <td>NaN</td>
      <td>1200</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>184</th>
      <td>Chennai</td>
      <td>Anna Theatre: Chennai</td>
      <td>94.600000</td>
      <td>364</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>185</th>
      <td>Chennai</td>
      <td>Annai Karumari, Virugambakkam</td>
      <td>NaN</td>
      <td>196</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>186</th>
      <td>Chennai</td>
      <td>Arvind Theatre A/C dts</td>
      <td>NaN</td>
      <td>445</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>187</th>
      <td>Chennai</td>
      <td>AVM Rajeswari A/C dts</td>
      <td>NaN</td>
      <td>603</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>188</th>
      <td>Chennai</td>
      <td>Baby Albert Theatre, Whannels Road</td>
      <td>NaN</td>
      <td>242</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>189</th>
      <td>Chennai</td>
      <td>Bala Theatre, Anna Road</td>
      <td>NaN</td>
      <td>518</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>190</th>
      <td>Chennai</td>
      <td>Bharath Theatre Dolby AtmosDolby Atmos</td>
      <td>NaN</td>
      <td>963</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>191</th>
      <td>Chennai</td>
      <td>Casino Theatre: Chennai</td>
      <td>59.000000</td>
      <td>83</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Chennai</td>
      <td>Chandran Theatre, Ashoknagar</td>
      <td>NaN</td>
      <td>515</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>193</th>
      <td>Chennai</td>
      <td>Devi Karumari A/C</td>
      <td>NaN</td>
      <td>850</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>194</th>
      <td>Chennai</td>
      <td>Devicineplex</td>
      <td>NaN</td>
      <td>2462</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>195</th>
      <td>Chennai</td>
      <td>Ega Cinema</td>
      <td>NaN</td>
      <td>1168</td>
      <td>2</td>
      <td>Multiscreen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>196</th>
      <td>Chennai</td>
      <td>Ganapathy Ram Theatre: Chennai</td>
      <td>90.000000</td>
      <td>852</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>197</th>
      <td>Chennai</td>
      <td>GK Cinemas 2K Dolby Atmos: Porur</td>
      <td>116.190000</td>
      <td>557</td>
      <td>2</td>
      <td>Multiscreen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>198</th>
      <td>Chennai</td>
      <td>INOX National: Arcot Road</td>
      <td>153.600000</td>
      <td>1182</td>
      <td>5</td>
      <td>Multiscreen</td>
      <td>Inox</td>
      <td>India</td>
    </tr>
    <tr>
      <th>199</th>
      <td>Chennai</td>
      <td>INOX: Chennai Citi Centre, Dr. RK Salai</td>
      <td>153.600000</td>
      <td>528</td>
      <td>4</td>
      <td>Multiscreen</td>
      <td>Inox</td>
      <td>India</td>
    </tr>
    <tr>
      <th>200</th>
      <td>Chennai</td>
      <td>Jothi Theatre 4K A/c DTS: ST Thomas Mount</td>
      <td>0.000000</td>
      <td>805</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>201</th>
      <td>Chennai</td>
      <td>Kamala CinemasF&amp;B;</td>
      <td>NaN</td>
      <td>586</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>202</th>
      <td>Chennai</td>
      <td>Kasi4K Dolby Atmos</td>
      <td>NaN</td>
      <td>733</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>203</th>
      <td>Chennai</td>
      <td>Krishnaveni, South Usman Raod</td>
      <td>NaN</td>
      <td>898</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>204</th>
      <td>Chennai</td>
      <td>Kumaran Theatre QUBE A/C DTS: Madipakkam</td>
      <td>0.000000</td>
      <td>1008</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>205</th>
      <td>Chennai</td>
      <td>Luxe Cinemas: Chennai</td>
      <td>153.600000</td>
      <td>1844</td>
      <td>9</td>
      <td>Multiscreen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>206</th>
      <td>Chennai</td>
      <td>Mahalakshmi Talkies, Strahans Road</td>
      <td>NaN</td>
      <td>1040</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>207</th>
      <td>Chennai</td>
      <td>Maharani Theatre 2K dts</td>
      <td>NaN</td>
      <td>910</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>208</th>
      <td>Chennai</td>
      <td>Mayura, Arakonam Road</td>
      <td>NaN</td>
      <td>474</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>209</th>
      <td>Chennai</td>
      <td>MM Theatre</td>
      <td>NaN</td>
      <td>772</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>210</th>
      <td>Chennai</td>
      <td>Murugan Cinemas - AmbatturDolby Atmos</td>
      <td>NaN</td>
      <td>960</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>211</th>
      <td>Chennai</td>
      <td>Nadhamuni Cinema</td>
      <td>NaN</td>
      <td>650</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>212</th>
      <td>Chennai</td>
      <td>Padmam, Poonamallee High Road</td>
      <td>NaN</td>
      <td>420</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>213</th>
      <td>Chennai</td>
      <td>Pandian, Moolakadai</td>
      <td>NaN</td>
      <td>1002</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>214</th>
      <td>Chennai</td>
      <td>PVR: Ampa, Chennai</td>
      <td>82.700000</td>
      <td>1794</td>
      <td>7</td>
      <td>Multiscreen</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>215</th>
      <td>Chennai</td>
      <td>PVR: Velachery, Chennai</td>
      <td>82.700000</td>
      <td>1275</td>
      <td>5</td>
      <td>Multiscreen</td>
      <td>PVR</td>
      <td>India</td>
    </tr>
    <tr>
      <th>216</th>
      <td>Chennai</td>
      <td>Raj Theatre - A/C DTS: Chennai</td>
      <td>175.000000</td>
      <td>950</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>217</th>
      <td>Chennai</td>
      <td>Rakki Cinemas - Ambattur</td>
      <td>NaN</td>
      <td>361</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>218</th>
      <td>Chennai</td>
      <td>Rohini Silver Screens: Chennai</td>
      <td>104.030000</td>
      <td>3175</td>
      <td>7</td>
      <td>Multiscreen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>219</th>
      <td>Chennai</td>
      <td>Roopam, Poonamallee High Road</td>
      <td>NaN</td>
      <td>288</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>220</th>
      <td>Chennai</td>
      <td>Sangam Cinemas</td>
      <td>NaN</td>
      <td>1662</td>
      <td>3</td>
      <td>Multiscreen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>221</th>
      <td>Chennai</td>
      <td>Saravana Theatre, Brick Kiln Road</td>
      <td>NaN</td>
      <td>600</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>222</th>
      <td>Chennai</td>
      <td>Sathyam Royapettah, Lloyds Estate</td>
      <td>NaN</td>
      <td>2283</td>
      <td>6</td>
      <td>Multiscreen</td>
      <td>SPI Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>223</th>
      <td>Chennai</td>
      <td>SK-Marlen Cinemas 2K, Guindy: Alandur</td>
      <td>150.000000</td>
      <td>229</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>224</th>
      <td>Chennai</td>
      <td>Spectrum Mall, Perambur North</td>
      <td>NaN</td>
      <td>1395</td>
      <td>5</td>
      <td>Multiscreen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>225</th>
      <td>Chennai</td>
      <td>Sri Bhuvaneshwari Theatre A/C dts</td>
      <td>NaN</td>
      <td>565</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>226</th>
      <td>Chennai</td>
      <td>Sri Ganga Cinemas Dolby Atmos - KolathurDolby ...</td>
      <td>NaN</td>
      <td>772</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>227</th>
      <td>Chennai</td>
      <td>Sri Murugan, Ambattur</td>
      <td>NaN</td>
      <td>960</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>228</th>
      <td>Chennai</td>
      <td>Srinivasa Theatre</td>
      <td>NaN</td>
      <td>900</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>229</th>
      <td>Chennai</td>
      <td>The Forum Vijaya Mall, Vadapalani</td>
      <td>NaN</td>
      <td>3010</td>
      <td>9</td>
      <td>Multiscreen</td>
      <td>SPI Cinemas</td>
      <td>India</td>
    </tr>
    <tr>
      <th>230</th>
      <td>Chennai</td>
      <td>Thirumurugan, Ambattur</td>
      <td>NaN</td>
      <td>510</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>231</th>
      <td>Chennai</td>
      <td>Udhayam Complex</td>
      <td>NaN</td>
      <td>759</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>232</th>
      <td>Chennai</td>
      <td>Udhayam Theatre, Ashoknagar</td>
      <td>NaN</td>
      <td>759</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>233</th>
      <td>Chennai</td>
      <td>Vetrrivel Theatre 2K - Nanganallur</td>
      <td>NaN</td>
      <td>600</td>
      <td>1</td>
      <td>Single Screen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
    <tr>
      <th>234</th>
      <td>Chennai</td>
      <td>Woodlands Complex: Chennai</td>
      <td>69.500000</td>
      <td>1713</td>
      <td>2</td>
      <td>Multiscreen</td>
      <td>Other</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
</div>


