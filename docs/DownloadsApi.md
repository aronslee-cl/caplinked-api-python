# caplinked.DownloadsApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_downloads_id**](DownloadsApi.md#delete_downloads_id) | **DELETE** /downloads/{id} | Delete download
[**get_downloads_file_file_id**](DownloadsApi.md#get_downloads_file_file_id) | **GET** /downloads/file/{file_id} | Get single file
[**get_downloads_id**](DownloadsApi.md#get_downloads_id) | **GET** /downloads/{id} | Get zip
[**get_downloads_status_workspace_id**](DownloadsApi.md#get_downloads_status_workspace_id) | **GET** /downloads/status/{workspace_id} | Get status of downloads for current user
[**post_downloads**](DownloadsApi.md#post_downloads) | **POST** /downloads | Create zip file


# **delete_downloads_id**
> Delete delete_downloads_id(id, workspace_id)

Delete download

Delete download

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.DownloadsApi()
id = 56 # int | ID of download to delete
workspace_id = 56 # int | ID of Workspace

try: 
    # Delete download
    api_response = api_instance.delete_downloads_id(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DownloadsApi->delete_downloads_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of download to delete | 
 **workspace_id** | **int**| ID of Workspace | 

### Return type

[**Delete**](Delete.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_downloads_file_file_id**
> ExpiringUrl get_downloads_file_file_id(file_id, workspace_id)

Get single file

Download single file without DRM applied

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.DownloadsApi()
file_id = 56 # int | ID of file to download
workspace_id = 56 # int | ID of Workspace

try: 
    # Get single file
    api_response = api_instance.get_downloads_file_file_id(file_id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DownloadsApi->get_downloads_file_file_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_id** | **int**| ID of file to download | 
 **workspace_id** | **int**| ID of Workspace | 

### Return type

[**ExpiringUrl**](ExpiringUrl.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_downloads_id**
> ExpiringUrl get_downloads_id(id, workspace_id)

Get zip

Get a zip file of a previously created download object

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.DownloadsApi()
id = 56 # int | ID of download
workspace_id = 56 # int | ID of Workspace

try: 
    # Get zip
    api_response = api_instance.get_downloads_id(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DownloadsApi->get_downloads_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of download | 
 **workspace_id** | **int**| ID of Workspace | 

### Return type

[**ExpiringUrl**](ExpiringUrl.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_downloads_status_workspace_id**
> Meta get_downloads_status_workspace_id(workspace_id)

Get status of downloads for current user

Get status of downloads created by current user within a specified workspace

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.DownloadsApi()
workspace_id = 56 # int | ID of Workspace

try: 
    # Get status of downloads for current user
    api_response = api_instance.get_downloads_status_workspace_id(workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DownloadsApi->get_downloads_status_workspace_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**| ID of Workspace | 

### Return type

[**Meta**](Meta.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_downloads**
> Meta post_downloads(workspace_id, download_folder_ids=download_folder_ids, download_file_ids=download_file_ids)

Create zip file

Create download object containing folders and/or files

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.DownloadsApi()
workspace_id = 56 # int | ID of Workspace
download_folder_ids = [56] # list[int] | IDs of folders to include in download (optional)
download_file_ids = [56] # list[int] | IDs of files to include in download (optional)

try: 
    # Create zip file
    api_response = api_instance.post_downloads(workspace_id, download_folder_ids=download_folder_ids, download_file_ids=download_file_ids)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DownloadsApi->post_downloads: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**| ID of Workspace | 
 **download_folder_ids** | [**list[int]**](int.md)| IDs of folders to include in download | [optional] 
 **download_file_ids** | [**list[int]**](int.md)| IDs of files to include in download | [optional] 

### Return type

[**Meta**](Meta.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

