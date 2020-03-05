# # SaveTransactionsResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transactionIds** | **string[]** | The transaction ids that were saved | 
**transaction** | [**\YNAB\Model\TransactionDetail**](TransactionDetail.md) |  | [optional] 
**transactions** | [**\YNAB\Model\TransactionDetail[]**](TransactionDetail.md) | If multiple transactions were specified, the transactions that were saved | [optional] 
**duplicateImportIds** | **string[]** | If multiple transactions were specified, a list of import_ids that were not created because of an existing import_id found on the same account | [optional] 
**serverKnowledge** | **int** | The knowledge of the server | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


