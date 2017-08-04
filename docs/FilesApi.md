# caplinked.FilesApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_files_id**](FilesApi.md#delete_files_id) | **DELETE** /files/{id} | Delete file
[**get_files_id**](FilesApi.md#get_files_id) | **GET** /files/{id} | Get file information
[**post_files_id_copy**](FilesApi.md#post_files_id_copy) | **POST** /files/{id}/copy | Copy file
[**post_files_id_move**](FilesApi.md#post_files_id_move) | **POST** /files/{id}/move | Move file
[**put_files_id**](FilesApi.md#put_files_id) | **PUT** /files/{id} | Update file information
[**put_files_upload**](FilesApi.md#put_files_upload) | **PUT** /files/upload | Upload file


# **delete_files_id**
> FileDelete delete_files_id(id, workspace_id)

Delete file

Delete file

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FilesApi()
id = 56 # int | ID of file to delete
workspace_id = 56 # int | ID of workspace

try: 
    # Delete file
    api_response = api_instance.delete_files_id(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FilesApi->delete_files_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of file to delete | 
 **workspace_id** | **int**| ID of workspace | 

### Return type

[**FileDelete**](FileDelete.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_files_id**
> FileInfoMapped get_files_id(id, workspace_id, page_number=page_number)

Get file information

Get file information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FilesApi()
id = 56 # int | ID of file
workspace_id = 56 # int | ID of workspace
page_number = 1 # int | Page number of file (for viewer tokens) (optional) (default to 1)

try: 
    # Get file information
    api_response = api_instance.get_files_id(id, workspace_id, page_number=page_number)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FilesApi->get_files_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of file | 
 **workspace_id** | **int**| ID of workspace | 
 **page_number** | **int**| Page number of file (for viewer tokens) | [optional] [default to 1]

### Return type

[**FileInfoMapped**](FileInfoMapped.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_files_id_copy**
> FileCopyMove post_files_id_copy(id, workspace_id, destination_folder_id)

Copy file

Copy file into another folder (existing file will not be modified)

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FilesApi()
id = 56 # int | ID of file to copy
workspace_id = 56 # int | ID of workspace
destination_folder_id = 56 # int | ID of destination parent folder

try: 
    # Copy file
    api_response = api_instance.post_files_id_copy(id, workspace_id, destination_folder_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FilesApi->post_files_id_copy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of file to copy | 
 **workspace_id** | **int**| ID of workspace | 
 **destination_folder_id** | **int**| ID of destination parent folder | 

### Return type

[**FileCopyMove**](FileCopyMove.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_files_id_move**
> FileCopyMove post_files_id_move(id, workspace_id, destination_folder_id)

Move file

Move file into another folder

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FilesApi()
id = 56 # int | ID of file to move
workspace_id = 56 # int | ID of workspace
destination_folder_id = 56 # int | ID of destination parent folder

try: 
    # Move file
    api_response = api_instance.post_files_id_move(id, workspace_id, destination_folder_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FilesApi->post_files_id_move: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of file to move | 
 **workspace_id** | **int**| ID of workspace | 
 **destination_folder_id** | **int**| ID of destination parent folder | 

### Return type

[**FileCopyMove**](FileCopyMove.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_files_id**
> FileInfoMapped put_files_id(id, workspace_id, file_title=file_title, file_index=file_index)

Update file information

Update file information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FilesApi()
id = 56 # int | ID of file
workspace_id = 56 # int | ID of workspace
file_title = 'file_title_example' # str | Title of file (optional)
file_index = 56 # int | Index number of file within current folder scope (integer) (optional)

try: 
    # Update file information
    api_response = api_instance.put_files_id(id, workspace_id, file_title=file_title, file_index=file_index)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FilesApi->put_files_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of file | 
 **workspace_id** | **int**| ID of workspace | 
 **file_title** | **str**| Title of file | [optional] 
 **file_index** | **int**| Index number of file within current folder scope (integer) | [optional] 

### Return type

[**FileInfoMapped**](FileInfoMapped.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_files_upload**
> FileInfoCompact put_files_upload(workspace_id, folder_id, file_name)

Upload file

Create or update a file with the same file name. Request body should be the file body itself as binary data.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FilesApi()
workspace_id = 56 # int | Workspace ID
folder_id = 56 # int | Folder ID
file_name = 'file_name_example' # str | File name

try: 
    # Upload file
    api_response = api_instance.put_files_upload(workspace_id, folder_id, file_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FilesApi->put_files_upload: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**| Workspace ID | 
 **folder_id** | **int**| Folder ID | 
 **file_name** | **str**| File name | 

### Return type

[**FileInfoCompact**](FileInfoCompact.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

