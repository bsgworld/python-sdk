# OtpList200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**OtpList200ResponseData**](OtpList200ResponseData.md) |  |  |

## Example

```python
from bsg_api.models.otp_list200_response import OtpList200Response

# TODO update the JSON string below
json = "{}"
# create an instance of OtpList200Response from a JSON string
otp_list200_response_instance = OtpList200Response.from_json(json)
# print the JSON string representation of the object
print(OtpList200Response.to_json())

# convert the object into a dict
otp_list200_response_dict = otp_list200_response_instance.to_dict()
# create an instance of OtpList200Response from a dict
otp_list200_response_from_dict = OtpList200Response.from_dict(otp_list200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

