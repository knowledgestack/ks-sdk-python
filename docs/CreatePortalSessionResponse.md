# CreatePortalSessionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**portal_url** | **str** |  | 
**session_id** | **str** |  | 

## Example

```python
from ksapi.models.create_portal_session_response import CreatePortalSessionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePortalSessionResponse from a JSON string
create_portal_session_response_instance = CreatePortalSessionResponse.from_json(json)
# print the JSON string representation of the object
print(CreatePortalSessionResponse.to_json())

# convert the object into a dict
create_portal_session_response_dict = create_portal_session_response_instance.to_dict()
# create an instance of CreatePortalSessionResponse from a dict
create_portal_session_response_from_dict = CreatePortalSessionResponse.from_dict(create_portal_session_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


