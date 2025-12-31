# VerifyOtp200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**TwoFactorAuthenticationSchema**](TwoFactorAuthenticationSchema.md) |  |  |

## Example

```python
from bsg_api.models.verify_otp200_response import VerifyOtp200Response

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyOtp200Response from a JSON string
verify_otp200_response_instance = VerifyOtp200Response.from_json(json)
# print the JSON string representation of the object
print(VerifyOtp200Response.to_json())

# convert the object into a dict
verify_otp200_response_dict = verify_otp200_response_instance.to_dict()
# create an instance of VerifyOtp200Response from a dict
verify_otp200_response_from_dict = VerifyOtp200Response.from_dict(verify_otp200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

