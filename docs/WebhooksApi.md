# \WebhooksApi

All URIs are relative to *https://io.adafruit.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateRawWebhookFeedData**](WebhooksApi.md#CreateRawWebhookFeedData) | **Post** /webhooks/feed/:token/raw | Send arbitrary data to a feed via webhook URL.
[**CreateWebhookFeedData**](WebhooksApi.md#CreateWebhookFeedData) | **Post** /webhooks/feed/:token | Send data to a feed via webhook URL.


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

