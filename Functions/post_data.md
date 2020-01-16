# **POST data**
<br/>

#### Loads data into the buffer for clustering
##### input
>`instanceID`
>>*label for the nano*
>
>`data`
>>*binary or csv file to upload*
>
>`metadata`
>>*pre-processing information*  
>>*NOTE: obsolete function*
>
>`runNano`
>>*boolean for whether to cluster after uploading data*
>
>`fileType`
>>*specify csv or raw(binary)*
>
>`gzip`
>>*boolean for whether the data is zipped*
>
>`results`
>>*option to return results if clustering the data in this step*
>
>`appendData`
>>*boolean for whether to add to buffer or replace contents with new data*

#### output
```json
  {
    "ID": [
      0
    ],
    "SI": [
      0
    ],
    "RI": [
      0
    ],
    "FI": [
      0
    ],
    "DI": [
      0
    ],
    "MD": [
      "string"
    ]
  }
```

<br/>

[back to list](../Guides/Guide_Boon_Nano.md)
