# VerifyOtp404Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | TwoFA Service error. | [optional]  |
| **errors** | **List[str]** | It may be one of the following: - **Authentication not found** - This error can occur when the authentication identifier is specified incorrectly or the specified authentication is not present in the system. Please ensure that you are using the correct authentication identifier and try again. - **The code does not match the expected value** - The error occurs when the provided code does not match the value that was sent to the recipient’s number.  | [optional]  |

## Example

```python
from bsg_api.models.verify_otp404_response import VerifyOtp404Response

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyOtp404Response from a JSON string
verify_otp404_response_instance = VerifyOtp404Response.from_json(json)
# print the JSON string representation of the object
print(VerifyOtp404Response.to_json())

# convert the object into a dict
verify_otp404_response_dict = verify_otp404_response_instance.to_dict()
# create an instance of VerifyOtp404Response from a dict
verify_otp404_response_from_dict = VerifyOtp404Response.from_dict(verify_otp404_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

