# StatJobsDelete200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error** | **int** |  | [optional]  |
| **key** | **str** |  | [optional]  |
| **error_description** | **str** |  | [optional]  |

## Example

```python
from bsg_api.models.stat_jobs_delete200_response import StatJobsDelete200Response

# TODO update the JSON string below
json = "{}"
# create an instance of StatJobsDelete200Response from a JSON string
stat_jobs_delete200_response_instance = StatJobsDelete200Response.from_json(json)
# print the JSON string representation of the object
print(StatJobsDelete200Response.to_json())

# convert the object into a dict
stat_jobs_delete200_response_dict = stat_jobs_delete200_response_instance.to_dict()
# create an instance of StatJobsDelete200Response from a dict
stat_jobs_delete200_response_from_dict = StatJobsDelete200Response.from_dict(stat_jobs_delete200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

