# OtpTemplateCreateRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | Name of the template.  A string of 3 to 50 characters. |  |
| **text** | **str** | The text of the template message. |  |
| **countries** | **List[str]** | Two-letter country code(s) for which the template must apply. Sending messages with the OTP code will only be possible if the recipient’s number belongs to the country you specify for the template. | [optional]  |

## Example

```python
from bsg_api.models.otp_template_create_request import OtpTemplateCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of OtpTemplateCreateRequest from a JSON string
otp_template_create_request_instance = OtpTemplateCreateRequest.from_json(json)
# print the JSON string representation of the object
print(OtpTemplateCreateRequest.to_json())

# convert the object into a dict
otp_template_create_request_dict = otp_template_create_request_instance.to_dict()
# create an instance of OtpTemplateCreateRequest from a dict
otp_template_create_request_from_dict = OtpTemplateCreateRequest.from_dict(otp_template_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

