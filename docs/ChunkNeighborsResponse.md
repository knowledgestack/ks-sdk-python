# ChunkNeighborsResponse

Response for chunk neighbor traversal.  Returns items in the same ``SectionOrChunkItem`` discriminated union format used by the document version contents endpoint.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[SectionContentItemOrChunkContentItem]**](SectionContentItemOrChunkContentItem.md) | Ordered siblings: preceding → anchor → succeeding | 
**anchor_index** | **int** | Index of the anchor chunk in items | 

## Example

```python
from ksapi.models.chunk_neighbors_response import ChunkNeighborsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ChunkNeighborsResponse from a JSON string
chunk_neighbors_response_instance = ChunkNeighborsResponse.from_json(json)
# print the JSON string representation of the object
print(ChunkNeighborsResponse.to_json())

# convert the object into a dict
chunk_neighbors_response_dict = chunk_neighbors_response_instance.to_dict()
# create an instance of ChunkNeighborsResponse from a dict
chunk_neighbors_response_from_dict = ChunkNeighborsResponse.from_dict(chunk_neighbors_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


