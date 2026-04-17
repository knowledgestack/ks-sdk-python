# TenantUsageResponse

Tenant-wide usage for the current billing period.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period_start** | **datetime** |  | 
**period_end** | **datetime** |  | 
**tokens_used** | **int** |  | 
**tokens_limit** | **int** |  | 
**documents_processed** | **int** |  | 
**documents_limit** | **int** |  | 
**percent_tokens_used** | **int** |  | 
**percent_documents_used** | **int** |  | 
**is_custom_limit** | **bool** |  | 

## Example

```python
from ksapi.models.tenant_usage_response import TenantUsageResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TenantUsageResponse from a JSON string
tenant_usage_response_instance = TenantUsageResponse.from_json(json)
# print the JSON string representation of the object
print(TenantUsageResponse.to_json())

# convert the object into a dict
tenant_usage_response_dict = tenant_usage_response_instance.to_dict()
# create an instance of TenantUsageResponse from a dict
tenant_usage_response_from_dict = TenantUsageResponse.from_dict(tenant_usage_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


