# OPayments\SDK\BalanceApi

Баланс.

All URIs are relative to https://api.opayments.io/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getBalance()**](BalanceApi.md#getBalance) | **GET** /balance | Получить баланс |


## `getBalance()`

```php
getBalance(): \OPayments\SDK\Model\Balance
```

Получить баланс

Возвращает текущий баланс проекта.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: RequestSignature
$config = OPayments\SDK\Configuration::getDefaultConfiguration()->setApiKey('X-Signature', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OPayments\SDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Signature', 'Bearer');

// Configure API key authorization: ProjectIdentity
$config = OPayments\SDK\Configuration::getDefaultConfiguration()->setApiKey('X-Identity', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OPayments\SDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Identity', 'Bearer');


$apiInstance = new OPayments\SDK\Api\BalanceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getBalance();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BalanceApi->getBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OPayments\SDK\Model\Balance**](../Model/Balance.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
