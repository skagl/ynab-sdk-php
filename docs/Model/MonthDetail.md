# # MonthDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**month** | [**\DateTime**](\DateTime.md) |  | 
**note** | **string** |  | [optional] 
**income** | **int** | The total amount in transactions categorized to &#39;Inflow: To be Budgeted&#39; in the month | 
**budgeted** | **int** | The total amount budgeted in the month | 
**activity** | **int** | The total amount in transactions in the month, excluding those categorized to &#39;Inflow: To be Budgeted&#39; | 
**toBeBudgeted** | **int** | The available amount for &#39;To be Budgeted&#39; | 
**ageOfMoney** | **int** | The Age of Money as of the month | [optional] 
**deleted** | **bool** | Whether or not the month has been deleted.  Deleted months will only be included in delta requests. | 
**categories** | [**\YNAB\Model\Category[]**](Category.md) | The budget month categories.  Amounts (budgeted, activity, balance, etc.) are specific to the {month} parameter specified. | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


