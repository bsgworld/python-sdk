# CancelOtp200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**TwoFactorAuthenticationSchema**](TwoFactorAuthenticationSchema.md) |  |  |

## Example

```python
from bsg_api.models.cancel_otp200_response import CancelOtp200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CancelOtp200Response from a JSON string
cancel_otp200_response_instance = CancelOtp200Response.from_json(json)
# print the JSON string representation of the object
print(CancelOtp200Response.to_json())

# convert the object into a dict
cancel_otp200_response_dict = cancel_otp200_response_instance.to_dict()
# create an instance of CancelOtp200Response from a dict
cancel_otp200_response_from_dict = CancelOtp200Response.from_dict(cancel_otp200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

