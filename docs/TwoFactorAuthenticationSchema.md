# TwoFactorAuthenticationSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | The ID of the generated authentication | [optional]  |
| **recipient** | **str** | Number of the recipient of the message with a one-time code | [optional]  |
| **status** | [**OtpStatus**](OtpStatus.md) |  | [optional]  |
| **channel** | [**OtpChannel**](OtpChannel.md) |  | [optional]  |
| **sender** | **str** | Sender name | [optional]  |
| **sender_alt** | **str** | SMS sender name | [optional]  |
| **message_text** | **str** | Message text. | [optional]  |
| **code_lifetime** | **int** | OTP expiration date | [optional]  |
| **code_max_tries** | **int** | The number of OTP check attempts | [optional]  |
| **code_digits** | **int** | The number of digits in the OTP | [optional]  |
| **price** | **float** | Authentication cost. At the time of creating the authentication, 0 is indicated | [optional]  |
| **currency** | **str** | The three-letter code of the currency in which the value is indicated. Corresponds to the user’s account currency | [optional]  |
| **country_code** | **str** | The country code of the recipient of the one-time password according to the ISO 3166-1 alpha-2 standard | [optional]  |
| **expired_at** | **datetime** | Date and time when the authentication expires in ISO 8601 format | [optional]  |
| **created_at** | **datetime** | The date and time of the authentication session were created in ISO 8601 format | [optional]  |
| **finished_at** | **datetime** | Date and time when the authentication session was closed. At the time of creating the authentication, the value “null” is indicated | [optional]  |

## Example

```python
from bsg_api.models.two_factor_authentication_schema import TwoFactorAuthenticationSchema

# TODO update the JSON string below
json = "{}"
# create an instance of TwoFactorAuthenticationSchema from a JSON string
two_factor_authentication_schema_instance = TwoFactorAuthenticationSchema.from_json(json)
# print the JSON string representation of the object
print(TwoFactorAuthenticationSchema.to_json())

# convert the object into a dict
two_factor_authentication_schema_dict = two_factor_authentication_schema_instance.to_dict()
# create an instance of TwoFactorAuthenticationSchema from a dict
two_factor_authentication_schema_from_dict = TwoFactorAuthenticationSchema.from_dict(two_factor_authentication_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

