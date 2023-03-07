# \FeedsApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddFeedToGroup**](FeedsApi.md#AddFeedToGroup) | **Post** /{username}/groups/{group_key}/add | Add an existing Feed to a Group
[**AllFeeds**](FeedsApi.md#AllFeeds) | **Get** /{username}/feeds | All feeds for current user
[**AllGroupFeeds**](FeedsApi.md#AllGroupFeeds) | **Get** /{username}/groups/{group_key}/feeds | All feeds for current user in a given group
[**CreateFeed**](FeedsApi.md#CreateFeed) | **Post** /{username}/feeds | Create a new Feed
[**CreateGroupFeed**](FeedsApi.md#CreateGroupFeed) | **Post** /{username}/groups/{group_key}/feeds | Create a new Feed in a Group
[**DestroyFeed**](FeedsApi.md#DestroyFeed) | **Delete** /{username}/feeds/{feed_key} | Delete an existing Feed
[**GetFeed**](FeedsApi.md#GetFeed) | **Get** /{username}/feeds/{feed_key} | Get feed by feed key
[**GetFeedDetails**](FeedsApi.md#GetFeedDetails) | **Get** /{username}/feeds/{feed_key}/details | Get detailed feed by feed key
[**RemoveFeedFromGroup**](FeedsApi.md#RemoveFeedFromGroup) | **Post** /{username}/groups/{group_key}/remove | Remove a Feed from a Group
[**ReplaceFeed**](FeedsApi.md#ReplaceFeed) | **Put** /{username}/feeds/{feed_key} | Replace an existing Feed
[**UpdateFeed**](FeedsApi.md#UpdateFeed) | **Patch** /{username}/feeds/{feed_key} | Update properties of an existing Feed


# **AddFeedToGroup**
> Group AddFeedToGroup(ctx, groupKey, username, optional)
Add an existing Feed to a Group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **groupKey** | **string**|  | 
  **username** | **string**| a valid username string | 
 **optional** | ***FeedsApiAddFeedToGroupOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FeedsApiAddFeedToGroupOpts struct

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

# **AllFeeds**
> []Feed AllFeeds(ctx, username)
All feeds for current user

The Feeds endpoint returns information about the user's feeds. The response includes the latest value of each feed, and other metadata about each feed.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 

### Return type

[**[]Feed**](Feed.md)

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

# **CreateFeed**
> Feed CreateFeed(ctx, username, feed, optional)
Create a new Feed



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feed** | [**Feed**](Feed.md)|  | 
 **optional** | ***FeedsApiCreateFeedOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FeedsApiCreateFeedOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **groupKey** | **optional.String**|  | 

### Return type

[**Feed**](Feed.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateGroupFeed**
> Feed CreateGroupFeed(ctx, username, groupKey, feed)
Create a new Feed in a Group



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **groupKey** | **string**|  | 
  **feed** | [**Feed**](Feed.md)|  | 

### Return type

[**Feed**](Feed.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DestroyFeed**
> DestroyFeed(ctx, username, feedKey)
Delete an existing Feed



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 

### Return type

 (empty response body)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetFeed**
> Feed GetFeed(ctx, username, feedKey)
Get feed by feed key

Returns feed based on the feed key

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 

### Return type

[**Feed**](Feed.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetFeedDetails**
> Feed GetFeedDetails(ctx, username, feedKey)
Get detailed feed by feed key

Returns more detailed feed record based on the feed key

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 

### Return type

[**Feed**](Feed.md)

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
 **optional** | ***FeedsApiRemoveFeedFromGroupOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FeedsApiRemoveFeedFromGroupOpts struct

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

# **ReplaceFeed**
> Feed ReplaceFeed(ctx, username, feedKey, feed)
Replace an existing Feed



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
  **feed** | [**Feed**](Feed.md)|  | 

### Return type

[**Feed**](Feed.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateFeed**
> Feed UpdateFeed(ctx, username, feedKey, feed)
Update properties of an existing Feed



### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| a valid username string | 
  **feedKey** | **string**| a valid feed key | 
  **feed** | [**Feed**](Feed.md)|  | 

### Return type

[**Feed**](Feed.md)

### Authorization

[HeaderKey](../README.md#HeaderKey), [HeaderSignature](../README.md#HeaderSignature), [QueryKey](../README.md#QueryKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

