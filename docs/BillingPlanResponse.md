# BillingPlanResponse

A plan in the catalog.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **UUID** |  | 
**tier** | [**BillingPlanTier**](BillingPlanTier.md) |  | 
**display_name** | **str** |  | 
**description** | **str** |  | 
**monthly_price_per_seat_cents** | **int** |  | 
**annual_price_per_seat_cents** | **int** |  | 
**annual_discount_percent** | **int** | Discount (%) from 12x monthly rate if annual (0-100) | 
**max_seats** | **int** |  | 
**monthly_token_limit** | **int** |  | 
**monthly_document_limit** | **int** |  | 
**litellm_budget_cents_per_user** | **int** | Per-tenant-user hard LLM spend cap (cents/month). | 
**sort_order** | **int** |  | 

## Example

```python
from ksapi.models.billing_plan_response import BillingPlanResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BillingPlanResponse from a JSON string
billing_plan_response_instance = BillingPlanResponse.from_json(json)
# print the JSON string representation of the object
print(BillingPlanResponse.to_json())

# convert the object into a dict
billing_plan_response_dict = billing_plan_response_instance.to_dict()
# create an instance of BillingPlanResponse from a dict
billing_plan_response_from_dict = BillingPlanResponse.from_dict(billing_plan_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


