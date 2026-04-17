# ksapi.UsersApi

All URIs are relative to *http://localhost:8000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_me**](UsersApi.md#get_me) | **GET** /v1/users/me | Get Me Handler
[**update_me**](UsersApi.md#update_me) | **PATCH** /v1/users | Update Me Handler


# **get_me**
> UserResponse get_me(authorization=authorization, ks_uat=ks_uat)

Get Me Handler

Get current user information including current tenant context.

Returns the authenticated user's profile along with their current tenant ID
(from the UAT token) and default tenant ID (from user record).

### Example


```python
import ksapi
from ksapi.models.user_response import UserResponse
from ksapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:8000
# See configuration.py for a list of all supported configuration parameters.
configuration = ksapi.Configuration(
    host = "http://localhost:8000"
)


# Enter a context with an instance of the API client
with ksapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ksapi.UsersApi(api_client)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Get Me Handler
        api_response = api_instance.get_me(authorization=authorization, ks_uat=ks_uat)
        print("The response of UsersApi->get_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->get_me: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**UserResponse**](UserResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_me**
> UserResponse update_me(update_user_request, authorization=authorization, ks_uat=ks_uat)

Update Me Handler

Update the user's profile (default tenant, name fields).

When updating default_tenant_id, the user must belong to the specified tenant.

### Example


```python
import ksapi
from ksapi.models.update_user_request import UpdateUserRequest
from ksapi.models.user_response import UserResponse
from ksapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:8000
# See configuration.py for a list of all supported configuration parameters.
configuration = ksapi.Configuration(
    host = "http://localhost:8000"
)


# Enter a context with an instance of the API client
with ksapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ksapi.UsersApi(api_client)
    update_user_request = ksapi.UpdateUserRequest() # UpdateUserRequest | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Update Me Handler
        api_response = api_instance.update_me(update_user_request, authorization=authorization, ks_uat=ks_uat)
        print("The response of UsersApi->update_me:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->update_me: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **update_user_request** | [**UpdateUserRequest**](UpdateUserRequest.md)|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**UserResponse**](UserResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

