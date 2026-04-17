# UpdateDocumentRequest

Request to update a document (rename, move, and/or change active version).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | New document name | [optional] 
**parent_path_part_id** | **UUID** | New parent PathPart ID for move (must be a FOLDER type) | [optional] 
**active_version_id** | **UUID** | New active version ID | [optional] 

## Example

```python
from ksapi.models.update_document_request import UpdateDocumentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateDocumentRequest from a JSON string
update_document_request_instance = UpdateDocumentRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateDocumentRequest.to_json())

# convert the object into a dict
update_document_request_dict = update_document_request_instance.to_dict()
# create an instance of UpdateDocumentRequest from a dict
update_document_request_from_dict = UpdateDocumentRequest.from_dict(update_document_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


