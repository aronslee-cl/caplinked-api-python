# caplinked.WorkspacesApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_workspaces**](WorkspacesApi.md#get_workspaces) | **GET** /workspaces | List all workspaces for a team
[**get_workspaces_id**](WorkspacesApi.md#get_workspaces_id) | **GET** /workspaces/{id} | Get workspace information
[**post_workspaces**](WorkspacesApi.md#post_workspaces) | **POST** /workspaces | Create workspace
[**put_workspaces_id**](WorkspacesApi.md#put_workspaces_id) | **PUT** /workspaces/{id} | Update workspace


# **get_workspaces**
> Workspace get_workspaces(team_id)

List all workspaces for a team

List all workspaces for a team

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.WorkspacesApi()
team_id = 56 # int | ID of team from which to list workspaces

try: 
    # List all workspaces for a team
    api_response = api_instance.get_workspaces(team_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspacesApi->get_workspaces: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **team_id** | **int**| ID of team from which to list workspaces | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workspaces_id**
> Workspace get_workspaces_id(id)

Get workspace information

Get workspace information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.WorkspacesApi()
id = 56 # int | ID of workspace

try: 
    # Get workspace information
    api_response = api_instance.get_workspaces_id(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspacesApi->get_workspaces_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of workspace | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_workspaces**
> Workspace post_workspaces(team_id, workspace_name)

Create workspace

Create workspace. Workspace creator will be added to Workspace Admins group.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.WorkspacesApi()
team_id = 56 # int | ID of parent team for this workspace
workspace_name = 'workspace_name_example' # str | Name of workspace to create

try: 
    # Create workspace
    api_response = api_instance.post_workspaces(team_id, workspace_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspacesApi->post_workspaces: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **team_id** | **int**| ID of parent team for this workspace | 
 **workspace_name** | **str**| Name of workspace to create | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_workspaces_id**
> Workspace put_workspaces_id(id, workspace_name=workspace_name)

Update workspace

Update workspace

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.WorkspacesApi()
id = 56 # int | ID of workspace to update
workspace_name = 'workspace_name_example' # str | Name of workspace to update (optional)

try: 
    # Update workspace
    api_response = api_instance.put_workspaces_id(id, workspace_name=workspace_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WorkspacesApi->put_workspaces_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of workspace to update | 
 **workspace_name** | **str**| Name of workspace to update | [optional] 

### Return type

[**Workspace**](Workspace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

