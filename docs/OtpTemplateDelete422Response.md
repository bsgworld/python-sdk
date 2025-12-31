# OtpTemplateDelete422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | The given data was invalid. | [optional]  |
| **errors** | **List[str]** | It may be one of the following:  - **Default template is not available for deletion** This error occurs when attempting to delete a template that is set as the default template. The default template cannot be deleted.   | [optional]  |

## Example

```python
from bsg_api.models.otp_template_delete422_response import OtpTemplateDelete422Response

# TODO update the JSON string below
json = "{}"
# create an instance of OtpTemplateDelete422Response from a JSON string
otp_template_delete422_response_instance = OtpTemplateDelete422Response.from_json(json)
# print the JSON string representation of the object
print(OtpTemplateDelete422Response.to_json())

# convert the object into a dict
otp_template_delete422_response_dict = otp_template_delete422_response_instance.to_dict()
# create an instance of OtpTemplateDelete422Response from a dict
otp_template_delete422_response_from_dict = OtpTemplateDelete422Response.from_dict(otp_template_delete422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

