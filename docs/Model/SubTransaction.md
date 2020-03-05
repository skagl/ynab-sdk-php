# # SubTransaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | 
**transactionId** | **string** |  | 
**amount** | **int** | The subtransaction amount in milliunits format | 
**memo** | **string** |  | [optional] 
**payeeId** | **string** |  | [optional] 
**categoryId** | **string** |  | [optional] 
**transferAccountId** | **string** | If a transfer, the account_id which the subtransaction transfers to | [optional] 
**deleted** | **bool** | Whether or not the subtransaction has been deleted.  Deleted subtransactions will only be included in delta requests. | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


