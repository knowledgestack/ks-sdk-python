# FolderResponseOrDocumentResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**part_type** | **str** | Path part type | 
**id** | **UUID** | Document ID | 
**path_part_id** | **UUID** | PathPart ID | 
**name** | **str** | Document name | 
**parent_path_part_id** | **UUID** | Parent PathPart ID | 
**materialized_path** | **str** | Full materialized path from root | 
**system_managed** | **bool** | Whether this document is system-managed | 
**tenant_id** | **UUID** | Tenant ID | 
**created_at** | **datetime** | Creation timestamp | 
**updated_at** | **datetime** | Last update timestamp | 
**tags** | [**List[TagResponse]**](TagResponse.md) | Tags attached to this document | [optional] 
**document_type** | [**DocumentType**](DocumentType.md) |  | 
**document_origin** | [**DocumentOrigin**](DocumentOrigin.md) |  | 
**active_version_id** | **UUID** | Active version ID | 
**active_version** | [**DocumentVersionResponse**](DocumentVersionResponse.md) |  | 

## Example

```python
from ksapi.models.folder_response_or_document_response import FolderResponseOrDocumentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FolderResponseOrDocumentResponse from a JSON string
folder_response_or_document_response_instance = FolderResponseOrDocumentResponse.from_json(json)
# print the JSON string representation of the object
print(FolderResponseOrDocumentResponse.to_json())

# convert the object into a dict
folder_response_or_document_response_dict = folder_response_or_document_response_instance.to_dict()
# create an instance of FolderResponseOrDocumentResponse from a dict
folder_response_or_document_response_from_dict = FolderResponseOrDocumentResponse.from_dict(folder_response_or_document_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


