# SmsSendIndividualRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **messages** | [**List[IndividualMessageData]**](IndividualMessageData.md) |  |  |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **start_at** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |

## Example

```python
from bsg_api.models.sms_send_individual_request import SmsSendIndividualRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SmsSendIndividualRequest from a JSON string
sms_send_individual_request_instance = SmsSendIndividualRequest.from_json(json)
# print the JSON string representation of the object
print(SmsSendIndividualRequest.to_json())

# convert the object into a dict
sms_send_individual_request_dict = sms_send_individual_request_instance.to_dict()
# create an instance of SmsSendIndividualRequest from a dict
sms_send_individual_request_from_dict = SmsSendIndividualRequest.from_dict(sms_send_individual_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

