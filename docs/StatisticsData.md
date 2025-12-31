# StatisticsData


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivered** | **int** |  | [optional]  |
| **sent** | **int** |  | [optional]  |
| **scheduled** | **int** |  | [optional]  |
| **moderation** | **int** |  | [optional]  |
| **accepted** | **int** |  | [optional]  |
| **sending** | **int** |  | [optional]  |
| **expired** | **int** |  | [optional]  |
| **failed** | **int** |  | [optional]  |
| **undelivered** | **int** |  | [optional]  |
| **unknown** | **int** |  | [optional]  |
| **read** | **int** |  | [optional]  |
| **not_viber_user** | **int** |  | [optional]  |
| **not_rcs_user** | **int** |  | [optional]  |

## Example

```python
from bsg_api.models.statistics_data import StatisticsData

# TODO update the JSON string below
json = "{}"
# create an instance of StatisticsData from a JSON string
statistics_data_instance = StatisticsData.from_json(json)
# print the JSON string representation of the object
print(StatisticsData.to_json())

# convert the object into a dict
statistics_data_dict = statistics_data_instance.to_dict()
# create an instance of StatisticsData from a dict
statistics_data_from_dict = StatisticsData.from_dict(statistics_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

