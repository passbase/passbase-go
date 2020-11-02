# {{classname}}

All URIs are relative to *https://api.passbase.com/verification/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetIdentityById**](IdentityApi.md#GetIdentityById) | **Get** /identities/{id} | Get identity
[**GetIdentityResourceById**](IdentityApi.md#GetIdentityResourceById) | **Get** /identity/{id}/resources/{resource_id} | Get resource
[**ListIdentities**](IdentityApi.md#ListIdentities) | **Get** /identities | List identities
[**ListIdentityResources**](IdentityApi.md#ListIdentityResources) | **Get** /identity/{id}/resources | List resources

# **GetIdentityById**
> Identity GetIdentityById(ctx, id)
Get identity

Retrieve an identity by providing the identity ID.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **id** | [**string**](.md)| Unique ID of the identity to return | 

### Return type

[**Identity**](Identity.md)

### Authorization

[SecretApiKey](../README.md#SecretApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetIdentityResourceById**
> Resource GetIdentityResourceById(ctx, id, resourceId)
Get resource

Get a resource attached to an identity by providing the resource ID. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **id** | **string**| Identity id | 
  **resourceId** | **string**| Resource id | 

### Return type

[**Resource**](Resource.md)

### Authorization

[SecretApiKey](../README.md#SecretApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ListIdentities**
> PaginatedIdentities ListIdentities(ctx, optional)
List identities

List all the identities retrievable by the provided API Secret Key.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***IdentityApiListIdentitiesOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a IdentityApiListIdentitiesOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **optional.Int32**|  | 
 **cursor** | **optional.String**|  | 

### Return type

[**PaginatedIdentities**](PaginatedIdentities.md)

### Authorization

[SecretApiKey](../README.md#SecretApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ListIdentityResources**
> PaginatedResources ListIdentityResources(ctx, id, optional)
List resources

List resources attached to an identity by providing the identity ID.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **id** | **string**| Identity id | 
 **optional** | ***IdentityApiListIdentityResourcesOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a IdentityApiListIdentityResourcesOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **limit** | **optional.Int32**|  | 
 **cursor** | **optional.String**|  | 

### Return type

[**PaginatedResources**](PaginatedResources.md)

### Authorization

[SecretApiKey](../README.md#SecretApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

