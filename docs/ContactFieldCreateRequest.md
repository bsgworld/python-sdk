# ContactFieldCreateRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | The name of the custom field for the contacts |  |
| **description** | **str** | Description of the custom contact field | [optional]  |
| **is_visible** | **bool** | Whether the field is displayed: true or false value | [optional] [default to True] |
| **type** | [**ContactFieldType**](ContactFieldType.md) |  |  |

## Example

```python
from bsg_api.models.contact_field_create_request import ContactFieldCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ContactFieldCreateRequest from a JSON string
contact_field_create_request_instance = ContactFieldCreateRequest.from_json(json)
# print the JSON string representation of the object
print(ContactFieldCreateRequest.to_json())

# convert the object into a dict
contact_field_create_request_dict = contact_field_create_request_instance.to_dict()
# create an instance of ContactFieldCreateRequest from a dict
contact_field_create_request_from_dict = ContactFieldCreateRequest.from_dict(contact_field_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

