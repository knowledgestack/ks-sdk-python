# SelfHostedRunnerConfig

Configuration for self-hosted workflow runner.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | 
**webhook_secret** | **str** |  | 

## Example

```python
from ksapi.models.self_hosted_runner_config import SelfHostedRunnerConfig

# TODO update the JSON string below
json = "{}"
# create an instance of SelfHostedRunnerConfig from a JSON string
self_hosted_runner_config_instance = SelfHostedRunnerConfig.from_json(json)
# print the JSON string representation of the object
print(SelfHostedRunnerConfig.to_json())

# convert the object into a dict
self_hosted_runner_config_dict = self_hosted_runner_config_instance.to_dict()
# create an instance of SelfHostedRunnerConfig from a dict
self_hosted_runner_config_from_dict = SelfHostedRunnerConfig.from_dict(self_hosted_runner_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


