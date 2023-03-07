# \GroupsApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddFeedToGroup**](GroupsApi.md#AddFeedToGroup) | **Post** /{username}/groups/{group_key}/add | Add an existing Feed to a Group
[**AllGroupFeeds**](GroupsApi.md#AllGroupFeeds) | **Get** /{username}/groups/{group_key}/feeds | All feeds for current user in a given group
[**AllGroups**](GroupsApi.md#AllGroups) | **Get** /{username}/groups | All groups for current user
[**CreateGroup**](GroupsApi.md#CreateGroup) | **Post** /{username}/groups | Create a new Group
[**DestroyGroup**](GroupsApi.md#DestroyGroup) | **Delete** /{username}/groups/{group_key} | Delete an existing Group
[**GetGroup**](GroupsApi.md#GetGroup) | **Get** /{username}/groups/{group_key} | Returns Group based on ID
[**RemoveFeedFromGroup**](GroupsApi.md#RemoveFeedFromGroup) | **Post** /{username}/groups/{group_key}/remove | Remove a Feed from a Group
[**ReplaceGroup**](GroupsApi.md#ReplaceGroup) | **Put** /{username}/groups/{group_key} | Replace an existing Group
[**UpdateGroup**](GroupsApi.md#UpdateGroup) | **Patch** /{username}/groups/{group_key} | Update properties of an existing Group


# **AddFeedToGroup**
> Group AddFeedToGroup(ctx, groupKey, username, optional)
Add an existing Feed to a Group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **groupKey** | **string**|  | 
  **username** | **string**| a valid username string | 
 **optional** | ***GroupsApiAddFeedToGroupOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GroupsApiAddFeedToGroupOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **feedKey** | **optional.String**|  | 

### Return type

[**Group**](Group.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AllGroupFeeds**
> []Feed AllGroupFeeds(ctx, groupKey, username)
All feeds for current user in a given group

The Group Feeds endpoint returns information about the user's feeds. The response includes the latest value of each feed, and other metadata about each feed, but only for feeds within the given group.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **groupKey** | **string**|  | 
  **username** | **string**| a valid username string | 

### Return type

[**[]Feed**](Feed.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **AllGroups**
> []Group AllGroups(ctx, username)
All groups for current user

The Groups endpoint returns information about the user's groups. The response includes the latest value of each feed in the group, and other metadata about the group. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 

### Return type

[**[]Group**](Group.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateGroup**
> Group CreateGroup(ctx, username, group)
Create a new Group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **group** | [**Group**](Group.md)|  | 

### Return type

[**Group**](Group.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DestroyGroup**
> string DestroyGroup(ctx, username, groupKey)
Delete an existing Group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 

### Return type

**string**

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetGroup**
> Group GetGroup(ctx, username, groupKey)
Returns Group based on ID

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 

### Return type

[**Group**](Group.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RemoveFeedFromGroup**
> Group RemoveFeedFromGroup(ctx, groupKey, username, optional)
Remove a Feed from a Group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **groupKey** | **string**|  | 
  **username** | **string**| a valid username string | 
 **optional** | ***GroupsApiRemoveFeedFromGroupOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GroupsApiRemoveFeedFromGroupOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **feedKey** | **optional.String**|  | 

### Return type

[**Group**](Group.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ReplaceGroup**
> Group ReplaceGroup(ctx, username, groupKey, group)
Replace an existing Group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 
  **group** | [**Group**](Group.md)|  | 

### Return type

[**Group**](Group.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateGroup**
> Group UpdateGroup(ctx, username, groupKey, group)
Update properties of an existing Group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 
  **group** | [**Group**](Group.md)|  | 

### Return type

[**Group**](Group.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

