# YNAB\CategoriesApi

All URIs are relative to *https://api.youneedabudget.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCategories**](CategoriesApi.md#getCategories) | **GET** /budgets/{budget_id}/categories | List categories
[**getCategoryById**](CategoriesApi.md#getCategoryById) | **GET** /budgets/{budget_id}/categories/{category_id} | Single category
[**getMonthCategoryById**](CategoriesApi.md#getMonthCategoryById) | **GET** /budgets/{budget_id}/months/{month}/categories/{category_id} | Single category for a specific budget month
[**updateMonthCategory**](CategoriesApi.md#updateMonthCategory) | **PATCH** /budgets/{budget_id}/months/{month}/categories/{category_id} | Update a category for a specific month



## getCategories

> \YNAB\Model\CategoriesResponse getCategories($budgetId, $lastKnowledgeOfServer)

List categories

Returns all categories grouped by category group.  Amounts (budgeted, activity, balance, etc.) are specific to the current budget month (UTC).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new YNAB\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = 'budgetId_example'; // string | The id of the budget (\"last-used\" can be used to specify the last used budget and \"default\" can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget)
$lastKnowledgeOfServer = 56; // int | The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

try {
    $result = $apiInstance->getCategories($budgetId, $lastKnowledgeOfServer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->getCategories: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | **string**| The id of the budget (\&quot;last-used\&quot; can be used to specify the last used budget and \&quot;default\&quot; can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget) |
 **lastKnowledgeOfServer** | **int**| The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included. | [optional]

### Return type

[**\YNAB\Model\CategoriesResponse**](../Model/CategoriesResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getCategoryById

> \YNAB\Model\CategoryResponse getCategoryById($budgetId, $categoryId)

Single category

Returns a single category.  Amounts (budgeted, activity, balance, etc.) are specific to the current budget month (UTC).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new YNAB\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = 'budgetId_example'; // string | The id of the budget (\"last-used\" can be used to specify the last used budget and \"default\" can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget)
$categoryId = 'categoryId_example'; // string | The id of the category

try {
    $result = $apiInstance->getCategoryById($budgetId, $categoryId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->getCategoryById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | **string**| The id of the budget (\&quot;last-used\&quot; can be used to specify the last used budget and \&quot;default\&quot; can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget) |
 **categoryId** | **string**| The id of the category |

### Return type

[**\YNAB\Model\CategoryResponse**](../Model/CategoryResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getMonthCategoryById

> \YNAB\Model\CategoryResponse getMonthCategoryById($budgetId, $month, $categoryId)

Single category for a specific budget month

Returns a single category for a specific budget month.  Amounts (budgeted, activity, balance, etc.) are specific to the current budget month (UTC).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new YNAB\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = 'budgetId_example'; // string | The id of the budget (\"last-used\" can be used to specify the last used budget and \"default\" can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget)
$month = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | The budget month in ISO format (e.g. 2016-12-01) (\"current\" can also be used to specify the current calendar month (UTC))
$categoryId = 'categoryId_example'; // string | The id of the category

try {
    $result = $apiInstance->getMonthCategoryById($budgetId, $month, $categoryId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->getMonthCategoryById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | **string**| The id of the budget (\&quot;last-used\&quot; can be used to specify the last used budget and \&quot;default\&quot; can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget) |
 **month** | **\DateTime**| The budget month in ISO format (e.g. 2016-12-01) (\&quot;current\&quot; can also be used to specify the current calendar month (UTC)) |
 **categoryId** | **string**| The id of the category |

### Return type

[**\YNAB\Model\CategoryResponse**](../Model/CategoryResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## updateMonthCategory

> \YNAB\Model\SaveCategoryResponse updateMonthCategory($budgetId, $month, $categoryId, $data)

Update a category for a specific month

Update a category for a specific month

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new YNAB\Api\CategoriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = 'budgetId_example'; // string | The id of the budget (\"last-used\" can be used to specify the last used budget and \"default\" can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget)
$month = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | The budget month in ISO format (e.g. 2016-12-01) (\"current\" can also be used to specify the current calendar month (UTC))
$categoryId = 'categoryId_example'; // string | The id of the category
$data = new \YNAB\Model\SaveMonthCategoryWrapper(); // \YNAB\Model\SaveMonthCategoryWrapper | The category to update

try {
    $result = $apiInstance->updateMonthCategory($budgetId, $month, $categoryId, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoriesApi->updateMonthCategory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | **string**| The id of the budget (\&quot;last-used\&quot; can be used to specify the last used budget and \&quot;default\&quot; can be used if default budget selection is enabled (see: https://api.youneedabudget.com/#oauth-default-budget) |
 **month** | **\DateTime**| The budget month in ISO format (e.g. 2016-12-01) (\&quot;current\&quot; can also be used to specify the current calendar month (UTC)) |
 **categoryId** | **string**| The id of the category |
 **data** | [**\YNAB\Model\SaveMonthCategoryWrapper**](../Model/SaveMonthCategoryWrapper.md)| The category to update |

### Return type

[**\YNAB\Model\SaveCategoryResponse**](../Model/SaveCategoryResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

