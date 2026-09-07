# OPayments\SDK\RefundsApi

Возвраты.

All URIs are relative to https://api.opayments.io/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPaymentRefund()**](RefundsApi.md#createPaymentRefund) | **POST** /payments/{paymentId}/refund | Создать возврат |
| [**getPaymentRefund()**](RefundsApi.md#getPaymentRefund) | **GET** /payments/{paymentId}/refund | Получить возврат |


## `createPaymentRefund()`

```php
createPaymentRefund($payment_id, $create_refund_request): \OPayments\SDK\Model\Refund
```

Создать возврат

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


$apiInstance = new OPayments\SDK\Api\RefundsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = c9ee7c85-4cc0-494f-a0de-0af7257a66a6; // string
$create_refund_request = new \OPayments\SDK\Model\CreateRefundRequest(); // \OPayments\SDK\Model\CreateRefundRequest

try {
    $result = $apiInstance->createPaymentRefund($payment_id, $create_refund_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->createPaymentRefund: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |
| **create_refund_request** | [**\OPayments\SDK\Model\CreateRefundRequest**](../Model/CreateRefundRequest.md)|  | |

### Return type

[**\OPayments\SDK\Model\Refund**](../Model/Refund.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaymentRefund()`

```php
getPaymentRefund($payment_id): \OPayments\SDK\Model\Refund
```

Получить возврат

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


$apiInstance = new OPayments\SDK\Api\RefundsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = c9ee7c85-4cc0-494f-a0de-0af7257a66a6; // string

try {
    $result = $apiInstance->getPaymentRefund($payment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->getPaymentRefund: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |

### Return type

[**\OPayments\SDK\Model\Refund**](../Model/Refund.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
