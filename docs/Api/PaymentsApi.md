# OPayments\SDK\PaymentsApi

Платежи проекта.

All URIs are relative to https://api.opayments.io/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getPayment()**](PaymentsApi.md#getPayment) | **GET** /payments/{paymentId} | Получить платёж |
| [**listPayments()**](PaymentsApi.md#listPayments) | **GET** /payments | Найти платежи |


## `getPayment()`

```php
getPayment($payment_id): \OPayments\SDK\Model\PaymentDetails
```

Получить платёж

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


$apiInstance = new OPayments\SDK\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = c9ee7c85-4cc0-494f-a0de-0af7257a66a6; // string

try {
    $result = $apiInstance->getPayment($payment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->getPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |

### Return type

[**\OPayments\SDK\Model\PaymentDetails**](../Model/PaymentDetails.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPayments()`

```php
listPayments($order_id, $status, $payment_method, $amount_from, $amount_to, $created_from, $created_to, $completed_from, $completed_to, $failure_code, $search, $sort, $sort_direction, $cursor, $limit): \OPayments\SDK\Model\PaymentList
```

Найти платежи

Возвращает список платежей проекта.

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


$apiInstance = new OPayments\SDK\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | Идентификатор заказа в системе мерчанта.
$status = array('status_example'); // string[]
$payment_method = 'payment_method_example'; // string
$amount_from = 56; // int | Не больше amountTo, если он передан.
$amount_to = 56; // int | Не меньше amountFrom, если он передан.
$created_from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Не позже createdTo, если он передан.
$created_to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Не раньше createdFrom, если он передан.
$completed_from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Не позже completedTo, если он передан.
$completed_to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Не раньше completedFrom, если он передан.
$failure_code = 'failure_code_example'; // string | Нормализованный код причины платежа.
$search = 'search_example'; // string | Поиск по paymentId, orderId и описанию платежа.
$sort = 'createdAt'; // string
$sort_direction = 'desc'; // string
$cursor = 'cursor_example'; // string | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID.
$limit = 20; // int | Количество записей в ответе.

try {
    $result = $apiInstance->listPayments($order_id, $status, $payment_method, $amount_from, $amount_to, $created_from, $created_to, $completed_from, $completed_to, $failure_code, $search, $sort, $sort_direction, $cursor, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->listPayments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **string**| Идентификатор заказа в системе мерчанта. | [optional] |
| **status** | [**string[]**](../Model/string.md)|  | [optional] |
| **payment_method** | **string**|  | [optional] |
| **amount_from** | **int**| Не больше amountTo, если он передан. | [optional] |
| **amount_to** | **int**| Не меньше amountFrom, если он передан. | [optional] |
| **created_from** | **\DateTime**| Не позже createdTo, если он передан. | [optional] |
| **created_to** | **\DateTime**| Не раньше createdFrom, если он передан. | [optional] |
| **completed_from** | **\DateTime**| Не позже completedTo, если он передан. | [optional] |
| **completed_to** | **\DateTime**| Не раньше completedFrom, если он передан. | [optional] |
| **failure_code** | **string**| Нормализованный код причины платежа. | [optional] |
| **search** | **string**| Поиск по paymentId, orderId и описанию платежа. | [optional] |
| **sort** | **string**|  | [optional] [default to &#39;createdAt&#39;] |
| **sort_direction** | **string**|  | [optional] [default to &#39;desc&#39;] |
| **cursor** | **string**| Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID. | [optional] |
| **limit** | **int**| Количество записей в ответе. | [optional] [default to 20] |

### Return type

[**\OPayments\SDK\Model\PaymentList**](../Model/PaymentList.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
