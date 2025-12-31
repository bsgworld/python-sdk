# Viber


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **str** |  |  |
| **sender** | **str** |  |  |
| **validity_seconds** | **int** | Validity period in seconds. If not set, validity field is used | [optional]  |
| **validity** | **int** | Validity period in hours | [optional] [default to 72] |
| **options** | [**ViberOptions**](ViberOptions.md) |  | [optional]  |
| **check_stop_list** | **bool** |  | [optional] [default to True] |

## Example

```python
from bsg_api.models.viber import Viber

# TODO update the JSON string below
json = "{}"
# create an instance of Viber from a JSON string
viber_instance = Viber.from_json(json)
# print the JSON string representation of the object
print(Viber.to_json())

# convert the object into a dict
viber_dict = viber_instance.to_dict()
# create an instance of Viber from a dict
viber_from_dict = Viber.from_dict(viber_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

