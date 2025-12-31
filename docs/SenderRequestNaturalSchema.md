# SenderRequestNaturalSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Number of the application for Sender registration | [optional]  |
| **name** | **str** | Last name, first name, and middle name | [optional]  |
| **status** | [**SenderRequestStatus**](SenderRequestStatus.md) |  | [optional]  |
| **type** | [**SenderRequestType**](SenderRequestType.md) |  | [optional] [default to SenderRequestType.SMS] |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **country_code** | **str** | Country code according to ISO 3166-1 alpha-2 standard | [optional]  |
| **sender** | **str** | Sender name.   Up to 11 Latin letters or digits, up to 15 – only digits. To setup senders visit the [account](https://app.bsg.world/sms/senders) or use [sender api](#tag/Senders) | [optional]  |
| **code_of_company** | **str** | National registration code of Company (ЄДРПОУ for Ukraine) | [optional]  |
| **site_url** | **str** | Website URL of your service | [optional]  |
| **informing_purpose** | **str** | Purpose of informing | [optional]  |
| **comment** | **str** | any additional information | [optional]  |
| **description** | **str** | Service description | [optional]  |

## Example

```python
from bsg_api.models.sender_request_natural_schema import SenderRequestNaturalSchema

# TODO update the JSON string below
json = "{}"
# create an instance of SenderRequestNaturalSchema from a JSON string
sender_request_natural_schema_instance = SenderRequestNaturalSchema.from_json(json)
# print the JSON string representation of the object
print(SenderRequestNaturalSchema.to_json())

# convert the object into a dict
sender_request_natural_schema_dict = sender_request_natural_schema_instance.to_dict()
# create an instance of SenderRequestNaturalSchema from a dict
sender_request_natural_schema_from_dict = SenderRequestNaturalSchema.from_dict(sender_request_natural_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

