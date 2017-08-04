# caplinked.FoldersApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_folders_id**](FoldersApi.md#delete_folders_id) | **DELETE** /folders/{id} | Delete folder
[**get_folders_id**](FoldersApi.md#get_folders_id) | **GET** /folders/{id} | Get folder information
[**post_folders**](FoldersApi.md#post_folders) | **POST** /folders | Create new folder
[**post_folders_id_copy**](FoldersApi.md#post_folders_id_copy) | **POST** /folders/{id}/copy | Copy folder
[**post_folders_id_move**](FoldersApi.md#post_folders_id_move) | **POST** /folders/{id}/move | Move folder
[**put_folders_id**](FoldersApi.md#put_folders_id) | **PUT** /folders/{id} | Update folder information


# **delete_folders_id**
> FolderDelete delete_folders_id(id, workspace_id)

Delete folder

Delete folder

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FoldersApi()
id = 56 # int | ID of folder to delete
workspace_id = 'workspace_id_example' # str | ID of workspace

try: 
    # Delete folder
    api_response = api_instance.delete_folders_id(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->delete_folders_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of folder to delete | 
 **workspace_id** | **str**| ID of workspace | 

### Return type

[**FolderDelete**](FolderDelete.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_folders_id**
> FolderContent get_folders_id(id, workspace_id)

Get folder information

Get folder information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FoldersApi()
id = 56 # int | ID of folder
workspace_id = 'workspace_id_example' # str | ID of workspace

try: 
    # Get folder information
    api_response = api_instance.get_folders_id(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->get_folders_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of folder | 
 **workspace_id** | **str**| ID of workspace | 

### Return type

[**FolderContent**](FolderContent.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_folders**
> FolderMeta post_folders(workspace_id, name, parent_id=parent_id)

Create new folder

Create new folder

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FoldersApi()
workspace_id = 'workspace_id_example' # str | ID of workspace
name = 'name_example' # str | Name of new folder
parent_id = 0 # int | ID of parent folder (defaults to root folder [id=0]) (optional) (default to 0)

try: 
    # Create new folder
    api_response = api_instance.post_folders(workspace_id, name, parent_id=parent_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->post_folders: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **str**| ID of workspace | 
 **name** | **str**| Name of new folder | 
 **parent_id** | **int**| ID of parent folder (defaults to root folder [id&#x3D;0]) | [optional] [default to 0]

### Return type

[**FolderMeta**](FolderMeta.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_folders_id_copy**
> FolderCopyMove post_folders_id_copy(id, workspace_id, destination_folder_id)

Copy folder

Copy folder into another folder (existing folder will not be modified). The copied folder will inherit group folder permissions from its new parent folder.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FoldersApi()
id = 56 # int | ID of folder to copy
workspace_id = 'workspace_id_example' # str | ID of workspace
destination_folder_id = 56 # int | ID of destination parent folder

try: 
    # Copy folder
    api_response = api_instance.post_folders_id_copy(id, workspace_id, destination_folder_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->post_folders_id_copy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of folder to copy | 
 **workspace_id** | **str**| ID of workspace | 
 **destination_folder_id** | **int**| ID of destination parent folder | 

### Return type

[**FolderCopyMove**](FolderCopyMove.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_folders_id_move**
> FolderCopyMove post_folders_id_move(id, workspace_id, destination_folder_id)

Move folder

Move folder into another folder

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FoldersApi()
id = 56 # int | ID of folder to move
workspace_id = 'workspace_id_example' # str | ID of workspace
destination_folder_id = 56 # int | ID of destination parent folder

try: 
    # Move folder
    api_response = api_instance.post_folders_id_move(id, workspace_id, destination_folder_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->post_folders_id_move: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of folder to move | 
 **workspace_id** | **str**| ID of workspace | 
 **destination_folder_id** | **int**| ID of destination parent folder | 

### Return type

[**FolderCopyMove**](FolderCopyMove.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_folders_id**
> FolderMeta put_folders_id(id, workspace_id, folder_name=folder_name, folder_index=folder_index)

Update folder information

Update folder information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.FoldersApi()
id = 56 # int | Update folder name and index
workspace_id = 'workspace_id_example' # str | ID of workspace
folder_name = 'folder_name_example' # str | Name of folder (optional)
folder_index = 56 # int | Index number of folder within current folder scope (integer) (optional)

try: 
    # Update folder information
    api_response = api_instance.put_folders_id(id, workspace_id, folder_name=folder_name, folder_index=folder_index)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->put_folders_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Update folder name and index | 
 **workspace_id** | **str**| ID of workspace | 
 **folder_name** | **str**| Name of folder | [optional] 
 **folder_index** | **int**| Index number of folder within current folder scope (integer) | [optional] 

### Return type

[**FolderMeta**](FolderMeta.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

