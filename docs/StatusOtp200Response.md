# StatusOtp200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**TwoFactorAuthenticationMessagesResource**](TwoFactorAuthenticationMessagesResource.md) |  |  |

## Example

```python
from bsg_api.models.status_otp200_response import StatusOtp200Response

# TODO update the JSON string below
json = "{}"
# create an instance of StatusOtp200Response from a JSON string
status_otp200_response_instance = StatusOtp200Response.from_json(json)
# print the JSON string representation of the object
print(StatusOtp200Response.to_json())

# convert the object into a dict
status_otp200_response_dict = status_otp200_response_instance.to_dict()
# create an instance of StatusOtp200Response from a dict
status_otp200_response_from_dict = StatusOtp200Response.from_dict(status_otp200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

