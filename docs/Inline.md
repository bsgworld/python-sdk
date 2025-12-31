# Inline


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | A variable representing the name or identifier of the inline attachment |  |
| **cid** | **str** | The content identifier (links the inline attachment to the email body) |  |
| **content_type** | **str** | MIME content type | [optional]  |
| **content** | **str** | The base64-encoded content of the inline attachment |  |

## Example

```python
from bsg_api.models.inline import Inline

# TODO update the JSON string below
json = "{}"
# create an instance of Inline from a JSON string
inline_instance = Inline.from_json(json)
# print the JSON string representation of the object
print(Inline.to_json())

# convert the object into a dict
inline_dict = inline_instance.to_dict()
# create an instance of Inline from a dict
inline_from_dict = Inline.from_dict(inline_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

