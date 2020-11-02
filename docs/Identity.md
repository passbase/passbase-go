# Identity

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique ID of the identity | [optional] [default to null]
**Status** | **string** | Current state of the identity in Passbase&#x27;s systems | [optional] [default to null]
**Owner** | [***IdentityOwner**](IdentityOwner.md) |  | [optional] [default to null]
**Score** | **float64** | Float between 0 and 1 representing our confidence that this identity is valid. 0 meaning we couldn&#x27;t verify any of the information provided with accuracy, and 1 absolute confidence. | [optional] [default to null]
**Created** | **int64** | Unix-timestamp of when the identity was created | [optional] [default to null]
**Updated** | **int64** | Unix-timestamp of when the identity was updated | [optional] [default to null]
**Resources** | [**[]IdentityResource**](IdentityResource.md) | resources attached to a verification | [optional] [default to null]
**Watchlist** | [***WatchlistResponse**](WatchlistResponse.md) |  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

