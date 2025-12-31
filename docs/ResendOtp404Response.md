# ResendOtp404Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | TwoFA Service error. | [optional]  |
| **errors** | **List[str]** | It may be one of the following: - **Authentication not found** - This error can occur when the authentication identifier is specified incorrectly or the specified authentication is not present in the system. Please ensure that you are using the correct authentication identifier and try again.  | [optional]  |

## Example

```python
from bsg_api.models.resend_otp404_response import ResendOtp404Response

# TODO update the JSON string below
json = "{}"
# create an instance of ResendOtp404Response from a JSON string
resend_otp404_response_instance = ResendOtp404Response.from_json(json)
# print the JSON string representation of the object
print(ResendOtp404Response.to_json())

# convert the object into a dict
resend_otp404_response_dict = resend_otp404_response_instance.to_dict()
# create an instance of ResendOtp404Response from a dict
resend_otp404_response_from_dict = ResendOtp404Response.from_dict(resend_otp404_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

