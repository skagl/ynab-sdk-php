# # BudgetDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | 
**name** | **string** |  | 
**lastModifiedOn** | [**\DateTime**](\DateTime.md) | The last time any changes were made to the budget from either a web or mobile client | [optional] 
**firstMonth** | [**\DateTime**](\DateTime.md) | The earliest budget month | [optional] 
**lastMonth** | [**\DateTime**](\DateTime.md) | The latest budget month | [optional] 
**dateFormat** | [**\YNAB\Model\DateFormat**](DateFormat.md) |  | [optional] 
**currencyFormat** | [**\YNAB\Model\CurrencyFormat**](CurrencyFormat.md) |  | [optional] 
**accounts** | [**\YNAB\Model\Account[]**](Account.md) |  | [optional] 
**payees** | [**\YNAB\Model\Payee[]**](Payee.md) |  | [optional] 
**payeeLocations** | [**\YNAB\Model\PayeeLocation[]**](PayeeLocation.md) |  | [optional] 
**categoryGroups** | [**\YNAB\Model\CategoryGroup[]**](CategoryGroup.md) |  | [optional] 
**categories** | [**\YNAB\Model\Category[]**](Category.md) |  | [optional] 
**months** | [**\YNAB\Model\MonthDetail[]**](MonthDetail.md) |  | [optional] 
**transactions** | [**\YNAB\Model\TransactionSummary[]**](TransactionSummary.md) |  | [optional] 
**subtransactions** | [**\YNAB\Model\SubTransaction[]**](SubTransaction.md) |  | [optional] 
**scheduledTransactions** | [**\YNAB\Model\ScheduledTransactionSummary[]**](ScheduledTransactionSummary.md) |  | [optional] 
**scheduledSubtransactions** | [**\YNAB\Model\ScheduledSubTransaction[]**](ScheduledSubTransaction.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


