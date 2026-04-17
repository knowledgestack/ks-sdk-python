# ksapi.WorkflowDefinitionsApi

All URIs are relative to *http://localhost:8000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_workflow_definition**](WorkflowDefinitionsApi.md#create_workflow_definition) | **POST** /v1/workflow-definitions | Create Workflow Definition Handler
[**delete_workflow_definition**](WorkflowDefinitionsApi.md#delete_workflow_definition) | **DELETE** /v1/workflow-definitions/{definition_id} | Delete Workflow Definition Handler
[**get_workflow_definition**](WorkflowDefinitionsApi.md#get_workflow_definition) | **GET** /v1/workflow-definitions/{definition_id} | Get Workflow Definition Handler
[**invoke_workflow**](WorkflowDefinitionsApi.md#invoke_workflow) | **POST** /v1/workflow-definitions/{definition_id}/invoke | Invoke Workflow Handler
[**list_workflow_definitions**](WorkflowDefinitionsApi.md#list_workflow_definitions) | **GET** /v1/workflow-definitions | List Workflow Definitions Handler
[**list_workflow_runs**](WorkflowDefinitionsApi.md#list_workflow_runs) | **GET** /v1/workflow-definitions/{definition_id}/runs | List Workflow Runs Handler
[**update_workflow_definition**](WorkflowDefinitionsApi.md#update_workflow_definition) | **PUT** /v1/workflow-definitions/{definition_id} | Update Workflow Definition Handler


# **create_workflow_definition**
> WorkflowDefinitionResponse create_workflow_definition(create_workflow_definition_request, authorization=authorization, ks_uat=ks_uat)

Create Workflow Definition Handler

### Example


```python
import ksapi
from ksapi.models.create_workflow_definition_request import CreateWorkflowDefinitionRequest
from ksapi.models.workflow_definition_response import WorkflowDefinitionResponse
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
    api_instance = ksapi.WorkflowDefinitionsApi(api_client)
    create_workflow_definition_request = ksapi.CreateWorkflowDefinitionRequest() # CreateWorkflowDefinitionRequest | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Create Workflow Definition Handler
        api_response = api_instance.create_workflow_definition(create_workflow_definition_request, authorization=authorization, ks_uat=ks_uat)
        print("The response of WorkflowDefinitionsApi->create_workflow_definition:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowDefinitionsApi->create_workflow_definition: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_workflow_definition_request** | [**CreateWorkflowDefinitionRequest**](CreateWorkflowDefinitionRequest.md)|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**WorkflowDefinitionResponse**](WorkflowDefinitionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_workflow_definition**
> delete_workflow_definition(definition_id, authorization=authorization, ks_uat=ks_uat)

Delete Workflow Definition Handler

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
    api_instance = ksapi.WorkflowDefinitionsApi(api_client)
    definition_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Delete Workflow Definition Handler
        api_instance.delete_workflow_definition(definition_id, authorization=authorization, ks_uat=ks_uat)
    except Exception as e:
        print("Exception when calling WorkflowDefinitionsApi->delete_workflow_definition: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **definition_id** | **UUID**|  | 
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

# **get_workflow_definition**
> WorkflowDefinitionResponse get_workflow_definition(definition_id, authorization=authorization, ks_uat=ks_uat)

Get Workflow Definition Handler

### Example


```python
import ksapi
from ksapi.models.workflow_definition_response import WorkflowDefinitionResponse
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
    api_instance = ksapi.WorkflowDefinitionsApi(api_client)
    definition_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Get Workflow Definition Handler
        api_response = api_instance.get_workflow_definition(definition_id, authorization=authorization, ks_uat=ks_uat)
        print("The response of WorkflowDefinitionsApi->get_workflow_definition:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowDefinitionsApi->get_workflow_definition: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **definition_id** | **UUID**|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**WorkflowDefinitionResponse**](WorkflowDefinitionResponse.md)

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

# **invoke_workflow**
> WorkflowRunResponse invoke_workflow(definition_id, invoke_workflow_request, authorization=authorization, ks_uat=ks_uat)

Invoke Workflow Handler

### Example


```python
import ksapi
from ksapi.models.invoke_workflow_request import InvokeWorkflowRequest
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
    api_instance = ksapi.WorkflowDefinitionsApi(api_client)
    definition_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    invoke_workflow_request = ksapi.InvokeWorkflowRequest() # InvokeWorkflowRequest | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Invoke Workflow Handler
        api_response = api_instance.invoke_workflow(definition_id, invoke_workflow_request, authorization=authorization, ks_uat=ks_uat)
        print("The response of WorkflowDefinitionsApi->invoke_workflow:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowDefinitionsApi->invoke_workflow: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **definition_id** | **UUID**|  | 
 **invoke_workflow_request** | [**InvokeWorkflowRequest**](InvokeWorkflowRequest.md)|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**WorkflowRunResponse**](WorkflowRunResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_workflow_definitions**
> PaginatedResponseWorkflowDefinitionResponse list_workflow_definitions(limit=limit, offset=offset, authorization=authorization, ks_uat=ks_uat)

List Workflow Definitions Handler

### Example


```python
import ksapi
from ksapi.models.paginated_response_workflow_definition_response import PaginatedResponseWorkflowDefinitionResponse
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
    api_instance = ksapi.WorkflowDefinitionsApi(api_client)
    limit = 20 # int | Number of items per page (optional) (default to 20)
    offset = 0 # int | Number of items to skip (optional) (default to 0)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # List Workflow Definitions Handler
        api_response = api_instance.list_workflow_definitions(limit=limit, offset=offset, authorization=authorization, ks_uat=ks_uat)
        print("The response of WorkflowDefinitionsApi->list_workflow_definitions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowDefinitionsApi->list_workflow_definitions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of items per page | [optional] [default to 20]
 **offset** | **int**| Number of items to skip | [optional] [default to 0]
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**PaginatedResponseWorkflowDefinitionResponse**](PaginatedResponseWorkflowDefinitionResponse.md)

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

# **list_workflow_runs**
> PaginatedResponseWorkflowRunResponse list_workflow_runs(definition_id, limit=limit, offset=offset, authorization=authorization, ks_uat=ks_uat)

List Workflow Runs Handler

### Example


```python
import ksapi
from ksapi.models.paginated_response_workflow_run_response import PaginatedResponseWorkflowRunResponse
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
    api_instance = ksapi.WorkflowDefinitionsApi(api_client)
    definition_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    limit = 20 # int | Number of items per page (optional) (default to 20)
    offset = 0 # int | Number of items to skip (optional) (default to 0)
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # List Workflow Runs Handler
        api_response = api_instance.list_workflow_runs(definition_id, limit=limit, offset=offset, authorization=authorization, ks_uat=ks_uat)
        print("The response of WorkflowDefinitionsApi->list_workflow_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowDefinitionsApi->list_workflow_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **definition_id** | **UUID**|  | 
 **limit** | **int**| Number of items per page | [optional] [default to 20]
 **offset** | **int**| Number of items to skip | [optional] [default to 0]
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**PaginatedResponseWorkflowRunResponse**](PaginatedResponseWorkflowRunResponse.md)

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

# **update_workflow_definition**
> WorkflowDefinitionResponse update_workflow_definition(definition_id, update_workflow_definition_request, authorization=authorization, ks_uat=ks_uat)

Update Workflow Definition Handler

### Example


```python
import ksapi
from ksapi.models.update_workflow_definition_request import UpdateWorkflowDefinitionRequest
from ksapi.models.workflow_definition_response import WorkflowDefinitionResponse
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
    api_instance = ksapi.WorkflowDefinitionsApi(api_client)
    definition_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    update_workflow_definition_request = ksapi.UpdateWorkflowDefinitionRequest() # UpdateWorkflowDefinitionRequest | 
    authorization = 'authorization_example' # str |  (optional)
    ks_uat = 'ks_uat_example' # str |  (optional)

    try:
        # Update Workflow Definition Handler
        api_response = api_instance.update_workflow_definition(definition_id, update_workflow_definition_request, authorization=authorization, ks_uat=ks_uat)
        print("The response of WorkflowDefinitionsApi->update_workflow_definition:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowDefinitionsApi->update_workflow_definition: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **definition_id** | **UUID**|  | 
 **update_workflow_definition_request** | [**UpdateWorkflowDefinitionRequest**](UpdateWorkflowDefinitionRequest.md)|  | 
 **authorization** | **str**|  | [optional] 
 **ks_uat** | **str**|  | [optional] 

### Return type

[**WorkflowDefinitionResponse**](WorkflowDefinitionResponse.md)

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

