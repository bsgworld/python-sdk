# OtpTemplateDelete404Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | TwoFA Service error. | [optional]  |
| **errors** | **List[str]** | It may be one of the following: - **Template not found** This error can occur when the template identifier is specified incorrectly or the specified template is not present in the system. Please ensure that you are using the correct template identifier and try again.  | [optional]  |

## Example

```python
from bsg_api.models.otp_template_delete404_response import OtpTemplateDelete404Response

# TODO update the JSON string below
json = "{}"
# create an instance of OtpTemplateDelete404Response from a JSON string
otp_template_delete404_response_instance = OtpTemplateDelete404Response.from_json(json)
# print the JSON string representation of the object
print(OtpTemplateDelete404Response.to_json())

# convert the object into a dict
otp_template_delete404_response_dict = otp_template_delete404_response_instance.to_dict()
# create an instance of OtpTemplateDelete404Response from a dict
otp_template_delete404_response_from_dict = OtpTemplateDelete404Response.from_dict(otp_template_delete404_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

