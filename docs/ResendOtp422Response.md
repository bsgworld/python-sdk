# ResendOtp422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | TwoFA Service error. | [optional]  |
| **errors** | **List[str]** | It may be one of the following:  - **Authentication failed status**  This error can occur when attempting to resend the OTP code for an authentication session that has already been completed with a ‘failed’ status. Resending the OTP code is only possible when the authentication session is in the ‘pending’ status.  - **Authentication canceled status** This error can occur when attempting to resend the OTP code for an authentication session that has already been completed with a ‘canceled’ status. Resending the OTP code is only possible when the authentication session is in the ‘pending’ status.  - **Authentication expired**   This error can occur when attempting to resend the OTP code for an authentication session that has already been completed with an ‘expired’ status. Resending the OTP code is only possible when the authentication session is in the ‘pending’ status   | [optional]  |

## Example

```python
from bsg_api.models.resend_otp422_response import ResendOtp422Response

# TODO update the JSON string below
json = "{}"
# create an instance of ResendOtp422Response from a JSON string
resend_otp422_response_instance = ResendOtp422Response.from_json(json)
# print the JSON string representation of the object
print(ResendOtp422Response.to_json())

# convert the object into a dict
resend_otp422_response_dict = resend_otp422_response_instance.to_dict()
# create an instance of ResendOtp422Response from a dict
resend_otp422_response_from_dict = ResendOtp422Response.from_dict(resend_otp422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

