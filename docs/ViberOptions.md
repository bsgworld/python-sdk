# ViberOptions


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **image_url** | **str** |  | [optional]  |
| **button_caption** | **str** |  | [optional]  |
| **link_url** | **str** | Required if button_caption is set | [optional]  |

## Example

```python
from bsg_api.models.viber_options import ViberOptions

# TODO update the JSON string below
json = "{}"
# create an instance of ViberOptions from a JSON string
viber_options_instance = ViberOptions.from_json(json)
# print the JSON string representation of the object
print(ViberOptions.to_json())

# convert the object into a dict
viber_options_dict = viber_options_instance.to_dict()
# create an instance of ViberOptions from a dict
viber_options_from_dict = ViberOptions.from_dict(viber_options_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

