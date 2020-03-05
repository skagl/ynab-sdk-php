# # Category

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | 
**categoryGroupId** | **string** |  | 
**name** | **string** |  | 
**hidden** | **bool** | Whether or not the category is hidden | 
**originalCategoryGroupId** | **string** | If category is hidden this is the id of the category group it originally belonged to before it was hidden. | [optional] 
**note** | **string** |  | [optional] 
**budgeted** | **int** | Budgeted amount in milliunits format | 
**activity** | **int** | Activity amount in milliunits format | 
**balance** | **int** | Balance in milliunits format | 
**goalType** | **string** | The type of goal, if the category has a goal (TB&#x3D;Target Category Balance, TBD&#x3D;Target Category Balance by Date, MF&#x3D;Monthly Funding) | [optional] 
**goalCreationMonth** | [**\DateTime**](\DateTime.md) | The month a goal was created | [optional] 
**goalTarget** | **int** | The goal target amount in milliunits | [optional] 
**goalTargetMonth** | [**\DateTime**](\DateTime.md) | If the goal type is &#39;TBD&#39; (Target Category Balance by Date), this is the target month for the goal to be completed | [optional] 
**goalPercentageComplete** | **int** | The percentage completion of the goal | [optional] 
**deleted** | **bool** | Whether or not the category has been deleted.  Deleted categories will only be included in delta requests. | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


