# ksapi.BillingApi

All URIs are relative to *http://localhost:8000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**admin_clear_enterprise_override**](BillingApi.md#admin_clear_enterprise_override) | **DELETE** /v1/billing/admin/tenants/{tenant_id}/overrides | Admin Clear Enterprise Override Handler
[**admin_set_enterprise_override**](BillingApi.md#admin_set_enterprise_override) | **PUT** /v1/billing/admin/tenants/{tenant_id}/overrides | Admin Set Enterprise Override Handler
[**cancel_tenant_subscription**](BillingApi.md#cancel_tenant_subscription) | **POST** /v1/billing/subscription/cancel | Cancel Tenant Subscription Handler
[**create_billing_checkout_session**](BillingApi.md#create_billing_checkout_session) | **POST** /v1/billing/checkout-session | Create Billing Checkout Session Handler
[**create_billing_portal_session**](BillingApi.md#create_billing_portal_session) | **POST** /v1/billing/portal-session | Create Billing Portal Session Handler
[**get_current_user_usage**](BillingApi.md#get_current_user_usage) | **GET** /v1/billing/usage/me | Get Current User Usage Handler
[**get_tenant_subscription**](BillingApi.md#get_tenant_subscription) | **GET** /v1/billing/subscription | Get Tenant Subscription Handler
[**get_tenant_usage**](BillingApi.md#get_tenant_usage) | **GET** /v1/billing/usage | Get Tenant Usage Handler
[**list_billing_plans**](BillingApi.md#list_billing_plans) | **GET** /v1/billing/plans | List Billing Plans Handler
[**resume_tenant_subscription**](BillingApi.md#resume_tenant_subscription) | **POST** /v1/billing/subscription/resume | Resume Tenant Subscription Handler
[**set_billing_contact**](BillingApi.md#set_billing_contact) | **PUT** /v1/billing/billing-contact | Set Billing Contact Handler


# **admin_clear_enterprise_override**
> TenantSubscriptionResponse admin_clear_enterprise_override(tenant_id, x_ks_platform_admin_key=x_ks_platform_admin_key)

Admin Clear Enterprise Override Handler

Clear all enterprise overrides for a tenant (contract ended).

### Example


```python
import ksapi
from ksapi.models.tenant_subscription_response import TenantSubscriptionResponse
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
    api_instance = ksapi.BillingApi(api_client)
    tenant_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    x_ks_platform_admin_key = 'x_ks_platform_admin_key_example' # str |  (optional)

    try:
        # Admin Clear Enterprise Override Handler
        api_response = api_instance.admin_clear_enterprise_override(tenant_id, x_ks_platform_admin_key=x_ks_platform_admin_key)
        print("The response of BillingApi->admin_clear_enterprise_override:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->admin_clear_enterprise_override: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tenant_id** | **UUID**|  | 
 **x_ks_platform_admin_key** | **str**|  | [optional] 

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

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

# **admin_set_enterprise_override**
> TenantSubscriptionResponse admin_set_enterprise_override(tenant_id, set_enterprise_override_request, x_ks_platform_admin_key=x_ks_platform_admin_key)

Admin Set Enterprise Override Handler

Set per-tenant enterprise contract overrides (custom pricing/limits).

### Example


```python
import ksapi
from ksapi.models.set_enterprise_override_request import SetEnterpriseOverrideRequest
from ksapi.models.tenant_subscription_response import TenantSubscriptionResponse
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
    api_instance = ksapi.BillingApi(api_client)
    tenant_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    set_enterprise_override_request = ksapi.SetEnterpriseOverrideRequest() # SetEnterpriseOverrideRequest | 
    x_ks_platform_admin_key = 'x_ks_platform_admin_key_example' # str |  (optional)

    try:
        # Admin Set Enterprise Override Handler
        api_response = api_instance.admin_set_enterprise_override(tenant_id, set_enterprise_override_request, x_ks_platform_admin_key=x_ks_platform_admin_key)
        print("The response of BillingApi->admin_set_enterprise_override:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->admin_set_enterprise_override: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tenant_id** | **UUID**|  | 
 **set_enterprise_override_request** | [**SetEnterpriseOverrideRequest**](SetEnterpriseOverrideRequest.md)|  | 
 **x_ks_platform_admin_key** | **str**|  | [optional] 

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

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

# **cancel_tenant_subscription**
> TenantSubscriptionResponse cancel_tenant_subscription(authorization=authorization, ks_uat=ks_uat)

Cancel Tenant Subscription Handler

Cancel subscription at end of current period.

### Example


```python
import ksapi
from ksapi.models.tenant_subscription_response import TenantSubscriptionResponse
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
    api_instance = ksapi.BillingApi(api_client)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Cancel Tenant Subscription Handler
        api_response = api_instance.cancel_tenant_subscription(authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->cancel_tenant_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->cancel_tenant_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

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

# **create_billing_checkout_session**
> CreateCheckoutSessionResponse create_billing_checkout_session(create_checkout_session_request, authorization=authorization, ks_uat=ks_uat)

Create Billing Checkout Session Handler

Create a Stripe Checkout session for upgrading to a paid plan.

### Example


```python
import ksapi
from ksapi.models.create_checkout_session_request import CreateCheckoutSessionRequest
from ksapi.models.create_checkout_session_response import CreateCheckoutSessionResponse
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
    api_instance = ksapi.BillingApi(api_client)
    create_checkout_session_request = ksapi.CreateCheckoutSessionRequest() # CreateCheckoutSessionRequest | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Create Billing Checkout Session Handler
        api_response = api_instance.create_billing_checkout_session(create_checkout_session_request, authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->create_billing_checkout_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->create_billing_checkout_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_checkout_session_request** | [**CreateCheckoutSessionRequest**](CreateCheckoutSessionRequest.md)|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**CreateCheckoutSessionResponse**](CreateCheckoutSessionResponse.md)

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

# **create_billing_portal_session**
> CreatePortalSessionResponse create_billing_portal_session(create_portal_session_request, authorization=authorization, ks_uat=ks_uat)

Create Billing Portal Session Handler

Create a Stripe billing portal session (manage payment method, cancel).

### Example


```python
import ksapi
from ksapi.models.create_portal_session_request import CreatePortalSessionRequest
from ksapi.models.create_portal_session_response import CreatePortalSessionResponse
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
    api_instance = ksapi.BillingApi(api_client)
    create_portal_session_request = ksapi.CreatePortalSessionRequest() # CreatePortalSessionRequest | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Create Billing Portal Session Handler
        api_response = api_instance.create_billing_portal_session(create_portal_session_request, authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->create_billing_portal_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->create_billing_portal_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_portal_session_request** | [**CreatePortalSessionRequest**](CreatePortalSessionRequest.md)|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**CreatePortalSessionResponse**](CreatePortalSessionResponse.md)

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

# **get_current_user_usage**
> UserUsageResponse get_current_user_usage(authorization=authorization, ks_uat=ks_uat)

Get Current User Usage Handler

Current user's own usage for this period (any authenticated user).

### Example


```python
import ksapi
from ksapi.models.user_usage_response import UserUsageResponse
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
    api_instance = ksapi.BillingApi(api_client)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Get Current User Usage Handler
        api_response = api_instance.get_current_user_usage(authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->get_current_user_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_current_user_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**UserUsageResponse**](UserUsageResponse.md)

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

# **get_tenant_subscription**
> TenantSubscriptionResponse get_tenant_subscription(authorization=authorization, ks_uat=ks_uat)

Get Tenant Subscription Handler

Fetch the tenant's current subscription (any authenticated user).

### Example


```python
import ksapi
from ksapi.models.tenant_subscription_response import TenantSubscriptionResponse
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
    api_instance = ksapi.BillingApi(api_client)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Get Tenant Subscription Handler
        api_response = api_instance.get_tenant_subscription(authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->get_tenant_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_tenant_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

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

# **get_tenant_usage**
> TenantUsageResponse get_tenant_usage(authorization=authorization, ks_uat=ks_uat)

Get Tenant Usage Handler

Tenant-wide usage (any authenticated tenant member).

Not admin-gated: the cap is a shared resource, so every team member
needs to see how close they are to it. No PII or money values are
exposed — just counters and percentages.

### Example


```python
import ksapi
from ksapi.models.tenant_usage_response import TenantUsageResponse
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
    api_instance = ksapi.BillingApi(api_client)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Get Tenant Usage Handler
        api_response = api_instance.get_tenant_usage(authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->get_tenant_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_tenant_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**TenantUsageResponse**](TenantUsageResponse.md)

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

# **list_billing_plans**
> List[BillingPlanResponse] list_billing_plans(authorization=authorization, ks_uat=ks_uat)

List Billing Plans Handler

List all active plans. Any authenticated user can see the catalog.

### Example


```python
import ksapi
from ksapi.models.billing_plan_response import BillingPlanResponse
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
    api_instance = ksapi.BillingApi(api_client)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # List Billing Plans Handler
        api_response = api_instance.list_billing_plans(authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->list_billing_plans:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->list_billing_plans: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**List[BillingPlanResponse]**](BillingPlanResponse.md)

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

# **resume_tenant_subscription**
> TenantSubscriptionResponse resume_tenant_subscription(authorization=authorization, ks_uat=ks_uat)

Resume Tenant Subscription Handler

Undo a prior cancel-at-period-end request.

### Example


```python
import ksapi
from ksapi.models.tenant_subscription_response import TenantSubscriptionResponse
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
    api_instance = ksapi.BillingApi(api_client)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Resume Tenant Subscription Handler
        api_response = api_instance.resume_tenant_subscription(authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->resume_tenant_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->resume_tenant_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

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

# **set_billing_contact**
> SetBillingContactResponse set_billing_contact(set_billing_contact_request, authorization=authorization, ks_uat=ks_uat)

Set Billing Contact Handler

Set the billing contact for invoice delivery.

Pass a ``user_id`` to send invoices to a specific user's email,
or a ``group_id`` to send to a group's email (the group must have
an email configured). Pass both as ``null`` to revert to the tenant
owner's email (default). Only OWNER or ADMIN can change this.

### Example


```python
import ksapi
from ksapi.models.set_billing_contact_request import SetBillingContactRequest
from ksapi.models.set_billing_contact_response import SetBillingContactResponse
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
    api_instance = ksapi.BillingApi(api_client)
    set_billing_contact_request = ksapi.SetBillingContactRequest() # SetBillingContactRequest | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Set Billing Contact Handler
        api_response = api_instance.set_billing_contact(set_billing_contact_request, authorization=authorization, ks_uat=ks_uat)
        print("The response of BillingApi->set_billing_contact:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->set_billing_contact: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **set_billing_contact_request** | [**SetBillingContactRequest**](SetBillingContactRequest.md)|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**SetBillingContactResponse**](SetBillingContactResponse.md)

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

