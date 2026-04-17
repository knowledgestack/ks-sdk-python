# WorkflowDefinitionResponse

Workflow definition response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **UUID** |  | 
**name** | **str** |  | 
**description** | **str** |  | 
**runner_type** | [**WorkflowRunnerType**](WorkflowRunnerType.md) |  | 
**runner_config** | [**SelfHostedRunnerConfigResponse**](SelfHostedRunnerConfigResponse.md) |  | 
**max_run_duration_seconds** | **int** |  | 
**source_path_part_ids** | **List[UUID]** |  | 
**instruction_path_part_ids** | **List[UUID]** |  | 
**output_path_part_ids** | **List[UUID]** |  | 
**template_path_part_id** | **UUID** |  | 
**is_active** | **bool** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from ksapi.models.workflow_definition_response import WorkflowDefinitionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WorkflowDefinitionResponse from a JSON string
workflow_definition_response_instance = WorkflowDefinitionResponse.from_json(json)
# print the JSON string representation of the object
print(WorkflowDefinitionResponse.to_json())

# convert the object into a dict
workflow_definition_response_dict = workflow_definition_response_instance.to_dict()
# create an instance of WorkflowDefinitionResponse from a dict
workflow_definition_response_from_dict = WorkflowDefinitionResponse.from_dict(workflow_definition_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


