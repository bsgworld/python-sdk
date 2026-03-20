# SendViberCampaign


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phones** | [**List[Phone]**](Phone.md) | The list of objects containing information about the mobile phone number (number) and (reference_id) to send a message to |  |
| **sender** | **str** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) |  |
| **text** | **str** |  |  |
| **image_url** | **str** |  | [optional]  |
| **button_caption** | **str** |  | [optional]  |
| **link_url** | **str** | Required if button_caption is set | [optional]  |
| **start_at** | **datetime** | Start sending the messages at | [optional]  |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **alternative_channel** | [**AlternativeChannel**](AlternativeChannel.md) |  | [optional]  |
| **add_to_contact_book** | **bool** | Specifies whether to add the specified phone number of the message recipient to the contact book | [optional] [default to True] |
| **check_stop_list** | **bool** | Check the recipient’s phone number for being in the stop list.  Possible values:    - true – if the number is found in the stop list, do not send the message  - false – ignore the stop list | [optional] [default to True] |

## Example

```python
from bsg_api.models.send_viber_campaign import SendViberCampaign

# TODO update the JSON string below
json = "{}"
# create an instance of SendViberCampaign from a JSON string
send_viber_campaign_instance = SendViberCampaign.from_json(json)
# print the JSON string representation of the object
print(SendViberCampaign.to_json())

# convert the object into a dict
send_viber_campaign_dict = send_viber_campaign_instance.to_dict()
# create an instance of SendViberCampaign from a dict
send_viber_campaign_from_dict = SendViberCampaign.from_dict(send_viber_campaign_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

