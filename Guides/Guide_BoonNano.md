# Guide: BoonNano
<br/>

## General
### [GET /expert/version](../Functions/get_version.md)
>returns the version number of the API that is currently running

### [POST /expert/settings](../Functions/post_settings.md)
>set new settings for the server

### [GET /expert/settings](../Functions/get_settings.md)
>get the current settings associated with the server

<br/>

## Instances
### [POST /expert/v2/nanoInstance](../Functions/post_nanoInstance.md) <br/> [POST /expert/v2/nanoInstance/{instanceID}](../Functions/post_nanoInstance.md)
>initializes a nano instance (either using the given ID or using the next available index)

### [POST /expert/v2/nanoInstance/{instanceID}](../Functions/get_nanoInstance.md)
>checks whether the given instanceID is an instantiated instance

### [DELETE /expert/v2/nanoInstances](../Functions/delete_nanoInstance.md) <br/> [DELETE /expert/v2/nanoInstance/{instanceID}](../Functions/delete_nanoInstance.md)
>deletes the specified instance or deletes all running instances (if no ID is given)

### [GET /expert/v2/nanoInstances](../Functions/get_nanoInstances.md)
>returns a list of running instance IDs

### [POST /expert/v2/snapshot/{instanceID}](../Functions/post_snapshot.md)
>loads previous nano settings and status to the instantiated instance

### [GET /expert/v2/snapshot/{instanceID}](../Functions/get_snapshot.md)
>saves the nano in its current state as a compressed serialized file

### [POST /expert/v2/subscriber/{instanceID}](../Functions/post_subscriber.md)
>set up a subscriber to send the nano results to

### [GET /expert/v2/subscriber/{instanceID}](../Functions/get_subscriber.md)
>return a list of subscribers currently set up with the instance

### [DELETE /expert/v2/subscriber/{instanceID}](../Functions/delete_subscriber.md)
>deletes all the subscribers

<br/>

## Configuration

### [GET /expert/v2/configTemplate](../Functions/get_configTemplate.md)
>returns a formatted json block from the given parameters

### [POST /expert/v2/clusterConfig/{instanceID}](../Functions/post_clusterConfig.md)
>loads the given configuration to the nano

### [GET /expert/v2/clusterConfig/{instanceID}](../Functions/get_clusterConfig.md)
>returns the json block containing the config parameters: mins, maxes, weights, labels (if applicable), numeric type, percent variation, streaming window size, and accuracy

### [POST /expert/v2/autoTuneConfig/{instanceID}](../Functions/post_autoTuneConfig.md)
>calculates and posts ideal clustering parameters for the given data in the buffer

### [POST /expert/v2/anomalyThreshold/{instanceID}](../Functions/post_anomalyThreshold.md)
>set a threshold for flagging anomalies with regards tot he anomaly index

### [GET /expert/v2/anomalyThreshold/{instanceID}](../Functions/get_anomalyThreshold.md)
>returns the current anomaly threshold set in the nano settings

<br/>

## Cluster
### [POST /expert/v2/data/{instanceID}](../Functions/post_data.md)
>uploads data to the buffer to be clustered

### [GET /expert/v2/bufferStatus/{instanceID}](../Functions/get_bufferStatus.md)
>returns the byte information about the status of the nano

### [POST /expert/v2/nanoRun/{instanceID}](../Functions/post_nanoRun.md)
>clusters the data in the buffer

### [GET /expert/v2/nanoResults/{instanceID}](../Functions/get_nanoResults.md)
>returns status results for each pattern clustered

### [GET /expert/v2/nanoStatus/{instanceID}](../Functions/get_nanoStatus.md)
>returns results for each cluster created

<br/>

[Return to documentation homepage](../Swagger_Landing_Page.md)
