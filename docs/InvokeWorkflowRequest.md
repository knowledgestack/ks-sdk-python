# InvokeWorkflowRequest

Request body for invoking a workflow definition.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**idempotency_key** | **str** | Optional key to prevent duplicate runs from retries | [optional] 

## Example

```python
from ksapi.models.invoke_workflow_request import InvokeWorkflowRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InvokeWorkflowRequest from a JSON string
invoke_workflow_request_instance = InvokeWorkflowRequest.from_json(json)
# print the JSON string representation of the object
print(InvokeWorkflowRequest.to_json())

# convert the object into a dict
invoke_workflow_request_dict = invoke_workflow_request_instance.to_dict()
# create an instance of InvokeWorkflowRequest from a dict
invoke_workflow_request_from_dict = InvokeWorkflowRequest.from_dict(invoke_workflow_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


