# SelfHostedRunnerConfigResponse

Response-safe version of runner config — excludes webhook_secret.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | 

## Example

```python
from ksapi.models.self_hosted_runner_config_response import SelfHostedRunnerConfigResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SelfHostedRunnerConfigResponse from a JSON string
self_hosted_runner_config_response_instance = SelfHostedRunnerConfigResponse.from_json(json)
# print the JSON string representation of the object
print(SelfHostedRunnerConfigResponse.to_json())

# convert the object into a dict
self_hosted_runner_config_response_dict = self_hosted_runner_config_response_instance.to_dict()
# create an instance of SelfHostedRunnerConfigResponse from a dict
self_hosted_runner_config_response_from_dict = SelfHostedRunnerConfigResponse.from_dict(self_hosted_runner_config_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


