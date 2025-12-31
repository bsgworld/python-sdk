# WhatsappSingle200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**MessageInfo**](MessageInfo.md) |  | [optional]  |

## Example

```python
from bsg_api.models.whatsapp_single200_response import WhatsappSingle200Response

# TODO update the JSON string below
json = "{}"
# create an instance of WhatsappSingle200Response from a JSON string
whatsapp_single200_response_instance = WhatsappSingle200Response.from_json(json)
# print the JSON string representation of the object
print(WhatsappSingle200Response.to_json())

# convert the object into a dict
whatsapp_single200_response_dict = whatsapp_single200_response_instance.to_dict()
# create an instance of WhatsappSingle200Response from a dict
whatsapp_single200_response_from_dict = WhatsappSingle200Response.from_dict(whatsapp_single200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

