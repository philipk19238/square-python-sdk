## Card Payment Details

Reflects the current status of a card payment.

### Structure

`CardPaymentDetails`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | `string` | Optional | The card payment's current state. It can be one of: `AUTHORIZED`, `CAPTURED`, `VOIDED`,<br>`FAILED`. |
| `card` | [`Card`](/doc/models/card.md) | Optional | Represents the payment details of a card to be used for payments. These<br>details are determined by the `card_nonce` generated by `SqPaymentForm`. |
| `entry_method` | `string` | Optional | The method used to enter the card's details for the payment.  Can be<br>`KEYED`, `SWIPED`, `EMV`, `ON_FILE`, or `CONTACTLESS`. |
| `cvv_status` | `string` | Optional | Status code returned from the Card Verification Value (CVV) check. |
| `avs_status` | `string` | Optional | Status code returned from the Address Verification System (AVS) check. |
| `auth_result_code` | `string` | Optional | Status code returned by the card issuer that describes the payment's<br>authorization status. |
| `application_identifier` | `string` | Optional | For EMV payments, identifies the EMV application used for the payment |
| `application_name` | `string` | Optional | For EMV payments, the human-readable name of the EMV application used for the payment. |
| `application_cryptogram` | `string` | Optional | For EMV payments, the cryptogram generated for the payment. |
| `errors` | [`List of Error`](/doc/models/error.md) | Optional | Information on errors encountered during the request. |

### Example (as JSON)

```json
{
  "status": null,
  "card": null,
  "entry_method": null,
  "cvv_status": null,
  "avs_status": null,
  "auth_result_code": null,
  "application_identifier": null,
  "application_name": null,
  "application_cryptogram": null,
  "errors": null
}
```
