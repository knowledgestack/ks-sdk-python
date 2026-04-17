# DocumentResponse

Document response model.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**part_type** | **str** | Path part type | 
**id** | **UUID** | Document ID | 
**path_part_id** | **UUID** | PathPart ID | 
**name** | **str** | Document name | 
**parent_path_part_id** | **UUID** | Parent PathPart ID | 
**document_type** | [**DocumentType**](DocumentType.md) |  | 
**document_origin** | [**DocumentOrigin**](DocumentOrigin.md) |  | 
**active_version_id** | **UUID** | Active version ID | 
**active_version** | [**DocumentVersionResponse**](DocumentVersionResponse.md) |  | 
**materialized_path** | **str** | Full materialized path from root | 
**system_managed** | **bool** | Whether this document is system-managed | 
**tenant_id** | **UUID** | Tenant ID | 
**created_at** | **datetime** | Creation timestamp | 
**updated_at** | **datetime** | Last update timestamp | 
**tags** | [**List[TagResponse]**](TagResponse.md) | Tags attached to this document | [optional] 

## Example

```python
from ksapi.models.document_response import DocumentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DocumentResponse from a JSON string
document_response_instance = DocumentResponse.from_json(json)
# print the JSON string representation of the object
print(DocumentResponse.to_json())

# convert the object into a dict
document_response_dict = document_response_instance.to_dict()
# create an instance of DocumentResponse from a dict
document_response_from_dict = DocumentResponse.from_dict(document_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


