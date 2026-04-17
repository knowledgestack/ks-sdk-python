# WorkflowRunSnapshot

Frozen ABCD configuration captured at workflow trigger time.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**workflow_definition_id** | **UUID** |  | 
**workflow_name** | **str** |  | 
**runner_type** | [**WorkflowRunnerType**](WorkflowRunnerType.md) |  | 
**user_id** | **UUID** |  | 
**max_run_duration_seconds** | **int** |  | 
**sources** | [**List[ABCDPathSnapshot]**](ABCDPathSnapshot.md) |  | 
**instructions** | [**List[ABCDPathSnapshot]**](ABCDPathSnapshot.md) |  | 
**outputs** | [**List[ABCDPathSnapshot]**](ABCDPathSnapshot.md) |  | 
**template** | [**ABCDPathSnapshot**](ABCDPathSnapshot.md) |  | 

## Example

```python
from ksapi.models.workflow_run_snapshot import WorkflowRunSnapshot

# TODO update the JSON string below
json = "{}"
# create an instance of WorkflowRunSnapshot from a JSON string
workflow_run_snapshot_instance = WorkflowRunSnapshot.from_json(json)
# print the JSON string representation of the object
print(WorkflowRunSnapshot.to_json())

# convert the object into a dict
workflow_run_snapshot_dict = workflow_run_snapshot_instance.to_dict()
# create an instance of WorkflowRunSnapshot from a dict
workflow_run_snapshot_from_dict = WorkflowRunSnapshot.from_dict(workflow_run_snapshot_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


