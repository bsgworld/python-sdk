# GetMessages200ResponseMeta

Information about search criteria and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**GetMessages200ResponseMetaPage**](GetMessages200ResponseMetaPage.md) |  | [optional]  |

## Example

```python
from bsg_api.models.get_messages200_response_meta import GetMessages200ResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of GetMessages200ResponseMeta from a JSON string
get_messages200_response_meta_instance = GetMessages200ResponseMeta.from_json(json)
# print the JSON string representation of the object
print(GetMessages200ResponseMeta.to_json())

# convert the object into a dict
get_messages200_response_meta_dict = get_messages200_response_meta_instance.to_dict()
# create an instance of GetMessages200ResponseMeta from a dict
get_messages200_response_meta_from_dict = GetMessages200ResponseMeta.from_dict(get_messages200_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

