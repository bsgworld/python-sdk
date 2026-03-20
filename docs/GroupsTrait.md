# GroupsTrait


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **groups** | **List[int]** | An array of lists (list id) with contacts from the address book to which RCS campaigns are to be sent. id of the lists can be obtained: using the Get [lists API](#tag/Contact-List) in your account [Contact Book → Lists](https://app.bsg.world/addressbook/lists) |  |

## Example

```python
from bsg_api.models.groups_trait import GroupsTrait

# TODO update the JSON string below
json = "{}"
# create an instance of GroupsTrait from a JSON string
groups_trait_instance = GroupsTrait.from_json(json)
# print the JSON string representation of the object
print(GroupsTrait.to_json())

# convert the object into a dict
groups_trait_dict = groups_trait_instance.to_dict()
# create an instance of GroupsTrait from a dict
groups_trait_from_dict = GroupsTrait.from_dict(groups_trait_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

