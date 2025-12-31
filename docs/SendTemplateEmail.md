# SendTemplateEmail


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **to** | **List[str]** | List of email addresses to send the email to |  |
| **var_from** | **str** | The sender’s email address |  |
| **template_id** | **int** | ID of the email template to be used for the email’s content |  |
| **subject** | **str** | The subject line of the email | [optional]  |
| **template_content** | **Dict[str, str]** | JSON object with key-value pairs for dynamic content in the email template | [optional]  |
| **inlines** | [**List[Inline]**](Inline.md) | A list of inline attachments | [optional]  |

## Example

```python
from bsg_api.models.send_template_email import SendTemplateEmail

# TODO update the JSON string below
json = "{}"
# create an instance of SendTemplateEmail from a JSON string
send_template_email_instance = SendTemplateEmail.from_json(json)
# print the JSON string representation of the object
print(SendTemplateEmail.to_json())

# convert the object into a dict
send_template_email_dict = send_template_email_instance.to_dict()
# create an instance of SendTemplateEmail from a dict
send_template_email_from_dict = SendTemplateEmail.from_dict(send_template_email_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

