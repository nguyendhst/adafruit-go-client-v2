# \DashboardsApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AllDashboards**](DashboardsApi.md#AllDashboards) | **Get** /{username}/dashboards | All dashboards for current user
[**CreateDashboard**](DashboardsApi.md#CreateDashboard) | **Post** /{username}/dashboards | Create a new Dashboard
[**DestroyDashboard**](DashboardsApi.md#DestroyDashboard) | **Delete** /{username}/dashboards/{id} | Delete an existing Dashboard
[**GetDashboard**](DashboardsApi.md#GetDashboard) | **Get** /{username}/dashboards/{id} | Returns Dashboard based on ID
[**ReplaceDashboard**](DashboardsApi.md#ReplaceDashboard) | **Put** /{username}/dashboards/{id} | Replace an existing Dashboard
[**UpdateDashboard**](DashboardsApi.md#UpdateDashboard) | **Patch** /{username}/dashboards/{id} | Update properties of an existing Dashboard


# **AllDashboards**
> []Dashboard AllDashboards(ctx, username)
All dashboards for current user

The Dashboards endpoint returns information about the user's dashboards. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 

### Return type

[**[]Dashboard**](Dashboard.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateDashboard**
> Dashboard CreateDashboard(ctx, username, dashboard)
Create a new Dashboard



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **dashboard** | [**Dashboard**](Dashboard.md)|  | 

### Return type

[**Dashboard**](Dashboard.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DestroyDashboard**
> string DestroyDashboard(ctx, username, id)
Delete an existing Dashboard



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **id** | **string**|  | 

### Return type

**string**

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetDashboard**
> Dashboard GetDashboard(ctx, username, id)
Returns Dashboard based on ID



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **id** | **string**|  | 

### Return type

[**Dashboard**](Dashboard.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ReplaceDashboard**
> Dashboard ReplaceDashboard(ctx, username, id, dashboard)
Replace an existing Dashboard



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **id** | **string**|  | 
  **dashboard** | [**Dashboard**](Dashboard.md)|  | 

### Return type

[**Dashboard**](Dashboard.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateDashboard**
> Dashboard UpdateDashboard(ctx, username, id, dashboard)
Update properties of an existing Dashboard



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **id** | **string**|  | 
  **dashboard** | [**Dashboard**](Dashboard.md)|  | 

### Return type

[**Dashboard**](Dashboard.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

