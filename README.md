
In [ ]:
import pandas as pd
import numpy as np
In [ ]:
from google.colab import files
uploaded=files.upload()
Saving 5.16.csv to 5.16.csv
In [ ]:
df=pd.read_csv("5.16.csv")
In [ ]:
print(df)
               State more than two times one or two times  Not Applicable
0     Andhra Pradesh                  50               50               0
1              Assam                  50               50               0
2              Bihar                 100                0               0
3            Gujarat                   0                0             100
4            Haryana                  50               50               0
5   Himachal Pradesh                   0                0             100
6          Jharkhand                 100                0               0
7          Karnataka                  50               50               0
8     Madhya Pradesh                43.3              NAN               0
9             Odisha                  55               45               0
10            Punjab                 NAN                0             100
11         Rajasthan                  90               10               0
12        Tamil Nadu                 100                0               0
13     Uttar Pradesh                49.7             50.3               0
14       West Bengal                  45              NAN               0
In [ ]:
df.head()
Out[ ]:
State	more than two times	one or two times	Not Applicable
0	Andhra Pradesh	50	50	0
1	Assam	50	50	0
2	Bihar	100	0	0
3	Gujarat	0	0	100
4	Haryana	50	50	0
In [ ]:
df.tail()
Out[ ]:
State	more than two times	one or two times	Not Applicable
10	Punjab	NAN	0	100
11	Rajasthan	90	10	0
12	Tamil Nadu	100	0	0
13	Uttar Pradesh	49.7	50.3	0
14	West Bengal	45	NAN	0
In [ ]:
x=df["State"]
print(x)
0       Andhra Pradesh
1                Assam
2                Bihar
3              Gujarat
4              Haryana
5     Himachal Pradesh
6            Jharkhand
7            Karnataka
8       Madhya Pradesh
9               Odisha
10              Punjab
11           Rajasthan
12          Tamil Nadu
13       Uttar Pradesh
14         West Bengal
Name: State, dtype: object
In [ ]:
y=df["more than two times"]
print(y)
0       50
1       50
2      100
3        0
4       50
5        0
6      100
7       50
8     43.3
9       55
10     NAN
11      90
12     100
13    49.7
14      45
Name: more than two times, dtype: object
In [ ]:
import matplotlib.pyplot as plt
In [ ]:
df.plot.bar()
plt.title("bar plot")
Out[ ]:
Text(0.5, 1.0, 'bar plot')

In [ ]:
df.plot.hist()
plt.title("hist plot")
Out[ ]:
Text(0.5, 1.0, 'hist plot')

In [ ]:
df.boxplot()
plt.title("box plot")
Out[ ]:
Text(0.5, 1.0, 'box plot')

In [ ]:
df.describe()
Out[ ]:
Not Applicable
count	15.000000
mean	20.000000
std	41.403934
min	0.000000
25%	0.000000
50%	0.000000
75%	0.000000
max	100.000000
In [ ]:
#df.plot
Out[ ]:
<pandas.plotting._core.PlotAccessor object at 0x7fe177121828>
In [ ]:
df.mode()
Out[ ]:
State	more than two times	one or two times	Not Applicable
0	Andhra Pradesh	50	0	0.0
1	Assam	NaN	NaN	NaN
2	Bihar	NaN	NaN	NaN
3	Gujarat	NaN	NaN	NaN
4	Haryana	NaN	NaN	NaN
5	Himachal Pradesh	NaN	NaN	NaN
6	Jharkhand	NaN	NaN	NaN
7	Karnataka	NaN	NaN	NaN
8	Madhya Pradesh	NaN	NaN	NaN
9	Odisha	NaN	NaN	NaN
10	Punjab	NaN	NaN	NaN
11	Rajasthan	NaN	NaN	NaN
12	Tamil Nadu	NaN	NaN	NaN
13	Uttar Pradesh	NaN	NaN	NaN
14	West Bengal	NaN	NaN	NaN
In [ ]:

In [ ]:
df.mean()
Out[ ]:
Not Applicable    20.0
dtype: float64
In [ ]:
df.median()
Out[ ]:
more than two times    50.0
one or two times       10.0
Not Applicable          0.0
dtype: float64
In [ ]:
df.min()
Out[ ]:
State                  Andhra Pradesh
more than two times                 0
one or two times                    0
Not Applicable                      0
dtype: object
In [ ]:
df.max()
Out[ ]:
State                  West Bengal
more than two times            NAN
one or two times               NAN
Not Applicable                 100
dtype: object
In [ ]:
df.corr()
Out[ ]:
Not Applicable
Not Applicable	1.0
In [ ]:
df.all()
Out[ ]:
State                   True
more than two times     True
one or two times        True
Not Applicable         False
dtype: bool
In [ ]:
df.any()
Out[ ]:
State                  True
more than two times    True
one or two times       True
Not Applicable         True
dtype: bool
