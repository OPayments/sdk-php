# OPayments\SDK\PaymentApi

Создание оплаты.

All URIs are relative to https://api.opayments.io/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSbpPayment()**](PaymentApi.md#createSbpPayment) | **POST** /payments/sbp | Создать платёж по СБП |
| [**createTpayPayment()**](PaymentApi.md#createTpayPayment) | **POST** /payments/tpay | Создать платёж через T-Pay |


## `createSbpPayment()`

```php
createSbpPayment($create_sbp_payment_request, $idempotency_key): \OPayments\SDK\Model\Payment
```

Создать платёж по СБП

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


$apiInstance = new OPayments\SDK\Api\PaymentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_sbp_payment_request = new \OPayments\SDK\Model\CreateSbpPaymentRequest(); // \OPayments\SDK\Model\CreateSbpPaymentRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createSbpPayment($create_sbp_payment_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentApi->createSbpPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_sbp_payment_request** | [**\OPayments\SDK\Model\CreateSbpPaymentRequest**](../Model/CreateSbpPaymentRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OPayments\SDK\Model\Payment**](../Model/Payment.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createTpayPayment()`

```php
createTpayPayment($create_tpay_payment_request, $idempotency_key): \OPayments\SDK\Model\Payment
```

Создать платёж через T-Pay

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


$apiInstance = new OPayments\SDK\Api\PaymentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_tpay_payment_request = new \OPayments\SDK\Model\CreateTpayPaymentRequest(); // \OPayments\SDK\Model\CreateTpayPaymentRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createTpayPayment($create_tpay_payment_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentApi->createTpayPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_tpay_payment_request** | [**\OPayments\SDK\Model\CreateTpayPaymentRequest**](../Model/CreateTpayPaymentRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OPayments\SDK\Model\Payment**](../Model/Payment.md)

### Authorization

[RequestSignature](../../README.md#RequestSignature), [ProjectIdentity](../../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
