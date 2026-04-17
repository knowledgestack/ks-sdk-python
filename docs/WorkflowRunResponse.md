# WorkflowRunResponse

Workflow run response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **UUID** |  | 
**workflow_definition_id** | **UUID** |  | 
**user_id** | **UUID** |  | 
**runner_type** | [**WorkflowRunnerType**](WorkflowRunnerType.md) |  | 
**status** | [**WorkflowRunStatus**](WorkflowRunStatus.md) |  | 
**started_at** | **datetime** |  | 
**completed_at** | **datetime** |  | 
**run_snapshot** | [**WorkflowRunSnapshot**](WorkflowRunSnapshot.md) |  | 
**error** | **str** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from ksapi.models.workflow_run_response import WorkflowRunResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WorkflowRunResponse from a JSON string
workflow_run_response_instance = WorkflowRunResponse.from_json(json)
# print the JSON string representation of the object
print(WorkflowRunResponse.to_json())

# convert the object into a dict
workflow_run_response_dict = workflow_run_response_instance.to_dict()
# create an instance of WorkflowRunResponse from a dict
workflow_run_response_from_dict = WorkflowRunResponse.from_dict(workflow_run_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


