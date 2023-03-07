# \UsersApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CurrentUser**](UsersApi.md#CurrentUser) | **Get** /user | Get information about the current user
[**GetCurrentUserThrottle**](UsersApi.md#GetCurrentUserThrottle) | **Get** /{username}/throttle | Get the user&#39;s data rate limit and current activity level.


# **CurrentUser**
> User CurrentUser(ctx, )
Get information about the current user

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**User**](User.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetCurrentUserThrottle**
> InlineResponse200 GetCurrentUserThrottle(ctx, username)
Get the user's data rate limit and current activity level.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 

### Return type

[**InlineResponse200**](inline_response_200.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

