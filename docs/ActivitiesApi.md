# caplinked.ActivitiesApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_activities_workspace_workspace_id**](ActivitiesApi.md#get_activities_workspace_workspace_id) | **GET** /activities/workspace/{workspace_id} | Get workspace activities


# **get_activities_workspace_workspace_id**
> Activity get_activities_workspace_workspace_id(workspace_id, page=page, per_page=per_page, user_id=user_id)

Get workspace activities

Get workspace activities

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.ActivitiesApi()
workspace_id = 56 # int | ID of the workspace
page = 1 # int | Page number of results (optional) (default to 1)
per_page = 100 # int | Per page number of results. Options: 25, 50, 75, 100 (optional) (default to 100)
user_id = 56 # int | ID of the user  (optional)

try: 
    # Get workspace activities
    api_response = api_instance.get_activities_workspace_workspace_id(workspace_id, page=page, per_page=per_page, user_id=user_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ActivitiesApi->get_activities_workspace_workspace_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**| ID of the workspace | 
 **page** | **int**| Page number of results | [optional] [default to 1]
 **per_page** | **int**| Per page number of results. Options: 25, 50, 75, 100 | [optional] [default to 100]
 **user_id** | **int**| ID of the user  | [optional] 

### Return type

[**Activity**](Activity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

