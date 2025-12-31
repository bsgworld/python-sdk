# ContactUpdate422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | It may be one of the following errors:  - **Phone number is already exist in contact book** - There are exists another contact with the same phone number, use that instead of change phone of this   - **Invalid contact id** - Pass correct contact id  - **Invalid phone number format** - Pass correct phone number  | [optional]  |
| **errors** | **List[object]** | errors | [optional]  |

## Example

```python
from bsg_api.models.contact_update422_response import ContactUpdate422Response

# TODO update the JSON string below
json = "{}"
# create an instance of ContactUpdate422Response from a JSON string
contact_update422_response_instance = ContactUpdate422Response.from_json(json)
# print the JSON string representation of the object
print(ContactUpdate422Response.to_json())

# convert the object into a dict
contact_update422_response_dict = contact_update422_response_instance.to_dict()
# create an instance of ContactUpdate422Response from a dict
contact_update422_response_from_dict = ContactUpdate422Response.from_dict(contact_update422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

