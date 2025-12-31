# SendOtp201Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**TwoFactorAuthenticationSchema**](TwoFactorAuthenticationSchema.md) |  |  |

## Example

```python
from bsg_api.models.send_otp201_response import SendOtp201Response

# TODO update the JSON string below
json = "{}"
# create an instance of SendOtp201Response from a JSON string
send_otp201_response_instance = SendOtp201Response.from_json(json)
# print the JSON string representation of the object
print(SendOtp201Response.to_json())

# convert the object into a dict
send_otp201_response_dict = send_otp201_response_instance.to_dict()
# create an instance of SendOtp201Response from a dict
send_otp201_response_from_dict = SendOtp201Response.from_dict(send_otp201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

