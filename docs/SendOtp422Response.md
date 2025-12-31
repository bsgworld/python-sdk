# SendOtp422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | The given data was invalid. | [optional]  |
| **errors** | **List[str]** | It may be one of the following:  - **User channel not found**  This error can occur when the channel is specified incorrectly. Please ensure that you are using the correct channel and try again.  - **Template not found**  This error can occur when the template identifier is specified incorrectly or the specified template is not present in the system. Please ensure that you are using the correct template identifier and try again.  - **Invalid template status**  This error occurs when the provided template identifier in the request does not match the “Approved” status.  - **Insufficient funds**  Insufficient funds to send OTP. Please top up your account.  - **Exists on the stop list**  We’re unable to send message as the phone number of recipient is currently in stop list.  - **User channel inactive**  The message sending method is disabled. Please enable method in your personal account and try again.  - **This action is available for the account of your type only for your manager phone number.**  To send OTP code is not allowed in Demo account mode.   - **Authentication limit with status pending**  This error can occur when total authentication limit with status “pending” is exceeded for your account.  - **Total authentication limit**  This error can occur when total authentication limit is exceeded for your account.  - **Template is not available** This error occurs when you try to create authentication using a template that is only available in the test mode of your account. Please choose a different template.  | [optional]  |

## Example

```python
from bsg_api.models.send_otp422_response import SendOtp422Response

# TODO update the JSON string below
json = "{}"
# create an instance of SendOtp422Response from a JSON string
send_otp422_response_instance = SendOtp422Response.from_json(json)
# print the JSON string representation of the object
print(SendOtp422Response.to_json())

# convert the object into a dict
send_otp422_response_dict = send_otp422_response_instance.to_dict()
# create an instance of SendOtp422Response from a dict
send_otp422_response_from_dict = SendOtp422Response.from_dict(send_otp422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

