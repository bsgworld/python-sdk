# SenderRequests200ResponseMetaPage

Pagination parameters and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **int** | Total items count at all of the pages | [optional]  |
| **limit** | **int** | Limit items at one page | [optional]  |
| **offset** | **int** | Get items starting at offset | [optional] [default to 0] |

## Example

```python
from bsg_api.models.sender_requests200_response_meta_page import SenderRequests200ResponseMetaPage

# TODO update the JSON string below
json = "{}"
# create an instance of SenderRequests200ResponseMetaPage from a JSON string
sender_requests200_response_meta_page_instance = SenderRequests200ResponseMetaPage.from_json(json)
# print the JSON string representation of the object
print(SenderRequests200ResponseMetaPage.to_json())

# convert the object into a dict
sender_requests200_response_meta_page_dict = sender_requests200_response_meta_page_instance.to_dict()
# create an instance of SenderRequests200ResponseMetaPage from a dict
sender_requests200_response_meta_page_from_dict = SenderRequests200ResponseMetaPage.from_dict(sender_requests200_response_meta_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

