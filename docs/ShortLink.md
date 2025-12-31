# ShortLink


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **link** | **str** | Target url |  |
| **placeholder** | **str** | Word in message text that need to be replaced by generated short link |  |
| **domain_ids** | **List[str]** | List of short domain identifiers to use for generate short links to follow at target url |  |
| **change_domain_after** | **int** | Change domain each X messages | [optional]  |
| **protocol** | **bool** | Add (https) protocol to short link or not | [optional] [default to True] |

## Example

```python
from bsg_api.models.short_link import ShortLink

# TODO update the JSON string below
json = "{}"
# create an instance of ShortLink from a JSON string
short_link_instance = ShortLink.from_json(json)
# print the JSON string representation of the object
print(ShortLink.to_json())

# convert the object into a dict
short_link_dict = short_link_instance.to_dict()
# create an instance of ShortLink from a dict
short_link_from_dict = ShortLink.from_dict(short_link_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

