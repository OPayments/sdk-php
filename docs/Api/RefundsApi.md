# OPayments\SDK\RefundsApi

Возвраты.

All URIs are relative to https://api.opayments.io/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPaymentRefund()**](RefundsApi.md#createPaymentRefund) | **POST** /payments/{paymentId}/refunds | Создать возврат |
| [**getRefund()**](RefundsApi.md#getRefund) | **GET** /refunds/{refundId} | Получить возврат |
| [**listPaymentRefunds()**](RefundsApi.md#listPaymentRefunds) | **GET** /payments/{paymentId}/refunds | Найти возвраты платежа |
| [**listRefunds()**](RefundsApi.md#listRefunds) | **GET** /refunds | Найти возвраты проекта |


## `createPaymentRefund()`

```php
createPaymentRefund($payment_id, $create_refund_request, $idempotency_key): \OPayments\SDK\Model\Refund
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
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createPaymentRefund($payment_id, $create_refund_request, $idempotency_key);
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
| **idempotency_key** | **string**|  | [optional] |

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

## `getRefund()`

```php
getRefund($refund_id): \OPayments\SDK\Model\Refund
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
$refund_id = 'refund_id_example'; // string

try {
    $result = $apiInstance->getRefund($refund_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->getRefund: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **refund_id** | **string**|  | |

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

## `listPaymentRefunds()`

```php
listPaymentRefunds($payment_id, $status, $reason_code, $cursor, $limit): \OPayments\SDK\Model\RefundPage
```

Найти возвраты платежа

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
$status = 'status_example'; // string
$reason_code = new \OPayments\SDK\Model\\OPayments\SDK\Model\RefundReason(); // \OPayments\SDK\Model\RefundReason
$cursor = 'cursor_example'; // string | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID.
$limit = 20; // int | Количество записей в ответе.

try {
    $result = $apiInstance->listPaymentRefunds($payment_id, $status, $reason_code, $cursor, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->listPaymentRefunds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |
| **status** | **string**|  | [optional] |
| **reason_code** | [**\OPayments\SDK\Model\RefundReason**](../Model/.md)|  | [optional] |
| **cursor** | **string**| Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID. | [optional] |
| **limit** | **int**| Количество записей в ответе. | [optional] [default to 20] |

### Return type

[**\OPayments\SDK\Model\RefundPage**](../Model/RefundPage.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listRefunds()`

```php
listRefunds($status, $payment_method, $payment_id, $reason_code, $created_from, $created_to, $cursor, $limit): \OPayments\SDK\Model\RefundPage
```

Найти возвраты проекта

Возвращает возвраты по всем платежам текущего проекта. Сортировка всегда `createdAt DESC, refundId DESC`; курсор нельзя использовать с другими фильтрами.

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
$status = 'status_example'; // string
$payment_method = 'payment_method_example'; // string
$payment_id = 'payment_id_example'; // string | Идентификатор исходного платежа.
$reason_code = new \OPayments\SDK\Model\\OPayments\SDK\Model\RefundReason(); // \OPayments\SDK\Model\RefundReason
$created_from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Не позже createdTo, если он передан.
$created_to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Не раньше createdFrom, если он передан.
$cursor = 'cursor_example'; // string | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID.
$limit = 20; // int | Количество записей в ответе.

try {
    $result = $apiInstance->listRefunds($status, $payment_method, $payment_id, $reason_code, $created_from, $created_to, $cursor, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->listRefunds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**|  | [optional] |
| **payment_method** | **string**|  | [optional] |
| **payment_id** | **string**| Идентификатор исходного платежа. | [optional] |
| **reason_code** | [**\OPayments\SDK\Model\RefundReason**](../Model/.md)|  | [optional] |
| **created_from** | **\DateTime**| Не позже createdTo, если он передан. | [optional] |
| **created_to** | **\DateTime**| Не раньше createdFrom, если он передан. | [optional] |
| **cursor** | **string**| Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID. | [optional] |
| **limit** | **int**| Количество записей в ответе. | [optional] [default to 20] |

### Return type

[**\OPayments\SDK\Model\RefundPage**](../Model/RefundPage.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
