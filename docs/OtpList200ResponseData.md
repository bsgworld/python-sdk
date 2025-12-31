# OtpList200ResponseData


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list** | [**List[TwoFactorAuthenticationMessagesResource]**](TwoFactorAuthenticationMessagesResource.md) |  | [optional]  |
| **total** | **int** | The total number of authentications. | [optional]  |

## Example

```python
from bsg_api.models.otp_list200_response_data import OtpList200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of OtpList200ResponseData from a JSON string
otp_list200_response_data_instance = OtpList200ResponseData.from_json(json)
# print the JSON string representation of the object
print(OtpList200ResponseData.to_json())

# convert the object into a dict
otp_list200_response_data_dict = otp_list200_response_data_instance.to_dict()
# create an instance of OtpList200ResponseData from a dict
otp_list200_response_data_from_dict = OtpList200ResponseData.from_dict(otp_list200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

