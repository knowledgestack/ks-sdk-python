# EffectiveLimitsResponse

Resolved limits for a tenant (plan defaults + overrides).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**price_per_seat_cents_monthly** | **int** |  | 
**price_per_seat_cents_billed** | **int** |  | 
**monthly_token_limit** | **int** |  | 
**monthly_document_limit** | **int** |  | 
**max_seats** | **int** |  | 
**litellm_budget_cents_per_user** | **int** |  | 
**has_custom_overrides** | **bool** |  | 

## Example

```python
from ksapi.models.effective_limits_response import EffectiveLimitsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of EffectiveLimitsResponse from a JSON string
effective_limits_response_instance = EffectiveLimitsResponse.from_json(json)
# print the JSON string representation of the object
print(EffectiveLimitsResponse.to_json())

# convert the object into a dict
effective_limits_response_dict = effective_limits_response_instance.to_dict()
# create an instance of EffectiveLimitsResponse from a dict
effective_limits_response_from_dict = EffectiveLimitsResponse.from_dict(effective_limits_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


