# CreatePortalSessionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**return_url** | **str** |  | 

## Example

```python
from ksapi.models.create_portal_session_request import CreatePortalSessionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePortalSessionRequest from a JSON string
create_portal_session_request_instance = CreatePortalSessionRequest.from_json(json)
# print the JSON string representation of the object
print(CreatePortalSessionRequest.to_json())

# convert the object into a dict
create_portal_session_request_dict = create_portal_session_request_instance.to_dict()
# create an instance of CreatePortalSessionRequest from a dict
create_portal_session_request_from_dict = CreatePortalSessionRequest.from_dict(create_portal_session_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


