# SetBillingContactRequest

Set billing contact to a user or group. Pass both as null to revert to owner.  Exactly one of ``user_id`` or ``group_id`` may be set (or both null to clear). If a group is specified, it must already have an email address.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **UUID** | User whose email will receive invoices. | [optional] 
**group_id** | **UUID** | Group whose email will receive invoices (must have email set). | [optional] 

## Example

```python
from ksapi.models.set_billing_contact_request import SetBillingContactRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SetBillingContactRequest from a JSON string
set_billing_contact_request_instance = SetBillingContactRequest.from_json(json)
# print the JSON string representation of the object
print(SetBillingContactRequest.to_json())

# convert the object into a dict
set_billing_contact_request_dict = set_billing_contact_request_instance.to_dict()
# create an instance of SetBillingContactRequest from a dict
set_billing_contact_request_from_dict = SetBillingContactRequest.from_dict(set_billing_contact_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


