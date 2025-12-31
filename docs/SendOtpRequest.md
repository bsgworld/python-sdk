# SendOtpRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **recipient** | **str** | The phone number of the recipient of the one-time password. 9 to 15 digits without the + sign. 3 to 15 characters for the sender’s numeric name. |  |
| **channel** | **str** | A channel for sending a one-time password. Possible values: sms, viber. |  |
| **sender** | **str** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) |  |
| **sender_alt** | **str** | Used only for the Viber channel to alternatively send a one-time code in SMS (if it was not possible to send the code in a Viber message, for example, if the recipient is not a Viber user).The name or number of the SMS sender. String up to 15 characters: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. | [optional]  |
| **template_id** | **int** | Unique identifier of the [template](https://app.bsg.world/2fa/templates) with the Approved status. It’s not allowed to specify the template ID in other statuses. The template ID must be from 1 to 9 digits |  |
| **code_lifetime** | **int** | The password expiration time after which the password becomes invalid. An integer from 30 seconds to 300 seconds. |  |
| **code_max_tries** | **int** | The number of password verification attempts. An integer from 1 to 5. |  |
| **code_digits** | **int** | The length of the numeric code, from 3 to 9 digits. |  |

## Example

```python
from bsg_api.models.send_otp_request import SendOtpRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SendOtpRequest from a JSON string
send_otp_request_instance = SendOtpRequest.from_json(json)
# print the JSON string representation of the object
print(SendOtpRequest.to_json())

# convert the object into a dict
send_otp_request_dict = send_otp_request_instance.to_dict()
# create an instance of SendOtpRequest from a dict
send_otp_request_from_dict = SendOtpRequest.from_dict(send_otp_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

