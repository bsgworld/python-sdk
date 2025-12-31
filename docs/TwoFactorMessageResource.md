# TwoFactorMessageResource


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | The unique ID of the message | [optional]  |
| **recipient** | **str** | Number of the recipient of the message with a one-time code | [optional]  |
| **status** | [**OtpMessageStatus**](OtpMessageStatus.md) |  | [optional]  |
| **channel** | [**OtpChannel**](OtpChannel.md) |  | [optional]  |
| **sender** | **str** | Sender name | [optional]  |
| **price** | **float** | Message cost | [optional]  |
| **currency** | **str** | The three-letter code of the currency in which the value is indicated. Corresponds to the user’s account currency | [optional]  |
| **sent_at** | **str** | The date and time of the message were sent in ISO 8601 format | [optional]  |
| **created_at** | **str** | The date and time the message was created in ISO 8601 format | [optional]  |

## Example

```python
from bsg_api.models.two_factor_message_resource import TwoFactorMessageResource

# TODO update the JSON string below
json = "{}"
# create an instance of TwoFactorMessageResource from a JSON string
two_factor_message_resource_instance = TwoFactorMessageResource.from_json(json)
# print the JSON string representation of the object
print(TwoFactorMessageResource.to_json())

# convert the object into a dict
two_factor_message_resource_dict = two_factor_message_resource_instance.to_dict()
# create an instance of TwoFactorMessageResource from a dict
two_factor_message_resource_from_dict = TwoFactorMessageResource.from_dict(two_factor_message_resource_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

