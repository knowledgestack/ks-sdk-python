# DocumentVersionMetadata

Schema for document_version.system_metadata JSONB field.  Tracks S3 URLs for generated artifacts, pipeline execution state, and document statistics. Convention-based paths (images, page screenshots) are derived from document_id/document_version_id via s3_paths helpers, using a flat S3 layout: documents/{document_id}/{document_version_id}/...  Internal conversion artifact paths (standard_pipeline_json_s3, high_accuracy_*_s3) are excluded from API responses via ``Field(exclude=True)`` so we don't expose underlying technology names to external consumers.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source_s3** | **str** | S3 URL to the source document (set by API on upload) | [optional] 
**cleaned_source_s3** | **str** | S3 URL to watermark-removed source document | [optional] 
**fast_plaintext_s3** | **str** | S3 URL to the fast plaintext export of the document | [optional] 
**hash** | **str** | Base64-encoded SHA256 hash of the uploaded source file | [optional] 
**pipeline_state** | [**PipelineState**](PipelineState.md) |  | [optional] 
**total_pages** | **int** | Total number of pages in the document | [optional] 
**total_sections** | **int** | Total number of sections created | [optional] 
**total_chunks** | **int** | Total number of chunks created | [optional] 
**total_formulas** | **int** | Total formula cells in the workbook (XLSX only) | [optional] 
**xlsx_parse_result_s3** | **str** | S3 URI to the full XLSX parse result JSON containing dependency graph, named ranges, and KPI catalog | [optional] 
**xlsx_named_ranges** | **List[Dict[str, object]]** | Named ranges defined in the workbook (name, ref_string, scope) | [optional] 
**xlsx_kpi_catalog** | **List[Dict[str, object]]** | KPI (Key Performance Indicator) cells detected by the XLSX parser. Each entry contains a label, computed value, cell address, and driver cell references. Applicable to financial models and operational spreadsheets; not populated for template spreadsheets that lack computed KPI cells. | [optional] 
**information_statistics** | [**InformationStatistics**](InformationStatistics.md) |  | [optional] 

## Example

```python
from ksapi.models.document_version_metadata import DocumentVersionMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of DocumentVersionMetadata from a JSON string
document_version_metadata_instance = DocumentVersionMetadata.from_json(json)
# print the JSON string representation of the object
print(DocumentVersionMetadata.to_json())

# convert the object into a dict
document_version_metadata_dict = document_version_metadata_instance.to_dict()
# create an instance of DocumentVersionMetadata from a dict
document_version_metadata_from_dict = DocumentVersionMetadata.from_dict(document_version_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


