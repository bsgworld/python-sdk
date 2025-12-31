# SenderRequestNaturalRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **str** | Country code according to ISO 3166-1 alpha-2 standard |  |
| **type** | [**SenderRequestType**](SenderRequestType.md) |  | [default to SenderRequestType.SMS] |
| **sender** | **str** | Sender name.   Up to 11 Latin letters or digits, up to 15 – only digits. To setup senders visit the [account](https://app.bsg.world/sms/senders) or use [sender api](#tag/Senders) |  |
| **name** | **str** | Last name, first name, and middle name |  |
| **code_of_company** | **str** | National registration code of Company (ЄДРПОУ for Ukraine) |  |
| **description** | **str** | Service description |  |
| **informing_purpose** | **str** | Purpose of informing |  |
| **site_url** | **str** | Website URL of your service | [optional]  |
| **comment** | **str** | any additional information | [optional]  |

## Example

```python
from bsg_api.models.sender_request_natural_request import SenderRequestNaturalRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SenderRequestNaturalRequest from a JSON string
sender_request_natural_request_instance = SenderRequestNaturalRequest.from_json(json)
# print the JSON string representation of the object
print(SenderRequestNaturalRequest.to_json())

# convert the object into a dict
sender_request_natural_request_dict = sender_request_natural_request_instance.to_dict()
# create an instance of SenderRequestNaturalRequest from a dict
sender_request_natural_request_from_dict = SenderRequestNaturalRequest.from_dict(sender_request_natural_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

