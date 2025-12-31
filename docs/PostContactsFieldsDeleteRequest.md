# PostContactsFieldsDeleteRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ids** | **List[int]** | List of contact field ids |  |

## Example

```python
from bsg_api.models.post_contacts_fields_delete_request import PostContactsFieldsDeleteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PostContactsFieldsDeleteRequest from a JSON string
post_contacts_fields_delete_request_instance = PostContactsFieldsDeleteRequest.from_json(json)
# print the JSON string representation of the object
print(PostContactsFieldsDeleteRequest.to_json())

# convert the object into a dict
post_contacts_fields_delete_request_dict = post_contacts_fields_delete_request_instance.to_dict()
# create an instance of PostContactsFieldsDeleteRequest from a dict
post_contacts_fields_delete_request_from_dict = PostContactsFieldsDeleteRequest.from_dict(post_contacts_fields_delete_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

