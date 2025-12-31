# ResendOtp200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**TwoFactorAuthenticationSchema**](TwoFactorAuthenticationSchema.md) |  |  |

## Example

```python
from bsg_api.models.resend_otp200_response import ResendOtp200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ResendOtp200Response from a JSON string
resend_otp200_response_instance = ResendOtp200Response.from_json(json)
# print the JSON string representation of the object
print(ResendOtp200Response.to_json())

# convert the object into a dict
resend_otp200_response_dict = resend_otp200_response_instance.to_dict()
# create an instance of ResendOtp200Response from a dict
resend_otp200_response_from_dict = ResendOtp200Response.from_dict(resend_otp200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

