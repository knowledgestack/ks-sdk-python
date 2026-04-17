# SetEnterpriseOverrideRequest

Platform-admin-only. Pass ``null`` in any field to leave it unchanged.  Use ``DELETE`` endpoint to clear all overrides.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**override_price_per_seat_cents** | **int** |  | [optional] 
**override_monthly_token_limit** | **int** |  | [optional] 
**override_monthly_document_limit** | **int** |  | [optional] 
**override_max_seats** | **int** |  | [optional] 
**override_litellm_budget_cents_per_user** | **int** |  | [optional] 
**override_notes** | **str** |  | [optional] 

## Example

```python
from ksapi.models.set_enterprise_override_request import SetEnterpriseOverrideRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SetEnterpriseOverrideRequest from a JSON string
set_enterprise_override_request_instance = SetEnterpriseOverrideRequest.from_json(json)
# print the JSON string representation of the object
print(SetEnterpriseOverrideRequest.to_json())

# convert the object into a dict
set_enterprise_override_request_dict = set_enterprise_override_request_instance.to_dict()
# create an instance of SetEnterpriseOverrideRequest from a dict
set_enterprise_override_request_from_dict = SetEnterpriseOverrideRequest.from_dict(set_enterprise_override_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


