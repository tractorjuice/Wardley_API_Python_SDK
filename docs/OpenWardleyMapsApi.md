# openapi_client.OpenWardleyMapsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generate_map_from_id_v2_generate_mapfromid_post**](OpenWardleyMapsApi.md#generate_map_from_id_v2_generate_mapfromid_post) | **POST** /v2/generate-mapfromid | Generate Map From Id
[**generate_map_from_text_v2_generate_mapfromtext_post**](OpenWardleyMapsApi.md#generate_map_from_text_v2_generate_mapfromtext_post) | **POST** /v2/generate-mapfromtext | Generate Map From Text
[**generate_svg_map_v2_generate_svgmap_post**](OpenWardleyMapsApi.md#generate_svg_map_v2_generate_svgmap_post) | **POST** /v2/generate-svgmap | Generate Svg Map
[**get_owm_anchors_v2_get_owm_anchors_post**](OpenWardleyMapsApi.md#get_owm_anchors_v2_get_owm_anchors_post) | **POST** /v2/get-owm-anchors | Get Owm Anchors
[**get_owm_annotations_v2_get_owm_annotations_post**](OpenWardleyMapsApi.md#get_owm_annotations_v2_get_owm_annotations_post) | **POST** /v2/get-owm-annotations | Get Owm Annotations
[**get_owm_component_v2_get_owm_component_post**](OpenWardleyMapsApi.md#get_owm_component_v2_get_owm_component_post) | **POST** /v2/get-owm-component | Get Owm Component
[**get_owm_components_v2_get_owm_components_post**](OpenWardleyMapsApi.md#get_owm_components_v2_get_owm_components_post) | **POST** /v2/get-owm-components | Get Owm Components
[**get_owm_map_text_v2_get_owm_text_post**](OpenWardleyMapsApi.md#get_owm_map_text_v2_get_owm_text_post) | **POST** /v2/get-owm-text | Get Owm Map Text
[**get_owm_notes_v2_get_owm_notes_post**](OpenWardleyMapsApi.md#get_owm_notes_v2_get_owm_notes_post) | **POST** /v2/get-owm-notes | Get Owm Notes
[**get_owm_pipelines_v2_get_owm_pipelines_post**](OpenWardleyMapsApi.md#get_owm_pipelines_v2_get_owm_pipelines_post) | **POST** /v2/get-owm-pipelines | Get Owm Pipelines
[**get_owm_warnings_v2_get_owm_warnings_post**](OpenWardleyMapsApi.md#get_owm_warnings_v2_get_owm_warnings_post) | **POST** /v2/get-owm-warnings | Get Owm Warnings
[**search_owm_components_v2_search_owm_components_post**](OpenWardleyMapsApi.md#search_owm_components_v2_search_owm_components_post) | **POST** /v2/search-owm-components | Search Owm Components


# **generate_map_from_id_v2_generate_mapfromid_post**
> bool, date, datetime, dict, float, int, list, str, none_type generate_map_from_id_v2_generate_mapfromid_post(map_id_request)

Generate Map From Id

API endpoint to generate a Wardley Map image from map_id.  :param request: The request body containing the map_id. :return: JSONResponse with the image URL.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.map_id_request import MapIdRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Generate Map From Id
        api_response = api_instance.generate_map_from_id_v2_generate_mapfromid_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->generate_map_from_id_v2_generate_mapfromid_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map_id_request** | [**MapIdRequest**](MapIdRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **generate_map_from_text_v2_generate_mapfromtext_post**
> bool, date, datetime, dict, float, int, list, str, none_type generate_map_from_text_v2_generate_mapfromtext_post(owm_text_request)

Generate Map From Text

API endpoint to generate a Wardley Map image from text.  :param request: The request body containing the owmtext. :return: JSONResponse with the image URL.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.owm_text_request import OwmTextRequest
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
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    owm_text_request = OwmTextRequest(
        owmtext="owmtext_example",
    ) # OwmTextRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Generate Map From Text
        api_response = api_instance.generate_map_from_text_v2_generate_mapfromtext_post(owm_text_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->generate_map_from_text_v2_generate_mapfromtext_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owm_text_request** | [**OwmTextRequest**](OwmTextRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **generate_svg_map_v2_generate_svgmap_post**
> bool, date, datetime, dict, float, int, list, str, none_type generate_svg_map_v2_generate_svgmap_post(owm_text_request)

Generate Svg Map

API endpoint to generate a Wardley Map SVG from text.  :param request: The request body containing the owmtext. :return: JSONResponse with the SVG image URL.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.owm_text_request import OwmTextRequest
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
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    owm_text_request = OwmTextRequest(
        owmtext="owmtext_example",
    ) # OwmTextRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Generate Svg Map
        api_response = api_instance.generate_svg_map_v2_generate_svgmap_post(owm_text_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->generate_svg_map_v2_generate_svgmap_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owm_text_request** | [**OwmTextRequest**](OwmTextRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **get_owm_anchors_v2_get_owm_anchors_post**
> bool, date, datetime, dict, float, int, list, str, none_type get_owm_anchors_v2_get_owm_anchors_post(map_id_request)

Get Owm Anchors

API endpoint to fetch anchors for a Wardley Map.  :param request: The request body containing the map_id. :return: JSONResponse with the anchors.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.map_id_request import MapIdRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Get Owm Anchors
        api_response = api_instance.get_owm_anchors_v2_get_owm_anchors_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->get_owm_anchors_v2_get_owm_anchors_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map_id_request** | [**MapIdRequest**](MapIdRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **get_owm_annotations_v2_get_owm_annotations_post**
> bool, date, datetime, dict, float, int, list, str, none_type get_owm_annotations_v2_get_owm_annotations_post(map_id_request)

Get Owm Annotations

API endpoint to fetch annotations for a Wardley Map.  :param request: The request body containing the map_id. :return: JSONResponse with the annotations.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.map_id_request import MapIdRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Get Owm Annotations
        api_response = api_instance.get_owm_annotations_v2_get_owm_annotations_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->get_owm_annotations_v2_get_owm_annotations_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map_id_request** | [**MapIdRequest**](MapIdRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **get_owm_component_v2_get_owm_component_post**
> bool, date, datetime, dict, float, int, list, str, none_type get_owm_component_v2_get_owm_component_post(component_request)

Get Owm Component

API endpoint to fetch a specific component for a Wardley Map.  :param request: The request body containing the map_id and component name. :return: JSONResponse with the component.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.component_request import ComponentRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    component_request = ComponentRequest(
        map_id="map_id_example",
        name="name_example",
    ) # ComponentRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Get Owm Component
        api_response = api_instance.get_owm_component_v2_get_owm_component_post(component_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->get_owm_component_v2_get_owm_component_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **component_request** | [**ComponentRequest**](ComponentRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **get_owm_components_v2_get_owm_components_post**
> bool, date, datetime, dict, float, int, list, str, none_type get_owm_components_v2_get_owm_components_post(map_id_request)

Get Owm Components

API endpoint to fetch components for a Wardley Map.  :param request: The request body containing the map_id. :return: JSONResponse with the components.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.map_id_request import MapIdRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Get Owm Components
        api_response = api_instance.get_owm_components_v2_get_owm_components_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->get_owm_components_v2_get_owm_components_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map_id_request** | [**MapIdRequest**](MapIdRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **get_owm_map_text_v2_get_owm_text_post**
> bool, date, datetime, dict, float, int, list, str, none_type get_owm_map_text_v2_get_owm_text_post(map_id_request)

Get Owm Map Text

API endpoint to fetch the text of a Wardley Map.  :param request: The request body containing the map_id. :return: JSONResponse with the map text.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.map_id_request import MapIdRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Get Owm Map Text
        api_response = api_instance.get_owm_map_text_v2_get_owm_text_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->get_owm_map_text_v2_get_owm_text_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map_id_request** | [**MapIdRequest**](MapIdRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **get_owm_notes_v2_get_owm_notes_post**
> bool, date, datetime, dict, float, int, list, str, none_type get_owm_notes_v2_get_owm_notes_post(map_id_request)

Get Owm Notes

API endpoint to fetch notes for a Wardley Map.  :param request: The request body containing the map_id. :return: JSONResponse with the notes.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.map_id_request import MapIdRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Get Owm Notes
        api_response = api_instance.get_owm_notes_v2_get_owm_notes_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->get_owm_notes_v2_get_owm_notes_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map_id_request** | [**MapIdRequest**](MapIdRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **get_owm_pipelines_v2_get_owm_pipelines_post**
> bool, date, datetime, dict, float, int, list, str, none_type get_owm_pipelines_v2_get_owm_pipelines_post(map_id_request)

Get Owm Pipelines

API endpoint to fetch pipelines for a Wardley Map.  :param request: The request body containing the map_id. :return: JSONResponse with the pipelines.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.map_id_request import MapIdRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Get Owm Pipelines
        api_response = api_instance.get_owm_pipelines_v2_get_owm_pipelines_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->get_owm_pipelines_v2_get_owm_pipelines_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map_id_request** | [**MapIdRequest**](MapIdRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **get_owm_warnings_v2_get_owm_warnings_post**
> bool, date, datetime, dict, float, int, list, str, none_type get_owm_warnings_v2_get_owm_warnings_post(map_id_request)

Get Owm Warnings

API endpoint to fetch warnings for a Wardley Map.  :param request: The request body containing the map_id. :return: JSONResponse with the warnings.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.map_id_request import MapIdRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Get Owm Warnings
        api_response = api_instance.get_owm_warnings_v2_get_owm_warnings_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->get_owm_warnings_v2_get_owm_warnings_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map_id_request** | [**MapIdRequest**](MapIdRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

# **search_owm_components_v2_search_owm_components_post**
> bool, date, datetime, dict, float, int, list, str, none_type search_owm_components_v2_search_owm_components_post(search_component_request)

Search Owm Components

API endpoint to search components in a Wardley Map.  :param request: The request body containing the map_id and search term. :return: JSONResponse with the search results.

### Example


```python
import time
import openapi_client
from openapi_client.api import open_wardley_maps_api
from openapi_client.model.search_component_request import SearchComponentRequest
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
    api_instance = open_wardley_maps_api.OpenWardleyMapsApi(api_client)
    search_component_request = SearchComponentRequest(
        map_id="map_id_example",
        search_term="search_term_example",
    ) # SearchComponentRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Search Owm Components
        api_response = api_instance.search_owm_components_v2_search_owm_components_post(search_component_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling OpenWardleyMapsApi->search_owm_components_v2_search_owm_components_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search_component_request** | [**SearchComponentRequest**](SearchComponentRequest.md)|  |

### Return type

**bool, date, datetime, dict, float, int, list, str, none_type**

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

