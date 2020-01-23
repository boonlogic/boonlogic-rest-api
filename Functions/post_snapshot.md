![Logo](../images/BoonLogic.png)
# **POST snapshot**
<br/>

#### Loads a serialized version of the nano
##### input
>`instanceID`
>>*label for the nano*
>
>`snapshot`
>>*tar file to upload containing a serialized nano*

#### output
```json
  {
    "numericFormat": "int16",
    "features": [
      {
        "minVal": 0,
        "maxVal": 1,
        "weight": 1,
        "label": ""
      }
    ],
    "percentVariation": 0.05,
    "accuracy": 0.99,
    "streamingWindowSize": 1
  }
```

<br/>

[back to list](../Guides/Guide_Boon_Nano.md)
