# PaginatedResponseAnnotatedUnionFolderResponseDocumentResponseDiscriminator


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[FolderResponseOrDocumentResponse]**](FolderResponseOrDocumentResponse.md) | List of items | 
**total** | **int** | Total number of items | 
**limit** | **int** | Number of items per page | 
**offset** | **int** | Number of items to skip | 

## Example

```python
from ksapi.models.paginated_response_annotated_union_folder_response_document_response_discriminator import PaginatedResponseAnnotatedUnionFolderResponseDocumentResponseDiscriminator

# TODO update the JSON string below
json = "{}"
# create an instance of PaginatedResponseAnnotatedUnionFolderResponseDocumentResponseDiscriminator from a JSON string
paginated_response_annotated_union_folder_response_document_response_discriminator_instance = PaginatedResponseAnnotatedUnionFolderResponseDocumentResponseDiscriminator.from_json(json)
# print the JSON string representation of the object
print(PaginatedResponseAnnotatedUnionFolderResponseDocumentResponseDiscriminator.to_json())

# convert the object into a dict
paginated_response_annotated_union_folder_response_document_response_discriminator_dict = paginated_response_annotated_union_folder_response_document_response_discriminator_instance.to_dict()
# create an instance of PaginatedResponseAnnotatedUnionFolderResponseDocumentResponseDiscriminator from a dict
paginated_response_annotated_union_folder_response_document_response_discriminator_from_dict = PaginatedResponseAnnotatedUnionFolderResponseDocumentResponseDiscriminator.from_dict(paginated_response_annotated_union_folder_response_document_response_discriminator_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


