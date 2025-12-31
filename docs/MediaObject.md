# MediaObject


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | Used if link is not set | [optional]  |
| **link** | **str** | Used if id is not set | [optional]  |
| **caption** | **str** |  | [optional]  |
| **filename** | **str** | Describes the filename for the specific document. Use only with document media.     The extension of the filename will specify what format the document is displayed as in WhatsApp | [optional]  |

## Example

```python
from bsg_api.models.media_object import MediaObject

# TODO update the JSON string below
json = "{}"
# create an instance of MediaObject from a JSON string
media_object_instance = MediaObject.from_json(json)
# print the JSON string representation of the object
print(MediaObject.to_json())

# convert the object into a dict
media_object_dict = media_object_instance.to_dict()
# create an instance of MediaObject from a dict
media_object_from_dict = MediaObject.from_dict(media_object_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

