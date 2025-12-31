# StatusOtp404Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | TwoFA Service error. | [optional]  |
| **errors** | **List[str]** | It may be one of the following: - **Authentication not found** - This error can occur when the authentication identifier is specified incorrectly or the specified authentication is not present in the system. Please ensure that you are using the correct authentication identifier and try again.  | [optional]  |

## Example

```python
from bsg_api.models.status_otp404_response import StatusOtp404Response

# TODO update the JSON string below
json = "{}"
# create an instance of StatusOtp404Response from a JSON string
status_otp404_response_instance = StatusOtp404Response.from_json(json)
# print the JSON string representation of the object
print(StatusOtp404Response.to_json())

# convert the object into a dict
status_otp404_response_dict = status_otp404_response_instance.to_dict()
# create an instance of StatusOtp404Response from a dict
status_otp404_response_from_dict = StatusOtp404Response.from_dict(status_otp404_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

