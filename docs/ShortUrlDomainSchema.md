# ShortUrlDomainSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | Unique Id of short domain (uuid) | [optional]  |
| **system_domain_id** | **str** |  | [optional]  |
| **status** | **str** |  | [optional]  |
| **name** | **str** | short domain | [optional]  |
| **is_default** | **bool** |  | [optional] [default to True] |
| **slug_type** | [**ShortDomainSlugType**](ShortDomainSlugType.md) |  | [optional]  |
| **init_deleted_at** | **datetime** |  | [optional]  |
| **created_at** | **datetime** |  | [optional]  |
| **not_found_page** | **str** | Url to redirect if original link return status 404 not found | [optional]  |
| **can_refresh_status** | **bool** |  | [optional] [default to True] |
| **can_restore** | **bool** |  | [optional] [default to True] |
| **record_type** | **str** | if system_domain_id is null it is necessary to setup your dns | [optional]  |
| **hostname** | **str** | if system_domain_id is null it is necessary to setup your dns | [optional]  |
| **cname** | **str** | if system_domain_id is null it is necessary to setup your dns | [optional]  |
| **count_short_links** | **int** |  | [optional]  |

## Example

```python
from bsg_api.models.short_url_domain_schema import ShortUrlDomainSchema

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlDomainSchema from a JSON string
short_url_domain_schema_instance = ShortUrlDomainSchema.from_json(json)
# print the JSON string representation of the object
print(ShortUrlDomainSchema.to_json())

# convert the object into a dict
short_url_domain_schema_dict = short_url_domain_schema_instance.to_dict()
# create an instance of ShortUrlDomainSchema from a dict
short_url_domain_schema_from_dict = ShortUrlDomainSchema.from_dict(short_url_domain_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

