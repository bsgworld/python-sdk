# ContactListUpdate422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | It may be one of the following errors:  - **Contact group is not found** - There is not contact list with this id, use correct contact list id - **Contact group is already exists** - There are exists another contact list with the same **name**, use different name for new list    | [optional]  |
| **errors** | **List[object]** | errors | [optional]  |

## Example

```python
from bsg_api.models.contact_list_update422_response import ContactListUpdate422Response

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListUpdate422Response from a JSON string
contact_list_update422_response_instance = ContactListUpdate422Response.from_json(json)
# print the JSON string representation of the object
print(ContactListUpdate422Response.to_json())

# convert the object into a dict
contact_list_update422_response_dict = contact_list_update422_response_instance.to_dict()
# create an instance of ContactListUpdate422Response from a dict
contact_list_update422_response_from_dict = ContactListUpdate422Response.from_dict(contact_list_update422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

