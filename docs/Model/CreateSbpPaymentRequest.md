# CreateSbpPaymentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **string** | Идентификатор заказа в системе мерчанта. |
**amount** | **int** | Сумма в копейках. |
**currency** | **string** |  |
**description** | **string** |  | [optional]
**ip** | **string** | IP-адрес плательщика: IPv4 или IPv6. |
**callback_url** | **string** | HTTPS-адрес уведомлений. |
**success_url** | **string** | HTTPS-адрес для успешной оплаты. |
**failed_url** | **string** | HTTPS-адрес для отменённой оплаты. |
**device_data** | [**\OPayments\SDK\Model\DeviceData**](DeviceData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
