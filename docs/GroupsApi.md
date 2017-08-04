# caplinked.GroupsApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_groups_id**](GroupsApi.md#delete_groups_id) | **DELETE** /groups/{id} | Delete group
[**delete_groups_id_memberships**](GroupsApi.md#delete_groups_id_memberships) | **DELETE** /groups/{id}/memberships | Remove a user from a group
[**get_groups**](GroupsApi.md#get_groups) | **GET** /groups | List all groups in workspace
[**get_groups_id**](GroupsApi.md#get_groups_id) | **GET** /groups/{id} | Get group information
[**get_groups_id_memberships**](GroupsApi.md#get_groups_id_memberships) | **GET** /groups/{id}/memberships | List all memberships for a group
[**post_groups**](GroupsApi.md#post_groups) | **POST** /groups | Create group
[**post_groups_id_memberships**](GroupsApi.md#post_groups_id_memberships) | **POST** /groups/{id}/memberships | Add user to group (adds to parent workspace if they are not already a member)
[**put_groups_id**](GroupsApi.md#put_groups_id) | **PUT** /groups/{id} | Update group
[**put_groups_id_disable_drm_expiration**](GroupsApi.md#put_groups_id_disable_drm_expiration) | **PUT** /groups/{id}/disable_drm_expiration | Disable DRM expiration for group
[**put_groups_id_disable_expire_access**](GroupsApi.md#put_groups_id_disable_expire_access) | **PUT** /groups/{id}/disable_expire_access | Disable access expiration for a group
[**put_groups_id_drm**](GroupsApi.md#put_groups_id_drm) | **PUT** /groups/{id}/drm | Update DRM for group
[**put_groups_id_enable_expire_access**](GroupsApi.md#put_groups_id_enable_expire_access) | **PUT** /groups/{id}/enable_expire_access | Enable access expiration for a group
[**put_groups_id_watermarking**](GroupsApi.md#put_groups_id_watermarking) | **PUT** /groups/{id}/watermarking | Watermarking for group


# **delete_groups_id**
> GroupInfoDeleted delete_groups_id(id, workspace_id)

Delete group

Delete group

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of group to update
workspace_id = 56 # int | Workspace ID for the group

try: 
    # Delete group
    api_response = api_instance.delete_groups_id(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->delete_groups_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of group to update | 
 **workspace_id** | **int**| Workspace ID for the group | 

### Return type

[**GroupInfoDeleted**](GroupInfoDeleted.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_groups_id_memberships**
> delete_groups_id_memberships(id, workspace_id, user_id)

Remove a user from a group

Remove a user from a group. Members of the Workspace Admin group may only be removed by other Workspace Admins. If Workspace Admin is Team Member, they may only be removed by another Team Member.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of the group you wish the user to be removed from
workspace_id = 56 # int | Workspace ID for the group
user_id = 56 # int | ID of the user to be removed from this group

try: 
    # Remove a user from a group
    api_instance.delete_groups_id_memberships(id, workspace_id, user_id)
except ApiException as e:
    print("Exception when calling GroupsApi->delete_groups_id_memberships: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the group you wish the user to be removed from | 
 **workspace_id** | **int**| Workspace ID for the group | 
 **user_id** | **int**| ID of the user to be removed from this group | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_groups**
> GroupInfo get_groups(workspace_id)

List all groups in workspace

List all groups in workspace

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
workspace_id = 56 # int | ID of workspace from which to list groups

try: 
    # List all groups in workspace
    api_response = api_instance.get_groups(workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->get_groups: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**| ID of workspace from which to list groups | 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_groups_id**
> GroupInfo get_groups_id(id, workspace_id)

Get group information

Get group information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of group
workspace_id = 56 # int | Workspace ID for the group

try: 
    # Get group information
    api_response = api_instance.get_groups_id(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->get_groups_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of group | 
 **workspace_id** | **int**| Workspace ID for the group | 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_groups_id_memberships**
> User get_groups_id_memberships(id, workspace_id)

List all memberships for a group

List all memberships for a group. Note that Workspace Admins are in two groups: Workspace Admins and Team Admins. The latter contains workspace admins that are also Team Members of the workspace parent team.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of the group you want to list the members of
workspace_id = 56 # int | Workspace ID for the group

try: 
    # List all memberships for a group
    api_response = api_instance.get_groups_id_memberships(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->get_groups_id_memberships: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the group you want to list the members of | 
 **workspace_id** | **int**| Workspace ID for the group | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_groups**
> GroupInfo post_groups(group_name, group_workspace_id, group_file_managing_abilities=group_file_managing_abilities)

Create group

Create group

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
group_name = 'group_name_example' # str | Name of group
group_workspace_id = 56 # int | Workspace ID for the group
group_file_managing_abilities = true # bool | Enable file managing abililies for uploading users (optional)

try: 
    # Create group
    api_response = api_instance.post_groups(group_name, group_workspace_id, group_file_managing_abilities=group_file_managing_abilities)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->post_groups: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group_name** | **str**| Name of group | 
 **group_workspace_id** | **int**| Workspace ID for the group | 
 **group_file_managing_abilities** | **bool**| Enable file managing abililies for uploading users | [optional] 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_groups_id_memberships**
> post_groups_id_memberships(id, workspace_id, user_id, send_email=send_email)

Add user to group (adds to parent workspace if they are not already a member)

Add user to group (adds to parent workspace if they are not already a member)

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of the group you wish the user to be added to
workspace_id = 56 # int | Workspace ID for the group
user_id = 56 # int | ID of the user to be added to this group
send_email = true # bool | Send workspace invitation email to this user.  Defaults to true, use false if you do not want the email to be sent (optional)

try: 
    # Add user to group (adds to parent workspace if they are not already a member)
    api_instance.post_groups_id_memberships(id, workspace_id, user_id, send_email=send_email)
except ApiException as e:
    print("Exception when calling GroupsApi->post_groups_id_memberships: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the group you wish the user to be added to | 
 **workspace_id** | **int**| Workspace ID for the group | 
 **user_id** | **int**| ID of the user to be added to this group | 
 **send_email** | **bool**| Send workspace invitation email to this user.  Defaults to true, use false if you do not want the email to be sent | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_groups_id**
> GroupInfo put_groups_id(id, workspace_id, group_name=group_name, group_file_managing_abilities=group_file_managing_abilities)

Update group

Update group

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of group
workspace_id = 56 # int | Workspace ID for the group
group_name = 'group_name_example' # str | Name of group (optional)
group_file_managing_abilities = true # bool | Ability to delete, rename, and reindex files for uploading users (optional)

try: 
    # Update group
    api_response = api_instance.put_groups_id(id, workspace_id, group_name=group_name, group_file_managing_abilities=group_file_managing_abilities)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->put_groups_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of group | 
 **workspace_id** | **int**| Workspace ID for the group | 
 **group_name** | **str**| Name of group | [optional] 
 **group_file_managing_abilities** | **bool**| Ability to delete, rename, and reindex files for uploading users | [optional] 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_groups_id_disable_drm_expiration**
> GroupInfo put_groups_id_disable_drm_expiration(id, workspace_id)

Disable DRM expiration for group

Disable DRM expiration for group

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of group to update
workspace_id = 56 # int | Workspace ID for the group

try: 
    # Disable DRM expiration for group
    api_response = api_instance.put_groups_id_disable_drm_expiration(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->put_groups_id_disable_drm_expiration: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of group to update | 
 **workspace_id** | **int**| Workspace ID for the group | 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_groups_id_disable_expire_access**
> GroupInfo put_groups_id_disable_expire_access(id, workspace_id)

Disable access expiration for a group

Disable access expiration for a group

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of group to update
workspace_id = 56 # int | Workspace ID for the group

try: 
    # Disable access expiration for a group
    api_response = api_instance.put_groups_id_disable_expire_access(id, workspace_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->put_groups_id_disable_expire_access: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of group to update | 
 **workspace_id** | **int**| Workspace ID for the group | 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_groups_id_drm**
> GroupInfo put_groups_id_drm(id, workspace_id, group_drm_enabled, group_drm_expires_after=group_drm_expires_after)

Update DRM for group

Update DRM for group

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of group to update
workspace_id = 56 # int | Workspace ID for the group
group_drm_enabled = 'group_drm_enabled_example' # str | Enable DRM for group
group_drm_expires_after = '2013-10-20' # date | Expire DRM after this date. Format: yyyy-mm-dd (optional)

try: 
    # Update DRM for group
    api_response = api_instance.put_groups_id_drm(id, workspace_id, group_drm_enabled, group_drm_expires_after=group_drm_expires_after)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->put_groups_id_drm: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of group to update | 
 **workspace_id** | **int**| Workspace ID for the group | 
 **group_drm_enabled** | **str**| Enable DRM for group | 
 **group_drm_expires_after** | **date**| Expire DRM after this date. Format: yyyy-mm-dd | [optional] 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_groups_id_enable_expire_access**
> GroupInfo put_groups_id_enable_expire_access(id, workspace_id, group_expire_workspace_access_at)

Enable access expiration for a group

Enable access expiration for a group

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of group to update
workspace_id = 56 # int | Workspace ID for the group
group_expire_workspace_access_at = '2013-10-20' # date | Expire access on the following date. Format: yyyy-mm-dd

try: 
    # Enable access expiration for a group
    api_response = api_instance.put_groups_id_enable_expire_access(id, workspace_id, group_expire_workspace_access_at)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->put_groups_id_enable_expire_access: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of group to update | 
 **workspace_id** | **int**| Workspace ID for the group | 
 **group_expire_workspace_access_at** | **date**| Expire access on the following date. Format: yyyy-mm-dd | 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_groups_id_watermarking**
> GroupInfo put_groups_id_watermarking(id, workspace_id, group_watermarking)

Watermarking for group

Watermarking for group

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.GroupsApi()
id = 56 # int | ID of group to update
workspace_id = 56 # int | Workspace ID for the group
group_watermarking = true # bool | Enable watermarking for group

try: 
    # Watermarking for group
    api_response = api_instance.put_groups_id_watermarking(id, workspace_id, group_watermarking)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GroupsApi->put_groups_id_watermarking: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of group to update | 
 **workspace_id** | **int**| Workspace ID for the group | 
 **group_watermarking** | **bool**| Enable watermarking for group | 

### Return type

[**GroupInfo**](GroupInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

