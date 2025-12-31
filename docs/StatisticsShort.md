# StatisticsShort


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivered** | **int** | messages that already delivered | [optional]  |
| **sent** | **int** | messages that already sent | [optional]  |

## Example

```python
from bsg_api.models.statistics_short import StatisticsShort

# TODO update the JSON string below
json = "{}"
# create an instance of StatisticsShort from a JSON string
statistics_short_instance = StatisticsShort.from_json(json)
# print the JSON string representation of the object
print(StatisticsShort.to_json())

# convert the object into a dict
statistics_short_dict = statistics_short_instance.to_dict()
# create an instance of StatisticsShort from a dict
statistics_short_from_dict = StatisticsShort.from_dict(statistics_short_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

