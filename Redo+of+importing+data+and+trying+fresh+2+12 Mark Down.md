
import pandas as pd
import json
import os


```python
# FINALLY got past this cell having errors after trying to get it right in this and the below cells and a separate 
# notebook way too long and convaluted yesterday, continuing with these 2 working lines of code further down
# and commenting out the in between

file1 = r"C:\Users\Amy\PandasHW\purchase_data.json"
data = open(file1)

#purch_data1 = json.read(file1)

```


```python
#print(file)
```

    \..PandasHW\purchase_data.json
    


```python
#jsonpath = os.path.join("PandasHW", "purchase_data.json")
```


```python
#data = json.dump(C:/Users/Amy/PandasHW/purchase_data.json, orient=index, typ=Frame, dtype=True, convert_axes=True, convert_dates=True, keep_default_dates=True, numpy=False, precise_float=False, date_unit=None, encoding=None, lines=False, chunksize=None) 
```


```python
file1 = os.path.realpath(r"C:\Users\Amy\PandasHW\purchase_data.json")
data = open(file1)
with open(file1) as f:
    data.append(json.load(f))

```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-133-4b0f6858f7fd> in <module>()
          2 data = open(file1)
          3 with open(file1) as f:
    ----> 4     data.append(json.load(f))
    

    AttributeError: '_io.TextIOWrapper' object has no attribute 'append'



```python
#print(file1)
```

    C:\Users\Amy\PandasHW\purchase_data.json
    


```python
#starting over again now that I think I has to be a text file :\

mydata = pd.read_table("C:\\Users\\Amy\\PandasHW\\willitworkpurchase_data.txt")
```


```python
purch_data1 = pd.DataFrame.from_dict(mydata)
```


```python
#This is as far as I got before I needed to leave for class :(
print(purch_data1)
```

                                                          [
    0                                                     {
    1                                    "SN": "Aelalis34",
    2                                            "Age": 38,
    3                                     "Gender": "Male",
    4                                       "Item ID": 165,
    5             "Item Name": "Bone Crushing Silver Ske...
    6                                         "Price": 3.37
    7                                                    },
    8                                                     {
    9                                       "SN": "Eolo46",
    10                                           "Age": 21,
    11                                    "Gender": "Male",
    12                                      "Item ID": 119,
    13            "Item Name": "Stormbringer, Dark Blade...
    14                                        "Price": 2.32
    15                                                   },
    16                                                    {
    17                                 "SN": "Assastnya25",
    18                                           "Age": 34,
    19                                    "Gender": "Male",
    20                                      "Item ID": 174,
    21                      "Item Name": "Primitive Blade",
    22                                        "Price": 2.46
    23                                                   },
    24                                                    {
    25                                "SN": "Pheusrical25",
    26                                           "Age": 21,
    27                                    "Gender": "Male",
    28                                       "Item ID": 92,
    29                         "Item Name": "Final Critic",
    ...                                                 ...
    6211                                  "Gender": "Male",
    6212                                    "Item ID": 104,
    6213                 "Item Name": "Gladiator's Glaive",
    6214                                      "Price": 1.36
    6215                                                 },
    6216                                                  {
    6217                                "SN": "Tillyrin30",
    6218                                         "Age": 20,
    6219                                  "Gender": "Male",
    6220                                    "Item ID": 117,
    6221          "Item Name": "Heartstriker, Legacy of ...
    6222                                      "Price": 4.15
    6223                                                 },
    6224                                                  {
    6225                                "SN": "Quelaton80",
    6226                                         "Age": 20,
    6227                                  "Gender": "Male",
    6228                                     "Item ID": 75,
    6229            "Item Name": "Brutality Ivory Warmace",
    6230                                      "Price": 1.72
    6231                                                 },
    6232                                                  {
    6233                                    "SN": "Alim85",
    6234                                         "Age": 23,
    6235                                "Gender": "Female",
    6236                                    "Item ID": 107,
    6237          "Item Name": "Splitter, Foe Of Subtlety",
    6238                                      "Price": 3.61
    6239                                                  }
    6240                                                  ]
    
    [6241 rows x 1 columns]
    
