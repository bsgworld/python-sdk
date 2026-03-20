# StatJobsCreate200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error** | **int** |  | [optional]  |
| **key** | **str** |  | [optional]  |
| **error_description** | **str** |  | [optional]  |

## Example

```python
from bsg_api.models.stat_jobs_create200_response import StatJobsCreate200Response

# TODO update the JSON string below
json = "{}"
# create an instance of StatJobsCreate200Response from a JSON string
stat_jobs_create200_response_instance = StatJobsCreate200Response.from_json(json)
# print the JSON string representation of the object
print(StatJobsCreate200Response.to_json())

# convert the object into a dict
stat_jobs_create200_response_dict = stat_jobs_create200_response_instance.to_dict()
# create an instance of StatJobsCreate200Response from a dict
stat_jobs_create200_response_from_dict = StatJobsCreate200Response.from_dict(stat_jobs_create200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

