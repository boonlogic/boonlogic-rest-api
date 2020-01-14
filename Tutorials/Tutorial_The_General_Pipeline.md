# Tutorial: The General Pipeline

If you have already authenticated the web page, skip to [Initialize Instance](#instance)
### Getting Started
1. Open web browser
2. In the URL, go to the web address assigned to your account. It should be your api-tenant followed by boonlogic.com. For example: https://6d4ed33b636a961b.boonlogic.com. This link can be found in the .BoonLogic file which was included in the account generation.

3. There should be a title that says: `Boon Logic BoonNano API`
4. Copy your unique api-key associated with your account from the .BoonLogic file.
2. In the Swagger web page, on the right side after the title panel, click on the green button labeled `Authorize` with a lock
3. When prompted, enter the copied api key in the `Value` field
4. Click `Authorize`

### Initialize Instance {#instance}
1. Click on the header labelled `instances` (second from the top)
2. Find and click on the first green `POST` option which is labelled `/expert/v2/nanoInstance`
3. On the right side under the green bar, click on `Try it out`
4. Two new buttons will appear. Choose `Execute`
5. A few lines down there is a header labelled `Code` followed by `Details` on the same line. Immediately under that is the response code to the request. For a successful request, the code should be `200` with a JSON block containing the instance ID on the same line.

    ```json
    {
      "instanceID": 0
    }
    ```

### Load the Configuration
1. Scroll down to find the next header labelled `configuration`. Click on it to expand the options.
2. The first option is a blue `GET` command labelled `expert/v2/configTemplate`. Click on the blue bar to expand the command.
3. Click on `Try it out` on the right hand side.
4. Fill in each field with the following values:  

    | variable | value |
    | ---| ---|
    | featureCount | 20 |
    | minVal | -10 |
    | maxVal | 15 |
    | weight | 1 |
    | percentVariation | 0.037 |
    | streamingWindowSize | 1 |
    | accuracy | 0.99 |

5. After the last variable, click on the blue `Execute` button.
6. A few lines down, there is the `Code` and `Details` header followed by a number and a `Response body` on the next line. If the number is `200`, highlight the entire JSON block in the `Response body` field. Save to clipboard.
7. Scroll down the webpage to the next rest call. It should be a green `POST` labelled `/expert/v2/clusterConfig/{instanceID}`. Click on the call bar and click the `Try it out` button on the right.
8. In the `instanceID` field, enter 0. This should match the integer you got as a result from [Initialize Instance](#instance).
9. Select everything in the `config` field. Paste the JSON block copied from step 6 so that it replaces what was there.
10. Click the blue `Execute` button.
11. A few lines down, find the `Code`/`Details` line and the results after it. The code should be `200` and the `Response body` should match exactly what was copied to your clipboard.

### Post Data
1. First download the example dataset from [Github](https://github.com/elc73527/BoonNano_APIs/blob/master/Data.csv)
1. Scroll all the way to the bottom of the webpage. The second to last header is labelled `cluster`. Click on the header to expand the options.
2. The first call after `cluster` should be a green `POST` labelled `expert/v2/data/`. Click on the title to expand the call and click the `Try it out` button on the right.
3. The first input field is labelled `instanceID`. In the input field, enter 0. Again, this should be the integer result from the [Initialize Instance](#instance) section.
4. The second input is labelled `data`. Click on the `Choose File` button and select the `Data.csv` file.
5. Fill in the following fields with the given values:

    | variable | value |
    | --- | --- |
    | fileType | csv |
    | gzip | false |
    | metadata |  |
    | appendData | false |
    | runNano | false |
    | results | -- |

6. Click the blue `Execute` button.
7. Check the result under the `Code` and `Details` heading for code `200` and `Response headers`
```
content-length: 0
content-type: application/json
date: Thu, 31 Oct 2019 15:00:27 GMT
```

### Run Nano
1. Scroll down the webpage to the next green header bar labelled `POST` `/expert/v2/nanoRun/{instanceID}`. Click on the bar to expand the options.
2. Click on the `Try it out` button on the right.
3. In the field labelled `instanceID`, enter 0 - the same value from the [Initialize Instance](#instance) section.
4. In the `results` field, select `--`.
3. Click on the blue `Execute` button.
2. Finally, double check the results code. Under the `Code` and `Details` header, the value should be `200` and the `Response body` should be {}.

  Congratulations! You have successfully clustered the data!   
  See [Guide: BoonNano](../Guides/Guide_BoonNano.md) for more information on function calls.

[Return to documentation homepage](../Swagger_Landing_Page.md)
