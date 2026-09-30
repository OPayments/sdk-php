# CreateSbpPaymentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **string** | Идентификатор заказа в системе мерчанта. |
**amount** | **int** | Сумма в копейках. |
**description** | **string** |  | [optional]
**metadata** | [**\OPayments\SDK\Model\PaymentMetadata**](PaymentMetadata.md) |  |
**callback_url** | **string** | HTTPS-адрес для уведомлений о платеже. |
**success_url** | **string** | HTTPS-адрес для успешной оплаты. |
**failed_url** | **string** | HTTPS-адрес для отменённой оплаты. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
