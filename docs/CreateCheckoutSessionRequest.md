# CreateCheckoutSessionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**target_tier** | [**BillingPlanTier**](BillingPlanTier.md) |  | 
**cadence** | [**BillingCadence**](BillingCadence.md) |  | 
**seats** | **int** |  | 
**success_url** | **str** |  | 
**cancel_url** | **str** |  | 

## Example

```python
from ksapi.models.create_checkout_session_request import CreateCheckoutSessionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCheckoutSessionRequest from a JSON string
create_checkout_session_request_instance = CreateCheckoutSessionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateCheckoutSessionRequest.to_json())

# convert the object into a dict
create_checkout_session_request_dict = create_checkout_session_request_instance.to_dict()
# create an instance of CreateCheckoutSessionRequest from a dict
create_checkout_session_request_from_dict = CreateCheckoutSessionRequest.from_dict(create_checkout_session_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


