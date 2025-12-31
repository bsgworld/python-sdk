# Components


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **str** |  |  |
| **sub_type** | **str** |  | [optional]  |
| **index** | **str** |  | [optional]  |
| **parameters** | [**List[Parameter]**](Parameter.md) |  | [optional]  |

## Example

```python
from bsg_api.models.components import Components

# TODO update the JSON string below
json = "{}"
# create an instance of Components from a JSON string
components_instance = Components.from_json(json)
# print the JSON string representation of the object
print(Components.to_json())

# convert the object into a dict
components_dict = components_instance.to_dict()
# create an instance of Components from a dict
components_from_dict = Components.from_dict(components_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

