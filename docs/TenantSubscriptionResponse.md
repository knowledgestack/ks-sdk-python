# TenantSubscriptionResponse

A tenant's current subscription.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **UUID** |  | 
**plan** | [**BillingPlanResponse**](BillingPlanResponse.md) |  | 
**status** | [**SubscriptionStatus**](SubscriptionStatus.md) |  | 
**cadence** | [**BillingCadence**](BillingCadence.md) |  | 
**seats** | **int** |  | 
**current_period_start** | **datetime** |  | 
**current_period_end** | **datetime** |  | 
**cancel_at_period_end** | **bool** |  | 
**canceled_at** | **datetime** |  | 
**effective_limits** | [**EffectiveLimitsResponse**](EffectiveLimitsResponse.md) |  | 
**billing_contact_user_id** | **UUID** | User whose email receives invoices. null &#x3D; tenant owner. | [optional] 
**billing_contact_group_id** | **UUID** | Group whose email receives invoices. null &#x3D; tenant owner. | [optional] 
**billing_email_resolved** | **str** | Resolved invoice email (from contact user/group, or null if owner default). | [optional] 
**override_notes** | **str** | Human-readable explanation of any custom contract terms | [optional] 

## Example

```python
from ksapi.models.tenant_subscription_response import TenantSubscriptionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TenantSubscriptionResponse from a JSON string
tenant_subscription_response_instance = TenantSubscriptionResponse.from_json(json)
# print the JSON string representation of the object
print(TenantSubscriptionResponse.to_json())

# convert the object into a dict
tenant_subscription_response_dict = tenant_subscription_response_instance.to_dict()
# create an instance of TenantSubscriptionResponse from a dict
tenant_subscription_response_from_dict = TenantSubscriptionResponse.from_dict(tenant_subscription_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


