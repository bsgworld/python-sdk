# ShortUrlDomainListSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** |  | [optional]  |
| **system_domain_id** | **str** |  | [optional]  |
| **status** | **str** |  | [optional]  |
| **name** | **str** |  | [optional]  |
| **is_default** | **bool** |  | [optional] [default to True] |
| **init_deleted_at** | **datetime** |  | [optional]  |
| **created_at** | **datetime** |  | [optional]  |
| **can_refresh_status** | **bool** |  | [optional] [default to True] |
| **can_restore** | **bool** |  | [optional] [default to True] |
| **count_short_links** | **int** |  | [optional]  |

## Example

```python
from bsg_api.models.short_url_domain_list_schema import ShortUrlDomainListSchema

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlDomainListSchema from a JSON string
short_url_domain_list_schema_instance = ShortUrlDomainListSchema.from_json(json)
# print the JSON string representation of the object
print(ShortUrlDomainListSchema.to_json())

# convert the object into a dict
short_url_domain_list_schema_dict = short_url_domain_list_schema_instance.to_dict()
# create an instance of ShortUrlDomainListSchema from a dict
short_url_domain_list_schema_from_dict = ShortUrlDomainListSchema.from_dict(short_url_domain_list_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

