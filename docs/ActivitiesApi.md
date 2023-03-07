# \ActivitiesApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AllActivities**](ActivitiesApi.md#AllActivities) | **Get** /{username}/activities | All activities for current user
[**DestroyActivities**](ActivitiesApi.md#DestroyActivities) | **Delete** /{username}/activities | All activities for current user
[**GetActivity**](ActivitiesApi.md#GetActivity) | **Get** /{username}/activities/{type} | Get activities by type for current user


# **AllActivities**
> []Activity AllActivities(ctx, username, optional)
All activities for current user

The Activities endpoint returns information about the user's activities.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
 **optional** | ***ActivitiesApiAllActivitiesOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a ActivitiesApiAllActivitiesOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **startTime** | **optional.Time**| Start time for filtering, returns records created after given time. | 
 **endTime** | **optional.Time**| End time for filtering, returns records created before give time. | 
 **limit** | **optional.Int32**| Limit the number of records returned. | 

### Return type

[**[]Activity**](Activity.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DestroyActivities**
> DestroyActivities(ctx, username)
All activities for current user

Delete all your activities.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 

### Return type

 (empty response body)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetActivity**
> []Activity GetActivity(ctx, username, type_, optional)
Get activities by type for current user

The Activities endpoint returns information about the user's activities.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **type_** | **string**|  | 
 **optional** | ***ActivitiesApiGetActivityOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a ActivitiesApiGetActivityOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **startTime** | **optional.Time**| Start time for filtering, returns records created after given time. | 
 **endTime** | **optional.Time**| End time for filtering, returns records created before give time. | 
 **limit** | **optional.Int32**| Limit the number of records returned. | 

### Return type

[**[]Activity**](Activity.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

