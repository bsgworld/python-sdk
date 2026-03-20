# CreateJobParams


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **str** | Job creation type |  |
| **time_in_from** | **datetime** | Datetime when messages were received on the platform |  |
| **time_in_to** | **datetime** | Datetime when messages were received on the platform |  |
| **time_sent_from** | **datetime** | Time of sending messages from the platform “from” | [optional]  |
| **time_sent_to** | **datetime** | Time of sending messages from the platform “to” | [optional]  |
| **phones** | **List[int]** | phone list | [optional]  |
| **sender** | **str** | Source from where the message came to the platform | [optional]  |
| **source** | **str** | Source from where the message came to the platform | [optional]  |
| **country** | **str** | The name of the country for search | [optional]  |
| **operator_id** | **str** | Indication of the country operator | [optional]  |
| **status** | **str** | The status of the messages to display | [optional]  |
| **sl_clicks** | **str** | The field is available only to the clients who have enabled Short URL service | [optional]  |
| **sl_clicks_comp** | **str** | Comparison operator with the clicks count value | [optional]  |
| **sl_clicks_count** | **str** | Comparison operator with the clicks count value | [optional]  |

## Example

```python
from bsg_api.models.create_job_params import CreateJobParams

# TODO update the JSON string below
json = "{}"
# create an instance of CreateJobParams from a JSON string
create_job_params_instance = CreateJobParams.from_json(json)
# print the JSON string representation of the object
print(CreateJobParams.to_json())

# convert the object into a dict
create_job_params_dict = create_job_params_instance.to_dict()
# create an instance of CreateJobParams from a dict
create_job_params_from_dict = CreateJobParams.from_dict(create_job_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

