# RcsMessage


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phone** | [**Phone**](Phone.md) |  |  |
| **sender** | **str** |  |  |
| **options** | [**Options**](Options.md) |  |  |
| **alternative_channel** | [**AlternativeChannel**](AlternativeChannel.md) |  | [optional]  |
| **callback_url** | **object** | Link to get the delivery status of messages. If this parameter is specified in the method, it will take precedence over the value specified in the “Callback URL” field in the Personal Area. | [optional]  |
| **tariff_code** | **int** |  | [optional]  |
| **validity_seconds** | **int** | Validity period in seconds. If not set, field \&quot;validity\&quot; is used | [optional]  |
| **validity** | **int** | Validity period in hours | [optional] [default to 72] |
| **add_to_contact_book** | **bool** |  | [optional] [default to True] |
| **check_stop_list** | **bool** |  | [optional] [default to True] |

## Example

```python
from bsg_api.models.rcs_message import RcsMessage

# TODO update the JSON string below
json = "{}"
# create an instance of RcsMessage from a JSON string
rcs_message_instance = RcsMessage.from_json(json)
# print the JSON string representation of the object
print(RcsMessage.to_json())

# convert the object into a dict
rcs_message_dict = rcs_message_instance.to_dict()
# create an instance of RcsMessage from a dict
rcs_message_from_dict = RcsMessage.from_dict(rcs_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

