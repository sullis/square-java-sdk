## Payment Refund

Represents a refund of a payment made using Square. Contains information on
the original payment and the amount of money refunded.

### Structure

`PaymentRefund`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `String` |  | Unique ID for this refund, generated by Square. |
| `Status` | `String` | Optional | The refund's status:<br>- `PENDING` - awaiting approval<br>- `COMPLETED` - successfully completed<br>- `REJECTED` - the refund was rejected<br>- `FAILED` - an error occurred |
| `LocationId` | `String` | Optional | Location ID associated with the payment this refund is attached to. |
| `AmountMoney` | [`Money`](/doc/models/money.md) |  | Represents an amount of money. `Money` fields can be signed or unsigned.<br>Fields that do not explicitly define whether they are signed or unsigned are<br>considered unsigned and can only hold positive amounts. For signed fields, the<br>sign of the value indicates the purpose of the money transfer. See<br>[Working with Monetary Amounts](https://developer.squareup.com/docs/build-basics/working-with-monetary-amounts)<br>for more information. |
| `AppFeeMoney` | [`Money`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned.<br>Fields that do not explicitly define whether they are signed or unsigned are<br>considered unsigned and can only hold positive amounts. For signed fields, the<br>sign of the value indicates the purpose of the money transfer. See<br>[Working with Monetary Amounts](https://developer.squareup.com/docs/build-basics/working-with-monetary-amounts)<br>for more information. |
| `ProcessingFee` | [`List<ProcessingFee>`](/doc/models/processing-fee.md) | Optional | Processing fees and fee adjustments assessed by Square on this refund. |
| `PaymentId` | `String` | Optional | The ID of the payment assocated with this refund. |
| `OrderId` | `String` | Optional | The ID of the order associated with the refund. |
| `Reason` | `String` | Optional | The reason for the refund. |
| `CreatedAt` | `String` | Optional | Timestamp of when the refund was created, in RFC 3339 format. |
| `UpdatedAt` | `String` | Optional | Timestamp of when the refund was last updated, in RFC 3339 format. |

### Example (as JSON)

```json
{
  "id": "id0",
  "status": null,
  "location_id": null,
  "amount_money": {
    "amount": null,
    "currency": null
  },
  "app_fee_money": null,
  "processing_fee": null,
  "payment_id": null,
  "order_id": null,
  "reason": null,
  "created_at": null,
  "updated_at": null
}
```

