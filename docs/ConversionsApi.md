# openapi_client.ConversionsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**convert_id2_png_v2_convertid2png_post**](ConversionsApi.md#convert_id2_png_v2_convertid2png_post) | **POST** /v2/convertid2png | Convert Id 2 Png
[**convert_owm2_json_v2_convertowm2json_post**](ConversionsApi.md#convert_owm2_json_v2_convertowm2json_post) | **POST** /v2/convertowm2json | Convert Owm 2 Json
[**convert_owm2_png_v2_convertowm2png_post**](ConversionsApi.md#convert_owm2_png_v2_convertowm2png_post) | **POST** /v2/convertowm2png | Convert Owm 2 Png
[**convert_owm2_svg_v2_convertowm2svg_post**](ConversionsApi.md#convert_owm2_svg_v2_convertowm2svg_post) | **POST** /v2/convertowm2svg | Convert Owm 2 Svg
[**convert_owm2_toml_v2_convertowm2toml_post**](ConversionsApi.md#convert_owm2_toml_v2_convertowm2toml_post) | **POST** /v2/convertowm2toml | Convert Owm 2 Toml
[**convert_owm2_yaml_v2_convertowm2yaml_post**](ConversionsApi.md#convert_owm2_yaml_v2_convertowm2yaml_post) | **POST** /v2/convertowm2yaml | Convert Owm 2 Yaml


# **convert_id2_png_v2_convertid2png_post**
> bool, date, datetime, dict, float, int, list, str, none_type convert_id2_png_v2_convertid2png_post(map_id_request)

Convert Id 2 Png

API endpoint to generate a Wardley Map image from map_id.  :param request: The request body containing the map_id. :return: JSONResponse with the image URL.

### Example


```python
import time
import openapi_client
from openapi_client.api import conversions_api
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
    api_instance = conversions_api.ConversionsApi(api_client)
    map_id_request = MapIdRequest(
        map_id="map_id_example",
    ) # MapIdRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Convert Id 2 Png
        api_response = api_instance.convert_id2_png_v2_convertid2png_post(map_id_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ConversionsApi->convert_id2_png_v2_convertid2png_post: %s\n" % e)
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

# **convert_owm2_json_v2_convertowm2json_post**
> bool, date, datetime, dict, float, int, list, str, none_type convert_owm2_json_v2_convertowm2json_post(owm_text_request)

Convert Owm 2 Json

API endpoint to convert Wardley Map text to JSON format.  :param request: The request body containing the owmtext. :return: JSONResponse with the JSON representation of the Wardley Map.

### Example


```python
import time
import openapi_client
from openapi_client.api import conversions_api
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
    api_instance = conversions_api.ConversionsApi(api_client)
    owm_text_request = OwmTextRequest(
        owmtext="owmtext_example",
    ) # OwmTextRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Convert Owm 2 Json
        api_response = api_instance.convert_owm2_json_v2_convertowm2json_post(owm_text_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ConversionsApi->convert_owm2_json_v2_convertowm2json_post: %s\n" % e)
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

# **convert_owm2_png_v2_convertowm2png_post**
> bool, date, datetime, dict, float, int, list, str, none_type convert_owm2_png_v2_convertowm2png_post(owm_text_request)

Convert Owm 2 Png

API endpoint to generate a Wardley Map image from text.  :param request: The request body containing the owmtext. :return: JSONResponse with the image URL.

### Example


```python
import time
import openapi_client
from openapi_client.api import conversions_api
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
    api_instance = conversions_api.ConversionsApi(api_client)
    owm_text_request = OwmTextRequest(
        owmtext="owmtext_example",
    ) # OwmTextRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Convert Owm 2 Png
        api_response = api_instance.convert_owm2_png_v2_convertowm2png_post(owm_text_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ConversionsApi->convert_owm2_png_v2_convertowm2png_post: %s\n" % e)
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

# **convert_owm2_svg_v2_convertowm2svg_post**
> bool, date, datetime, dict, float, int, list, str, none_type convert_owm2_svg_v2_convertowm2svg_post(owm_text_request)

Convert Owm 2 Svg

API endpoint to generate a Wardley Map SVG from text.  :param request: The request body containing the owmtext. :return: JSONResponse with the SVG image URL.

### Example


```python
import time
import openapi_client
from openapi_client.api import conversions_api
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
    api_instance = conversions_api.ConversionsApi(api_client)
    owm_text_request = OwmTextRequest(
        owmtext="owmtext_example",
    ) # OwmTextRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Convert Owm 2 Svg
        api_response = api_instance.convert_owm2_svg_v2_convertowm2svg_post(owm_text_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ConversionsApi->convert_owm2_svg_v2_convertowm2svg_post: %s\n" % e)
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

# **convert_owm2_toml_v2_convertowm2toml_post**
> bool, date, datetime, dict, float, int, list, str, none_type convert_owm2_toml_v2_convertowm2toml_post(owm_text_request)

Convert Owm 2 Toml

API endpoint to convert Wardley Map text to TOML format.  :param request: The request body containing the owmtext. :return: JSONResponse with the TOML representation of the Wardley Map.

### Example


```python
import time
import openapi_client
from openapi_client.api import conversions_api
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
    api_instance = conversions_api.ConversionsApi(api_client)
    owm_text_request = OwmTextRequest(
        owmtext="owmtext_example",
    ) # OwmTextRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Convert Owm 2 Toml
        api_response = api_instance.convert_owm2_toml_v2_convertowm2toml_post(owm_text_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ConversionsApi->convert_owm2_toml_v2_convertowm2toml_post: %s\n" % e)
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

# **convert_owm2_yaml_v2_convertowm2yaml_post**
> bool, date, datetime, dict, float, int, list, str, none_type convert_owm2_yaml_v2_convertowm2yaml_post(owm_text_request)

Convert Owm 2 Yaml

API endpoint to convert Wardley Map text to YAML format.  :param request: The request body containing the owmtext. :return: JSONResponse with the YAML representation of the Wardley Map.

### Example


```python
import time
import openapi_client
from openapi_client.api import conversions_api
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
    api_instance = conversions_api.ConversionsApi(api_client)
    owm_text_request = OwmTextRequest(
        owmtext="owmtext_example",
    ) # OwmTextRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Convert Owm 2 Yaml
        api_response = api_instance.convert_owm2_yaml_v2_convertowm2yaml_post(owm_text_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ConversionsApi->convert_owm2_yaml_v2_convertowm2yaml_post: %s\n" % e)
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

