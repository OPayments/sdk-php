# CreateRefundRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **int** | Сумма в копейках. | [optional]
**reason_code** | [**\OPayments\SDK\Model\RefundReason**](RefundReason.md) |  | [optional]
**reason_comment** | **string** |  | [optional]
**reason** | **string** | Устаревшее произвольное описание причины. Новые клиенты используют reasonCode и опционально reasonComment. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
