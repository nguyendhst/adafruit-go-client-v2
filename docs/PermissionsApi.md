# \PermissionsApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AllPermissions**](PermissionsApi.md#AllPermissions) | **Get** /{username}/{type}/{type_id}/acl | All permissions for current user and type
[**CreatePermission**](PermissionsApi.md#CreatePermission) | **Post** /{username}/{type}/{type_id}/acl | Create a new Permission
[**DestroyPermission**](PermissionsApi.md#DestroyPermission) | **Delete** /{username}/{type}/{type_id}/acl/{id} | Delete an existing Permission
[**GetPermission**](PermissionsApi.md#GetPermission) | **Get** /{username}/{type}/{type_id}/acl/{id} | Returns Permission based on ID
[**ReplacePermission**](PermissionsApi.md#ReplacePermission) | **Put** /{username}/{type}/{type_id}/acl/{id} | Replace an existing Permission
[**UpdatePermission**](PermissionsApi.md#UpdatePermission) | **Patch** /{username}/{type}/{type_id}/acl/{id} | Update properties of an existing Permission


# **AllPermissions**
> []Permission AllPermissions(ctx, username, type_, typeId)
All permissions for current user and type

The Permissions endpoint returns information about the user's permissions. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **type_** | **string**|  | 
  **typeId** | **string**|  | 

### Return type

[**[]Permission**](Permission.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreatePermission**
> Permission CreatePermission(ctx, username, type_, typeId, permission)
Create a new Permission



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **type_** | **string**|  | 
  **typeId** | **string**|  | 
  **permission** | [**Permission**](Permission.md)|  | 

### Return type

[**Permission**](Permission.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DestroyPermission**
> string DestroyPermission(ctx, username, type_, typeId, id)
Delete an existing Permission



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **type_** | **string**|  | 
  **typeId** | **string**|  | 
  **id** | **string**|  | 

### Return type

**string**

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetPermission**
> Permission GetPermission(ctx, username, type_, typeId, id)
Returns Permission based on ID



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **type_** | **string**|  | 
  **typeId** | **string**|  | 
  **id** | **string**|  | 

### Return type

[**Permission**](Permission.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ReplacePermission**
> Permission ReplacePermission(ctx, username, type_, typeId, id, permission)
Replace an existing Permission



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **type_** | **string**|  | 
  **typeId** | **string**|  | 
  **id** | **string**|  | 
  **permission** | [**Permission**](Permission.md)|  | 

### Return type

[**Permission**](Permission.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdatePermission**
> Permission UpdatePermission(ctx, username, type_, typeId, id, permission)
Update properties of an existing Permission



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **type_** | **string**|  | 
  **typeId** | **string**|  | 
  **id** | **string**|  | 
  **permission** | [**Permission**](Permission.md)|  | 

### Return type

[**Permission**](Permission.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

