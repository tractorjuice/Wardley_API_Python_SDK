# openapi_client.ToolsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_github_map_v2_get_github_map_get**](ToolsApi.md#get_github_map_v2_get_github_map_get) | **GET** /v2/get-github-map | Get Github Map
[**list_github_maps_v2_list_github_maps_get**](ToolsApi.md#list_github_maps_v2_list_github_maps_get) | **GET** /v2/list-github-maps | List Github Maps
[**open_map_v2_openmap_get**](ToolsApi.md#open_map_v2_openmap_get) | **GET** /v2/openmap | Open Map
[**privacy_statement_v2_privacy_get**](ToolsApi.md#privacy_statement_v2_privacy_get) | **GET** /v2/privacy | Privacy Statement


# **get_github_map_v2_get_github_map_get**
> MapTextAndWarnings get_github_map_v2_get_github_map_get(github_path)

Get Github Map

API endpoint to get the content of a file in the GitHub repository and return warnings.  :param github_path: Full path of the file to retrieve. :return: Content of the file and warnings.

### Example


```python
import time
import openapi_client
from openapi_client.api import tools_api
from openapi_client.model.map_text_and_warnings import MapTextAndWarnings
from openapi_client.model.http_validation_error import HTTPValidationError
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = tools_api.ToolsApi(api_client)
    github_path = "github_path_example" # str | The full path of the file to retrieve

    # example passing only required values which don't have defaults set
    try:
        # Get Github Map
        api_response = api_instance.get_github_map_v2_get_github_map_get(github_path)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ToolsApi->get_github_map_v2_get_github_map_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **github_path** | **str**| The full path of the file to retrieve |

### Return type

[**MapTextAndWarnings**](MapTextAndWarnings.md)

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

# **list_github_maps_v2_list_github_maps_get**
> [str] list_github_maps_v2_list_github_maps_get()

List Github Maps

API endpoint to list all relevant files in the GitHub repository.  :return: List of file paths.

### Example


```python
import time
import openapi_client
from openapi_client.api import tools_api
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = tools_api.ToolsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # List Github Maps
        api_response = api_instance.list_github_maps_v2_list_github_maps_get()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ToolsApi->list_github_maps_v2_list_github_maps_get: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

**[str]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **open_map_v2_openmap_get**
> bool, date, datetime, dict, float, int, list, str, none_type open_map_v2_openmap_get(url)

Open Map

API endpoint to open a Wardley Map from a GitHub URL.  :param url: The GitHub URL of the Wardley Map. :return: RedirectResponse to the edit URL of the saved map.

### Example


```python
import time
import openapi_client
from openapi_client.api import tools_api
from openapi_client.model.http_validation_error import HTTPValidationError
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = tools_api.ToolsApi(api_client)
    url = "url_example" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Open Map
        api_response = api_instance.open_map_v2_openmap_get(url)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ToolsApi->open_map_v2_openmap_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **url** | **str**|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **privacy_statement_v2_privacy_get**
> str privacy_statement_v2_privacy_get()

Privacy Statement

API endpoint to provide the privacy statement.  :return: The privacy statement as a string.

### Example


```python
import time
import openapi_client
from openapi_client.api import tools_api
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = tools_api.ToolsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Privacy Statement
        api_response = api_instance.privacy_statement_v2_privacy_get()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ToolsApi->privacy_statement_v2_privacy_get: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

