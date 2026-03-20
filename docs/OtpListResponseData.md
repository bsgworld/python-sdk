# OtpListResponseData


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list** | [**List[TwoFactorAuthenticationMessagesResource]**](TwoFactorAuthenticationMessagesResource.md) |  | [optional]  |
| **total** | **int** | The total number of authentications. | [optional]  |

## Example

```python
from bsg_api.models.otp_list_response_data import OtpListResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of OtpListResponseData from a JSON string
otp_list_response_data_instance = OtpListResponseData.from_json(json)
# print the JSON string representation of the object
print(OtpListResponseData.to_json())

# convert the object into a dict
otp_list_response_data_dict = otp_list_response_data_instance.to_dict()
# create an instance of OtpListResponseData from a dict
otp_list_response_data_from_dict = OtpListResponseData.from_dict(otp_list_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

