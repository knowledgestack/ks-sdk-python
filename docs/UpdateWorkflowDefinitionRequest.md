# UpdateWorkflowDefinitionRequest

Full replacement (PUT semantics). All fields are required.

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
**is_active** | **bool** |  | [optional] [default to True]

## Example

```python
from ksapi.models.update_workflow_definition_request import UpdateWorkflowDefinitionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateWorkflowDefinitionRequest from a JSON string
update_workflow_definition_request_instance = UpdateWorkflowDefinitionRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateWorkflowDefinitionRequest.to_json())

# convert the object into a dict
update_workflow_definition_request_dict = update_workflow_definition_request_instance.to_dict()
# create an instance of UpdateWorkflowDefinitionRequest from a dict
update_workflow_definition_request_from_dict = UpdateWorkflowDefinitionRequest.from_dict(update_workflow_definition_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


