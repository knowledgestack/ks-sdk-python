# ThreadMessageDetailsInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**steps** | [**List[StepInput]**](StepInput.md) |  | [optional] 

## Example

```python
from ksapi.models.thread_message_details_input import ThreadMessageDetailsInput

# TODO update the JSON string below
json = "{}"
# create an instance of ThreadMessageDetailsInput from a JSON string
thread_message_details_input_instance = ThreadMessageDetailsInput.from_json(json)
# print the JSON string representation of the object
print(ThreadMessageDetailsInput.to_json())

# convert the object into a dict
thread_message_details_input_dict = thread_message_details_input_instance.to_dict()
# create an instance of ThreadMessageDetailsInput from a dict
thread_message_details_input_from_dict = ThreadMessageDetailsInput.from_dict(thread_message_details_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


