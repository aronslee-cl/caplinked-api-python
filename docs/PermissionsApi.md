# caplinked.PermissionsApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_permissions_folders_id**](PermissionsApi.md#get_permissions_folders_id) | **GET** /permissions/folders/{id} | List subfolder permissions
[**put_permissions_folders_id**](PermissionsApi.md#put_permissions_folders_id) | **PUT** /permissions/folders/{id} | Update folder permissions


# **get_permissions_folders_id**
> FolderList get_permissions_folders_id(id, workspace_id, group_id)

List subfolder permissions

List subfolder permissions for a group. Will return an array of subfolders under the specified folder, along with their permissions information. For is_mixed_view, is_mixed_download, and is_mixed_upload: if attribute is set to true, it indicates that at least one (but not all) child folder with view, download, or upload attributes set to true, respectively. \"All Folders\" is the parent of all other folders within the workspace; its permissions will be returned if a folder is not specified.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.PermissionsApi()
id = 56 # int | ID of folder (0 for root)
workspace_id = 56 # int | ID of workspace
group_id = 56 # int | ID of group

try: 
    # List subfolder permissions
    api_response = api_instance.get_permissions_folders_id(id, workspace_id, group_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PermissionsApi->get_permissions_folders_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of folder (0 for root) | 
 **workspace_id** | **int**| ID of workspace | 
 **group_id** | **int**| ID of group | 

### Return type

[**FolderList**](FolderList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_permissions_folders_id**
> FolderUpdate put_permissions_folders_id(id, workspace_id, group_id, verb, folder_action)

Update folder permissions

Update folder permissions for a group. View = TRUE, this means that group members can return the folder/file and its viewer image. Download = TRUE, this means tha that group members can create download containing the folder. Upload = TRUE, this mean that group members can create an upload object with the folder as a parent.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.PermissionsApi()
id = 56 # int | ID of folder (0 for root)
workspace_id = 56 # int | ID of workspace
group_id = 56 # int | ID of group
verb = 'verb_example' # str | Grant or revoke permission for folder
folder_action = 'folder_action_example' # str | Permission type for folder

try: 
    # Update folder permissions
    api_response = api_instance.put_permissions_folders_id(id, workspace_id, group_id, verb, folder_action)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PermissionsApi->put_permissions_folders_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of folder (0 for root) | 
 **workspace_id** | **int**| ID of workspace | 
 **group_id** | **int**| ID of group | 
 **verb** | **str**| Grant or revoke permission for folder | 
 **folder_action** | **str**| Permission type for folder | 

### Return type

[**FolderUpdate**](FolderUpdate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

