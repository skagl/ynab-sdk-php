# # SaveSubTransaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **int** | The sub-transaction amount in milliunits format. | 
**payeeId** | **string** | The payee for the sub-transaction.  Transfer payees are not allowed. | [optional] 
**payeeName** | **string** | The payee name.  If a payee_name value is provided and payee_id has a null value, the payee_name value will be used to resolve the payee by either (1) a matching payee rename rule (only if import_id is also specified on parent transaction) or (2) a payee with the same name or (3) creation of a new payee. | [optional] 
**categoryId** | **string** | The category for the sub-transaction.  Credit Card Payment categories are not permitted and will be ignored if supplied. | [optional] 
**memo** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


