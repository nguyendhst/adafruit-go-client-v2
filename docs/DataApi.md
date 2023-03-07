# \DataApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AllData**](DataApi.md#AllData) | **Get** /{username}/feeds/{feed_key}/data | Get all data for the given feed
[**AllGroupFeedData**](DataApi.md#AllGroupFeedData) | **Get** /{username}/groups/{group_key}/feeds/{feed_key}/data | All data for current feed in a specific group
[**BatchCreateData**](DataApi.md#BatchCreateData) | **Post** /{username}/feeds/{feed_key}/data/batch | Create multiple new Data records
[**BatchCreateGroupFeedData**](DataApi.md#BatchCreateGroupFeedData) | **Post** /{username}/groups/{group_key}/feeds/{feed_key}/data/batch | Create multiple new Data records in a feed belonging to a particular group
[**ChartData**](DataApi.md#ChartData) | **Get** /{username}/feeds/{feed_key}/data/chart | Chart data for current feed
[**CreateData**](DataApi.md#CreateData) | **Post** /{username}/feeds/{feed_key}/data | Create new Data
[**CreateGroupData**](DataApi.md#CreateGroupData) | **Post** /{username}/groups/{group_key}/data | Create new data for multiple feeds in a group
[**CreateGroupFeedData**](DataApi.md#CreateGroupFeedData) | **Post** /{username}/groups/{group_key}/feeds/{feed_key}/data | Create new Data in a feed belonging to a particular group
[**CreateRawWebhookFeedData**](DataApi.md#CreateRawWebhookFeedData) | **Post** /webhooks/feed/:token/raw | Send arbitrary data to a feed via webhook URL.
[**CreateWebhookFeedData**](DataApi.md#CreateWebhookFeedData) | **Post** /webhooks/feed/:token | Send data to a feed via webhook URL.
[**DestroyData**](DataApi.md#DestroyData) | **Delete** /{username}/feeds/{feed_key}/data/{id} | Delete existing Data
[**FirstData**](DataApi.md#FirstData) | **Get** /{username}/feeds/{feed_key}/data/first | First Data in Queue
[**GetData**](DataApi.md#GetData) | **Get** /{username}/feeds/{feed_key}/data/{id} | Returns data based on feed key
[**LastData**](DataApi.md#LastData) | **Get** /{username}/feeds/{feed_key}/data/last | Last Data in Queue
[**NextData**](DataApi.md#NextData) | **Get** /{username}/feeds/{feed_key}/data/next | Next Data in Queue
[**PreviousData**](DataApi.md#PreviousData) | **Get** /{username}/feeds/{feed_key}/data/previous | Previous Data in Queue
[**ReplaceData**](DataApi.md#ReplaceData) | **Put** /{username}/feeds/{feed_key}/data/{id} | Replace existing Data
[**RetainData**](DataApi.md#RetainData) | **Get** /{username}/feeds/{feed_key}/data/retain | Last Data in MQTT CSV format
[**UpdateData**](DataApi.md#UpdateData) | **Patch** /{username}/feeds/{feed_key}/data/{id} | Update properties of existing Data


# **AllData**
> []DataResponse AllData(ctx, username, feedKey, optional)
Get all data for the given feed



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
 **optional** | ***DataApiAllDataOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DataApiAllDataOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **startTime** | **optional.Time**| Start time for filtering, returns records created after given time. | 
 **endTime** | **optional.Time**| End time for filtering, returns records created before give time. | 
 **limit** | **optional.Int32**| Limit the number of records returned. | 
 **include** | **optional.String**| List of Data record fields to include in response as comma separated list. Acceptable values are: &#x60;value&#x60;, &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60;, &#x60;id&#x60;, and &#x60;created_at&#x60;.  | 

### Return type

[**[]DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AllGroupFeedData**
> []DataResponse AllGroupFeedData(ctx, username, groupKey, feedKey, optional)
All data for current feed in a specific group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 
  **feedKey** | **string**| a valid feed key | 
 **optional** | ***DataApiAllGroupFeedDataOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DataApiAllGroupFeedDataOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **startTime** | **optional.Time**| Start time for filtering data. Returns data created after given time. | 
 **endTime** | **optional.Time**| End time for filtering data. Returns data created before give time. | 
 **limit** | **optional.Int32**| Limit the number of records returned. | 

### Return type

[**[]DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **BatchCreateData**
> []DataResponse BatchCreateData(ctx, username, feedKey, data)
Create multiple new Data records

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
  **data** | [**[]Datum**](datum.md)| A collection of data records including &#x60;value&#x60; (required) and optionally including: &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60; (latitude, longitude, and elevation values), and &#x60;created_at&#x60; (a date/time string). | 

### Return type

[**[]DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **BatchCreateGroupFeedData**
> []DataResponse BatchCreateGroupFeedData(ctx, username, groupKey, feedKey, data)
Create multiple new Data records in a feed belonging to a particular group

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 
  **feedKey** | **string**| a valid feed key | 
  **data** | [**[]Datum**](datum.md)| A collection of data records including &#x60;value&#x60; (required) and optionally including: &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60; (latitude, longitude, and elevation values), and &#x60;created_at&#x60; (a date/time string). | 

### Return type

[**[]DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ChartData**
> InlineResponse2001 ChartData(ctx, username, feedKey, optional)
Chart data for current feed

The Chart API is what we use on io.adafruit.com to populate charts over varying timespans with a consistent number of data points. The maximum number of points returned is 480. This API works by aggregating slices of time into a single value by averaging.  All time-based parameters are optional, if none are given it will default to 1 hour at the finest-grained resolution possible.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
 **optional** | ***DataApiChartDataOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DataApiChartDataOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **startTime** | **optional.Time**| Start time for filtering, returns records created after given time. | 
 **endTime** | **optional.Time**| End time for filtering, returns records created before give time. | 
 **resolution** | **optional.Int32**| A resolution size in minutes. By giving a resolution value you will get back grouped data points aggregated over resolution-sized intervals. NOTE: time span is preferred over resolution, so if you request a span of time that includes more than max limit points you may get a larger resolution than you requested. Valid resolutions are 1, 5, 10, 30, 60, and 120. | 
 **hours** | **optional.Int32**| The number of hours the chart should cover. | 

### Return type

[**InlineResponse2001**](inline_response_200_1.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateData**
> Data CreateData(ctx, username, feedKey, datum)
Create new Data

Create new data records on the given feed.  **NOTE:** when feed history is on, data `value` size is limited to 1KB, when feed history is turned off data value size is limited to 100KB.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
  **datum** | [**Datum**](Datum.md)| Data record including a &#x60;value&#x60; field (required) and optionally including: &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60; (latitude, longitude, and elevation values), and &#x60;created_at&#x60; (a date/time string). | 

### Return type

[**Data**](Data.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateGroupData**
> []DataResponse CreateGroupData(ctx, username, groupKey, groupFeedData)
Create new data for multiple feeds in a group

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 
  **groupFeedData** | [**GroupFeedData**](GroupFeedData.md)|  | 

### Return type

[**[]DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateGroupFeedData**
> DataResponse CreateGroupFeedData(ctx, username, groupKey, feedKey, datum)
Create new Data in a feed belonging to a particular group

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 
  **feedKey** | **string**| a valid feed key | 
  **datum** | [**Datum**](Datum.md)| Data record including a &#x60;value&#x60; field (required) and optionally including: &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60; (latitude, longitude, and elevation values), and &#x60;created_at&#x60; (a date/time string). | 

### Return type

[**DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateRawWebhookFeedData**
> Data CreateRawWebhookFeedData(ctx, )
Send arbitrary data to a feed via webhook URL.

The raw data webhook receiver accepts POST requests and stores the raw request body on your feed. This is useful when you don't have control of the webhook sender. If feed history is turned on, payloads will be truncated at 1024 bytes. If feed history is turned off, payloads will be truncated at 100KB.

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**Data**](Data.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateWebhookFeedData**
> Data CreateWebhookFeedData(ctx, payload)
Send data to a feed via webhook URL.



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **payload** | [**Payload**](Payload.md)| Webhook payload containing data &#x60;value&#x60; parameter. | 

### Return type

[**Data**](Data.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DestroyData**
> string DestroyData(ctx, username, feedKey, id)
Delete existing Data



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
  **id** | **string**|  | 

### Return type

**string**

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FirstData**
> DataResponse FirstData(ctx, username, feedKey, optional)
First Data in Queue

Get the oldest data point in the feed. This request sets the queue pointer to the beginning of the feed.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
 **optional** | ***DataApiFirstDataOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DataApiFirstDataOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **include** | **optional.String**| List of Data record fields to include in response as comma separated list. Acceptable values are: &#x60;value&#x60;, &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60;, &#x60;id&#x60;, and &#x60;created_at&#x60;.  | 

### Return type

[**DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetData**
> DataResponse GetData(ctx, username, feedKey, id, optional)
Returns data based on feed key



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
  **id** | **string**|  | 
 **optional** | ***DataApiGetDataOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DataApiGetDataOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **include** | **optional.String**| List of Data record fields to include in response as comma separated list. Acceptable values are: &#x60;value&#x60;, &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60;, &#x60;id&#x60;, and &#x60;created_at&#x60;.  | 

### Return type

[**DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **LastData**
> DataResponse LastData(ctx, username, feedKey, optional)
Last Data in Queue

Get the most recent data point in the feed. This request sets the queue pointer to the end of the feed.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
 **optional** | ***DataApiLastDataOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DataApiLastDataOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **include** | **optional.String**| List of Data record fields to include in response as comma separated list. Acceptable values are: &#x60;value&#x60;, &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60;, &#x60;id&#x60;, and &#x60;created_at&#x60;.  | 

### Return type

[**DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **NextData**
> DataResponse NextData(ctx, username, feedKey, optional)
Next Data in Queue

Get the next newest data point in the feed. If queue processing hasn't been started, the first data point in the feed will be returned.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
 **optional** | ***DataApiNextDataOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DataApiNextDataOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **include** | **optional.String**| List of Data record fields to include in response as comma separated list. Acceptable values are: &#x60;value&#x60;, &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60;, &#x60;id&#x60;, and &#x60;created_at&#x60;.  | 

### Return type

[**DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **PreviousData**
> DataResponse PreviousData(ctx, username, feedKey, optional)
Previous Data in Queue

Get the previously processed data point in the feed. NOTE: this method doesn't move the processing queue pointer.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
 **optional** | ***DataApiPreviousDataOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DataApiPreviousDataOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **include** | **optional.String**| List of Data record fields to include in response as comma separated list. Acceptable values are: &#x60;value&#x60;, &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60;, &#x60;id&#x60;, and &#x60;created_at&#x60;.  | 

### Return type

[**DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ReplaceData**
> DataResponse ReplaceData(ctx, username, feedKey, id, datum)
Replace existing Data



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
  **id** | **string**|  | 
  **datum** | [**Datum**](Datum.md)| Data record including a &#x60;value&#x60; field (required) and optionally including: &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60; (latitude, longitude, and elevation values), and &#x60;created_at&#x60; (a date/time string). | 

### Return type

[**DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RetainData**
> string RetainData(ctx, username, feedKey)
Last Data in MQTT CSV format

Get the most recent data point in the feed in an MQTT compatible CSV format: `value,lat,lon,ele`

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 

### Return type

**string**

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateData**
> DataResponse UpdateData(ctx, username, feedKey, id, datum)
Update properties of existing Data



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
  **id** | **string**|  | 
  **datum** | [**Datum**](Datum.md)| Data record including a &#x60;value&#x60; field (required) and optionally including: &#x60;lat&#x60;, &#x60;lon&#x60;, &#x60;ele&#x60; (latitude, longitude, and elevation values), and &#x60;created_at&#x60; (a date/time string). | 

### Return type

[**DataResponse**](DataResponse.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

