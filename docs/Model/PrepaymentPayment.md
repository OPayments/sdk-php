# PrepaymentPayment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_id** | **string** |  |
**order_id** | **string** |  |
**amount** | **int** | Сумма в копейках. |
**currency** | **string** |  |
**description** | **string** |  | [optional]
**payment_method** | **string** |  |
**status** | **string** |  |
**payment_url** | **string** | Адрес оплаты для платежа в статусе pending. | [optional]
**failure_code** | **string** |  | [optional]
**failure_message** | **string** | Нормализованное сообщение, безопасное для показа мерчанту; никогда не содержит сырой ответ провайдера, credentials или данные карты. | [optional]
**refund_summary** | [**\OPayments\SDK\Model\RefundSummary**](RefundSummary.md) |  | [optional]
**completed_at** | **\DateTime** |  | [optional]
**created_at** | **\DateTime** |  |
**updated_at** | **\DateTime** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
