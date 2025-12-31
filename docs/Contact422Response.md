# Contact422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | Invalid contact id | [optional]  |
| **errors** | **List[object]** | errors | [optional]  |

## Example

```python
from bsg_api.models.contact422_response import Contact422Response

# TODO update the JSON string below
json = "{}"
# create an instance of Contact422Response from a JSON string
contact422_response_instance = Contact422Response.from_json(json)
# print the JSON string representation of the object
print(Contact422Response.to_json())

# convert the object into a dict
contact422_response_dict = contact422_response_instance.to_dict()
# create an instance of Contact422Response from a dict
contact422_response_from_dict = Contact422Response.from_dict(contact422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

