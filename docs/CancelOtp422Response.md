# CancelOtp422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | TwoFA Service error. | [optional]  |
| **errors** | **List[str]** | It may be one of the following:  - **Authentication expired** - This error can occur when attempting to cancel an authentication session that is already completed with an “expired” status. It is only possible to cancel an authentication session while it is in the “pending” status.   - **Authentication failed status** - This error can occur when attempting to cancel an authentication session that is already completed with a “failed” status. It is only possible to cancel an authentication session while it is in the “pending” status.    | [optional]  |

## Example

```python
from bsg_api.models.cancel_otp422_response import CancelOtp422Response

# TODO update the JSON string below
json = "{}"
# create an instance of CancelOtp422Response from a JSON string
cancel_otp422_response_instance = CancelOtp422Response.from_json(json)
# print the JSON string representation of the object
print(CancelOtp422Response.to_json())

# convert the object into a dict
cancel_otp422_response_dict = cancel_otp422_response_instance.to_dict()
# create an instance of CancelOtp422Response from a dict
cancel_otp422_response_from_dict = CancelOtp422Response.from_dict(cancel_otp422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

