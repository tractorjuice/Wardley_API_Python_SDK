# openapi_client.WardleyMapsOnlineApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fetch_wardley_data_v2_maps_fetch_get**](WardleyMapsOnlineApi.md#fetch_wardley_data_v2_maps_fetch_get) | **GET** /v2/maps/fetch | Fetch Wardley Data
[**get_image_v2_image_filename_get**](WardleyMapsOnlineApi.md#get_image_v2_image_filename_get) | **GET** /v2/image/{filename} | Get Image
[**save_wardley_map_v2_maps_save_post**](WardleyMapsOnlineApi.md#save_wardley_map_v2_maps_save_post) | **POST** /v2/maps/save | Save Wardley Map


# **fetch_wardley_data_v2_maps_fetch_get**
> bool, date, datetime, dict, float, int, list, str, none_type fetch_wardley_data_v2_maps_fetch_get(id)

Fetch Wardley Data

API endpoint to fetch a Wardley Map by map_id.  :param map_id: The map ID to fetch. :return: JSONResponse with the map data.

### Example


```python
import time
import openapi_client
from openapi_client.api import wardley_maps_online_api
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
    api_instance = wardley_maps_online_api.WardleyMapsOnlineApi(api_client)
    id = "id_example" # str | The map ID to fetch

    # example passing only required values which don't have defaults set
    try:
        # Fetch Wardley Data
        api_response = api_instance.fetch_wardley_data_v2_maps_fetch_get(id)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling WardleyMapsOnlineApi->fetch_wardley_data_v2_maps_fetch_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| The map ID to fetch |

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

# **get_image_v2_image_filename_get**
> bool, date, datetime, dict, float, int, list, str, none_type get_image_v2_image_filename_get(filename)

Get Image

API endpoint to retrieve an image by filename.  :param filename: The name of the file to retrieve. :return: FileResponse with the image.

### Example


```python
import time
import openapi_client
from openapi_client.api import wardley_maps_online_api
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
    api_instance = wardley_maps_online_api.WardleyMapsOnlineApi(api_client)
    filename = "filename_example" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Get Image
        api_response = api_instance.get_image_v2_image_filename_get(filename)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling WardleyMapsOnlineApi->get_image_v2_image_filename_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filename** | **str**|  |

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

# **save_wardley_map_v2_maps_save_post**
> bool, date, datetime, dict, float, int, list, str, none_type save_wardley_map_v2_maps_save_post(text_request)

Save Wardley Map

API endpoint to save a Wardley Map.  :param request: The request body containing the map data. :return: JSONResponse with the saved map data.

### Example


```python
import time
import openapi_client
from openapi_client.api import wardley_maps_online_api
from openapi_client.model.http_validation_error import HTTPValidationError
from openapi_client.model.text_request import TextRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = wardley_maps_online_api.WardleyMapsOnlineApi(api_client)
    text_request = TextRequest(
        owmtext="owmtext_example",
    ) # TextRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Save Wardley Map
        api_response = api_instance.save_wardley_map_v2_maps_save_post(text_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling WardleyMapsOnlineApi->save_wardley_map_v2_maps_save_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **text_request** | [**TextRequest**](TextRequest.md)|  |

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

