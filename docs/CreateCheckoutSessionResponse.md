# CreateCheckoutSessionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checkout_url** | **str** |  | 
**session_id** | **str** |  | 

## Example

```python
from ksapi.models.create_checkout_session_response import CreateCheckoutSessionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCheckoutSessionResponse from a JSON string
create_checkout_session_response_instance = CreateCheckoutSessionResponse.from_json(json)
# print the JSON string representation of the object
print(CreateCheckoutSessionResponse.to_json())

# convert the object into a dict
create_checkout_session_response_dict = create_checkout_session_response_instance.to_dict()
# create an instance of CreateCheckoutSessionResponse from a dict
create_checkout_session_response_from_dict = CreateCheckoutSessionResponse.from_dict(create_checkout_session_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


