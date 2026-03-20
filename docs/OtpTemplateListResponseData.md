# OtpTemplateListResponseData


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list** | [**List[TwoFaTemplateResource]**](TwoFaTemplateResource.md) |  | [optional]  |
| **total** | **int** | A total number of templates that meet the search conditions. | [optional]  |

## Example

```python
from bsg_api.models.otp_template_list_response_data import OtpTemplateListResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of OtpTemplateListResponseData from a JSON string
otp_template_list_response_data_instance = OtpTemplateListResponseData.from_json(json)
# print the JSON string representation of the object
print(OtpTemplateListResponseData.to_json())

# convert the object into a dict
otp_template_list_response_data_dict = otp_template_list_response_data_instance.to_dict()
# create an instance of OtpTemplateListResponseData from a dict
otp_template_list_response_data_from_dict = OtpTemplateListResponseData.from_dict(otp_template_list_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

