# CreateJobMessage


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **str** | Job creation type |  |
| **message_id** | **List[int]** | Message Ids |  |

## Example

```python
from bsg_api.models.create_job_message import CreateJobMessage

# TODO update the JSON string below
json = "{}"
# create an instance of CreateJobMessage from a JSON string
create_job_message_instance = CreateJobMessage.from_json(json)
# print the JSON string representation of the object
print(CreateJobMessage.to_json())

# convert the object into a dict
create_job_message_dict = create_job_message_instance.to_dict()
# create an instance of CreateJobMessage from a dict
create_job_message_from_dict = CreateJobMessage.from_dict(create_job_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

