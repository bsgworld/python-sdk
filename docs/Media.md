# Media


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **str** | Contains a link to an image or video that will be to be attached to the message. The link must begin with http/https.  Acceptable formats for images/videos:   - pictures: jpeg, jpg, gif, png  - videos: h263, m4v, mp4, mpeg, mpeg4, webm  - size: images – 2 MB, videos – 10 MB |  |

## Example

```python
from bsg_api.models.media import Media

# TODO update the JSON string below
json = "{}"
# create an instance of Media from a JSON string
media_instance = Media.from_json(json)
# print the JSON string representation of the object
print(Media.to_json())

# convert the object into a dict
media_dict = media_instance.to_dict()
# create an instance of Media from a dict
media_from_dict = Media.from_dict(media_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

