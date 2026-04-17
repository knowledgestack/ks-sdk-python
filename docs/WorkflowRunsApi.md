# ksapi.WorkflowRunsApi

All URIs are relative to *http://localhost:8000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_workflow_run**](WorkflowRunsApi.md#delete_workflow_run) | **DELETE** /v1/workflow-runs/{run_id} | Delete Workflow Run Handler
[**get_workflow_run**](WorkflowRunsApi.md#get_workflow_run) | **GET** /v1/workflow-runs/{run_id} | Get Workflow Run Handler
[**workflow_run_callback**](WorkflowRunsApi.md#workflow_run_callback) | **POST** /v1/workflow-runs/{run_id}/callback | Workflow Run Callback Handler


# **delete_workflow_run**
> delete_workflow_run(run_id, authorization=authorization, ks_uat=ks_uat)

Delete Workflow Run Handler

### Example


```python
import ksapi
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
    api_instance = ksapi.WorkflowRunsApi(api_client)
    run_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Delete Workflow Run Handler
        api_instance.delete_workflow_run(run_id, authorization=authorization, ks_uat=ks_uat)
    except Exception as e:
        print("Exception when calling WorkflowRunsApi->delete_workflow_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_id** | **UUID**|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workflow_run**
> WorkflowRunResponse get_workflow_run(run_id, authorization=authorization, ks_uat=ks_uat)

Get Workflow Run Handler

### Example


```python
import ksapi
from ksapi.models.workflow_run_response import WorkflowRunResponse
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
    api_instance = ksapi.WorkflowRunsApi(api_client)
    run_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Get Workflow Run Handler
        api_response = api_instance.get_workflow_run(run_id, authorization=authorization, ks_uat=ks_uat)
        print("The response of WorkflowRunsApi->get_workflow_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowRunsApi->get_workflow_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_id** | **UUID**|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**WorkflowRunResponse**](WorkflowRunResponse.md)

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

# **workflow_run_callback**
> WorkflowCallbackResponse workflow_run_callback(run_id, workflow_run_callback_request)

Workflow Run Callback Handler

### Example


```python
import ksapi
from ksapi.models.workflow_callback_response import WorkflowCallbackResponse
from ksapi.models.workflow_run_callback_request import WorkflowRunCallbackRequest
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
    api_instance = ksapi.WorkflowRunsApi(api_client)
    run_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    workflow_run_callback_request = ksapi.WorkflowRunCallbackRequest() # WorkflowRunCallbackRequest | 

    try:
        # Workflow Run Callback Handler
        api_response = api_instance.workflow_run_callback(run_id, workflow_run_callback_request)
        print("The response of WorkflowRunsApi->workflow_run_callback:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowRunsApi->workflow_run_callback: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_id** | **UUID**|  | 
 **workflow_run_callback_request** | [**WorkflowRunCallbackRequest**](WorkflowRunCallbackRequest.md)|  | 

### Return type

[**WorkflowCallbackResponse**](WorkflowCallbackResponse.md)

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

