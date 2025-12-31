# OtpTemplateCreate200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**TwoFaTemplateResource**](TwoFaTemplateResource.md) |  |  |

## Example

```python
from bsg_api.models.otp_template_create200_response import OtpTemplateCreate200Response

# TODO update the JSON string below
json = "{}"
# create an instance of OtpTemplateCreate200Response from a JSON string
otp_template_create200_response_instance = OtpTemplateCreate200Response.from_json(json)
# print the JSON string representation of the object
print(OtpTemplateCreate200Response.to_json())

# convert the object into a dict
otp_template_create200_response_dict = otp_template_create200_response_instance.to_dict()
# create an instance of OtpTemplateCreate200Response from a dict
otp_template_create200_response_from_dict = OtpTemplateCreate200Response.from_dict(otp_template_create200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

