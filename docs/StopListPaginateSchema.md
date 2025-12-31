# StopListPaginateSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | ID of the contact added to the stop list | [optional]  |
| **phone** | **int** | Phone number without leading plus, just digits | [optional]  |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **sms_stoplist** | **bool** | Whether the contact was added to the SMS stop list | [optional]  |
| **viber_stoplist** | **bool** | Whether the contact was added to the Viber stop list | [optional]  |
| **rcs_stoplist** | **bool** | Whether the contact was added to the Rcs stop list | [optional]  |

## Example

```python
from bsg_api.models.stop_list_paginate_schema import StopListPaginateSchema

# TODO update the JSON string below
json = "{}"
# create an instance of StopListPaginateSchema from a JSON string
stop_list_paginate_schema_instance = StopListPaginateSchema.from_json(json)
# print the JSON string representation of the object
print(StopListPaginateSchema.to_json())

# convert the object into a dict
stop_list_paginate_schema_dict = stop_list_paginate_schema_instance.to_dict()
# create an instance of StopListPaginateSchema from a dict
stop_list_paginate_schema_from_dict = StopListPaginateSchema.from_dict(stop_list_paginate_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

