![Logo](../images/BoonLogic.png)
# **POST autoTuneConfig**
<br/>

#### Calculates and loads an ideal clustering configuration for the current data
##### input
>`instanceID`
>>*label for the nano*
>
>`byFeature`
>>*boolean for whether to autotune the min/max per feature or overall*
>
>`autoTunePV`
>>*boolean to determine whether to autotune the percent variation*
>
>`autoTuneRange`
>>*boolean to determine whether to autotune the min and max values*
>
>`exclusions`
>>*list of columns to exclude when autotuning the range*

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
