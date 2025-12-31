# DateTimeParameter


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **fallback_value** | **str** | Default text. For Cloud API, we always use the fallback value, and we do not attempt to localize using other optional fields |  |

## Example

```python
from bsg_api.models.date_time_parameter import DateTimeParameter

# TODO update the JSON string below
json = "{}"
# create an instance of DateTimeParameter from a JSON string
date_time_parameter_instance = DateTimeParameter.from_json(json)
# print the JSON string representation of the object
print(DateTimeParameter.to_json())

# convert the object into a dict
date_time_parameter_dict = date_time_parameter_instance.to_dict()
# create an instance of DateTimeParameter from a dict
date_time_parameter_from_dict = DateTimeParameter.from_dict(date_time_parameter_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

