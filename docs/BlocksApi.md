# \BlocksApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AllBlocks**](BlocksApi.md#AllBlocks) | **Get** /{username}/dashboards/{dashboard_id}/blocks | All blocks for current user
[**CreateBlock**](BlocksApi.md#CreateBlock) | **Post** /{username}/dashboards/{dashboard_id}/blocks | Create a new Block
[**DestroyBlock**](BlocksApi.md#DestroyBlock) | **Delete** /{username}/dashboards/{dashboard_id}/blocks/{id} | Delete an existing Block
[**GetBlock**](BlocksApi.md#GetBlock) | **Get** /{username}/dashboards/{dashboard_id}/blocks/{id} | Returns Block based on ID
[**ReplaceBlock**](BlocksApi.md#ReplaceBlock) | **Put** /{username}/dashboards/{dashboard_id}/blocks/{id} | Replace an existing Block
[**UpdateBlock**](BlocksApi.md#UpdateBlock) | **Patch** /{username}/dashboards/{dashboard_id}/blocks/{id} | Update properties of an existing Block


# **AllBlocks**
> []Block AllBlocks(ctx, username, dashboardId)
All blocks for current user

The Blocks endpoint returns information about the user's blocks. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **dashboardId** | **string**|  | 

### Return type

[**[]Block**](Block.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateBlock**
> Block CreateBlock(ctx, username, block, dashboardId)
Create a new Block



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **block** | [**Block**](Block.md)|  | 
  **dashboardId** | **string**|  | 

### Return type

[**Block**](Block.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DestroyBlock**
> string DestroyBlock(ctx, username, dashboardId, id)
Delete an existing Block



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **dashboardId** | **string**|  | 
  **id** | **string**|  | 

### Return type

**string**

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetBlock**
> Block GetBlock(ctx, username, dashboardId, id)
Returns Block based on ID



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **dashboardId** | **string**|  | 
  **id** | **string**|  | 

### Return type

[**Block**](Block.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ReplaceBlock**
> Block ReplaceBlock(ctx, username, dashboardId, id, block)
Replace an existing Block



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **dashboardId** | **string**|  | 
  **id** | **string**|  | 
  **block** | [**Block**](Block.md)|  | 

### Return type

[**Block**](Block.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateBlock**
> Block UpdateBlock(ctx, username, dashboardId, id, block)
Update properties of an existing Block



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **dashboardId** | **string**|  | 
  **id** | **string**|  | 
  **block** | [**Block**](Block.md)|  | 

### Return type

[**Block**](Block.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

