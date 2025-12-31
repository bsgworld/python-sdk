# OtpTemplateList200ResponseData


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list** | [**List[TwoFaTemplateResource]**](TwoFaTemplateResource.md) |  | [optional]  |
| **total** | **int** | A total number of templates that meet the search conditions. | [optional]  |

## Example

```python
from bsg_api.models.otp_template_list200_response_data import OtpTemplateList200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of OtpTemplateList200ResponseData from a JSON string
otp_template_list200_response_data_instance = OtpTemplateList200ResponseData.from_json(json)
# print the JSON string representation of the object
print(OtpTemplateList200ResponseData.to_json())

# convert the object into a dict
otp_template_list200_response_data_dict = otp_template_list200_response_data_instance.to_dict()
# create an instance of OtpTemplateList200ResponseData from a dict
otp_template_list200_response_data_from_dict = OtpTemplateList200ResponseData.from_dict(otp_template_list200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

