# SendEmail


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **to** | **List[str]** | List of email addresses to send the email to |  |
| **var_from** | **str** | The sender’s email address |  |
| **subject** | **str** | The subject line of the email |  |
| **body** | **str** | Optional email body as plain text in addition to &#x60;htmlbody&#x60; for old email clients without html support | [optional]  |
| **htmlbody** | **str** | The HTML-formatted content of the email body (can include rich text elements) |  |
| **inlines** | [**List[Inline]**](Inline.md) | A list of inline attachments | [optional]  |

## Example

```python
from bsg_api.models.send_email import SendEmail

# TODO update the JSON string below
json = "{}"
# create an instance of SendEmail from a JSON string
send_email_instance = SendEmail.from_json(json)
# print the JSON string representation of the object
print(SendEmail.to_json())

# convert the object into a dict
send_email_dict = send_email_instance.to_dict()
# create an instance of SendEmail from a dict
send_email_from_dict = SendEmail.from_dict(send_email_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

