# PhonesTrait


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phones** | [**List[Phone]**](Phone.md) | The list of objects containing information about the mobile phone number (number) and (reference_id) to send a message to |  |

## Example

```python
from bsg_api.models.phones_trait import PhonesTrait

# TODO update the JSON string below
json = "{}"
# create an instance of PhonesTrait from a JSON string
phones_trait_instance = PhonesTrait.from_json(json)
# print the JSON string representation of the object
print(PhonesTrait.to_json())

# convert the object into a dict
phones_trait_dict = phones_trait_instance.to_dict()
# create an instance of PhonesTrait from a dict
phones_trait_from_dict = PhonesTrait.from_dict(phones_trait_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

