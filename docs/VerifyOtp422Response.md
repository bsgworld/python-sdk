# VerifyOtp422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | TwoFA Service error. | [optional]  |
| **errors** | **List[str]** | It may be one of the following:  - **Authentication expired** - Your OTP password has expired. OTP password is no longer valid.  - **Authentication failed status** - This error can occur when attempts limit is exceeded for authentication session.   | [optional]  |

## Example

```python
from bsg_api.models.verify_otp422_response import VerifyOtp422Response

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyOtp422Response from a JSON string
verify_otp422_response_instance = VerifyOtp422Response.from_json(json)
# print the JSON string representation of the object
print(VerifyOtp422Response.to_json())

# convert the object into a dict
verify_otp422_response_dict = verify_otp422_response_instance.to_dict()
# create an instance of VerifyOtp422Response from a dict
verify_otp422_response_from_dict = VerifyOtp422Response.from_dict(verify_otp422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

