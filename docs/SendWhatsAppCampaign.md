# SendWhatsAppCampaign


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phones** | [**List[Phone]**](Phone.md) | $phones |  |
| **sender** | **str** | The name of the agent used to send the whatsapp message |  |
| **type** | **str** | Type of Whatsapp message, only \&quot;template\&quot; now is supported |  |
| **template** | [**Template**](Template.md) | Required for type \&quot;template\&quot; | [optional]  |
| **alternative_channel** | [**SendWhatsAppCampaignAlternativeChannel**](SendWhatsAppCampaignAlternativeChannel.md) |  | [optional]  |
| **start_at** | **datetime** | Start sending the messages at | [optional]  |
| **add_to_contact_book** | **bool** | Specifies whether to add the specified phone number of the message recipient to the contact book | [optional] [default to True] |
| **check_stop_list** | **bool** | Check the recipient’s phone number for being in the stop list.  Possible values:    - true – if the number is found in the stop list, do not send the message  - false – ignore the stop list | [optional] [default to True] |

## Example

```python
from bsg_api.models.send_whats_app_campaign import SendWhatsAppCampaign

# TODO update the JSON string below
json = "{}"
# create an instance of SendWhatsAppCampaign from a JSON string
send_whats_app_campaign_instance = SendWhatsAppCampaign.from_json(json)
# print the JSON string representation of the object
print(SendWhatsAppCampaign.to_json())

# convert the object into a dict
send_whats_app_campaign_dict = send_whats_app_campaign_instance.to_dict()
# create an instance of SendWhatsAppCampaign from a dict
send_whats_app_campaign_from_dict = SendWhatsAppCampaign.from_dict(send_whats_app_campaign_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

