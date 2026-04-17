# CreateWorkflowDefinitionRequest

Create a new workflow definition.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**runner_type** | [**WorkflowRunnerType**](WorkflowRunnerType.md) |  | 
**runner_config** | [**SelfHostedRunnerConfig**](SelfHostedRunnerConfig.md) |  | [optional] 
**max_run_duration_seconds** | **int** |  | [optional] [default to 300]
**source_path_part_ids** | **List[UUID]** |  | 
**instruction_path_part_ids** | **List[UUID]** |  | 
**output_path_part_ids** | **List[UUID]** |  | 
**template_path_part_id** | **UUID** |  | [optional] 

## Example

```python
from ksapi.models.create_workflow_definition_request import CreateWorkflowDefinitionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateWorkflowDefinitionRequest from a JSON string
create_workflow_definition_request_instance = CreateWorkflowDefinitionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateWorkflowDefinitionRequest.to_json())

# convert the object into a dict
create_workflow_definition_request_dict = create_workflow_definition_request_instance.to_dict()
# create an instance of CreateWorkflowDefinitionRequest from a dict
create_workflow_definition_request_from_dict = CreateWorkflowDefinitionRequest.from_dict(create_workflow_definition_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


