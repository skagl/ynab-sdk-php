# YNAB\ScheduledTransactionsApi

All URIs are relative to *https://api.youneedabudget.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getScheduledTransactionById**](ScheduledTransactionsApi.md#getScheduledTransactionById) | **GET** /budgets/{budget_id}/scheduled_transactions/{scheduled_transaction_id} | Single scheduled transaction
[**getScheduledTransactions**](ScheduledTransactionsApi.md#getScheduledTransactions) | **GET** /budgets/{budget_id}/scheduled_transactions | List scheduled transactions



## getScheduledTransactionById

> \YNAB\Model\ScheduledTransactionResponse getScheduledTransactionById($budgetId, $scheduledTransactionId)

Single scheduled transaction

Returns a single scheduled transaction

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new YNAB\Api\ScheduledTransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = 'budgetId_example'; // string | The id of the budget (\"last-used\" can be used to specify the last used budget and \"default\" can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget)
$scheduledTransactionId = 'scheduledTransactionId_example'; // string | The id of the scheduled transaction

try {
    $result = $apiInstance->getScheduledTransactionById($budgetId, $scheduledTransactionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledTransactionsApi->getScheduledTransactionById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | **string**| The id of the budget (\&quot;last-used\&quot; can be used to specify the last used budget and \&quot;default\&quot; can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget) |
 **scheduledTransactionId** | **string**| The id of the scheduled transaction |

### Return type

[**\YNAB\Model\ScheduledTransactionResponse**](../Model/ScheduledTransactionResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getScheduledTransactions

> \YNAB\Model\ScheduledTransactionsResponse getScheduledTransactions($budgetId, $lastKnowledgeOfServer)

List scheduled transactions

Returns all scheduled transactions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new YNAB\Api\ScheduledTransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = 'budgetId_example'; // string | The id of the budget (\"last-used\" can be used to specify the last used budget and \"default\" can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget)
$lastKnowledgeOfServer = 56; // int | The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

try {
    $result = $apiInstance->getScheduledTransactions($budgetId, $lastKnowledgeOfServer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledTransactionsApi->getScheduledTransactions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | **string**| The id of the budget (\&quot;last-used\&quot; can be used to specify the last used budget and \&quot;default\&quot; can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget) |
 **lastKnowledgeOfServer** | **int**| The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included. | [optional]

### Return type

[**\YNAB\Model\ScheduledTransactionsResponse**](../Model/ScheduledTransactionsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

