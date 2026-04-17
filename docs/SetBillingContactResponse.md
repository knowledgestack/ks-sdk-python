# SetBillingContactResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**billing_contact_user_id** | **UUID** |  | 
**billing_contact_group_id** | **UUID** |  | 
**billing_email_resolved** | **str** | The email that will receive invoices after this change. | 

## Example

```python
from ksapi.models.set_billing_contact_response import SetBillingContactResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SetBillingContactResponse from a JSON string
set_billing_contact_response_instance = SetBillingContactResponse.from_json(json)
# print the JSON string representation of the object
print(SetBillingContactResponse.to_json())

# convert the object into a dict
set_billing_contact_response_dict = set_billing_contact_response_instance.to_dict()
# create an instance of SetBillingContactResponse from a dict
set_billing_contact_response_from_dict = SetBillingContactResponse.from_dict(set_billing_contact_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


