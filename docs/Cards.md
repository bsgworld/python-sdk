# Cards


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cards** | [**List[Card]**](Card.md) | The array contains information about the card. The maximum number of cards is 5. Messages with one card are called “Single card”, messages with 2 or more cards are called “Carousel”. Depending on the chosen tariff, the number of cards may be limited (for example, you can send only Single cards).  Details will be provided by manager. |  |

## Example

```python
from bsg_api.models.cards import Cards

# TODO update the JSON string below
json = "{}"
# create an instance of Cards from a JSON string
cards_instance = Cards.from_json(json)
# print the JSON string representation of the object
print(Cards.to_json())

# convert the object into a dict
cards_dict = cards_instance.to_dict()
# create an instance of Cards from a dict
cards_from_dict = Cards.from_dict(cards_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

