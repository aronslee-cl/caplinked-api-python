# caplinked.TeamsApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_teams_id_memberships**](TeamsApi.md#delete_teams_id_memberships) | **DELETE** /teams/{id}/memberships | Remove team member
[**get_teams**](TeamsApi.md#get_teams) | **GET** /teams | List all teams in organization
[**get_teams_id**](TeamsApi.md#get_teams_id) | **GET** /teams/{id} | Get team information
[**get_teams_id_memberships**](TeamsApi.md#get_teams_id_memberships) | **GET** /teams/{id}/memberships | Get list of team members
[**get_teams_id_watermark_settings**](TeamsApi.md#get_teams_id_watermark_settings) | **GET** /teams/{id}/watermark_settings | List custom watermarks for a team
[**post_teams**](TeamsApi.md#post_teams) | **POST** /teams | Create team
[**post_teams_id_memberships**](TeamsApi.md#post_teams_id_memberships) | **POST** /teams/{id}/memberships | Add team member
[**put_teams_id**](TeamsApi.md#put_teams_id) | **PUT** /teams/{id} | Update team


# **delete_teams_id_memberships**
> delete_teams_id_memberships(id, user_id)

Remove team member

Remove team member

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.TeamsApi()
id = 56 # int | ID of team from which user will be removed
user_id = 56 # int | ID of user to remove

try: 
    # Remove team member
    api_instance.delete_teams_id_memberships(id, user_id)
except ApiException as e:
    print("Exception when calling TeamsApi->delete_teams_id_memberships: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of team from which user will be removed | 
 **user_id** | **int**| ID of user to remove | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_teams**
> Team get_teams()

List all teams in organization

List all teams in organization

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.TeamsApi()

try: 
    # List all teams in organization
    api_response = api_instance.get_teams()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->get_teams: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Team**](Team.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_teams_id**
> Team get_teams_id(id)

Get team information

Get team information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.TeamsApi()
id = 56 # int | ID of the Team

try: 
    # Get team information
    api_response = api_instance.get_teams_id(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->get_teams_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the Team | 

### Return type

[**Team**](Team.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_teams_id_memberships**
> list[Membership] get_teams_id_memberships(id)

Get list of team members

Get list of team members

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.TeamsApi()
id = 56 # int | ID of team for which users will be listed

try: 
    # Get list of team members
    api_response = api_instance.get_teams_id_memberships(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->get_teams_id_memberships: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of team for which users will be listed | 

### Return type

[**list[Membership]**](Membership.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_teams_id_watermark_settings**
> CustomWatermarkSetting get_teams_id_watermark_settings(id)

List custom watermarks for a team

List custom watermarks for a team

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.TeamsApi()
id = 56 # int | ID of team

try: 
    # List custom watermarks for a team
    api_response = api_instance.get_teams_id_watermark_settings(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->get_teams_id_watermark_settings: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of team | 

### Return type

[**CustomWatermarkSetting**](CustomWatermarkSetting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_teams**
> Team post_teams(team_name, team_allowed_workspaces=team_allowed_workspaces, team_allowed_admins=team_allowed_admins, team_drm_enabled=team_drm_enabled, team_watermarking=team_watermarking, team_suppress_emails=team_suppress_emails)

Create team

Create team. Current user will become team owner.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.TeamsApi()
team_name = 'team_name_example' # str | Name of the team
team_allowed_workspaces = 1 # int | Maximum workspaces for team (optional) (default to 1)
team_allowed_admins = 10 # int | Maximum number of admins for team (optional) (default to 10)
team_drm_enabled = true # bool | Toggle DRM (feature availability in workspaces) (optional)
team_watermarking = true # bool | Toggle watermarking (feature availability in workspaces) (optional)
team_suppress_emails = true # bool | Toggle email invites (optional) (default to true)

try: 
    # Create team
    api_response = api_instance.post_teams(team_name, team_allowed_workspaces=team_allowed_workspaces, team_allowed_admins=team_allowed_admins, team_drm_enabled=team_drm_enabled, team_watermarking=team_watermarking, team_suppress_emails=team_suppress_emails)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->post_teams: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **team_name** | **str**| Name of the team | 
 **team_allowed_workspaces** | **int**| Maximum workspaces for team | [optional] [default to 1]
 **team_allowed_admins** | **int**| Maximum number of admins for team | [optional] [default to 10]
 **team_drm_enabled** | **bool**| Toggle DRM (feature availability in workspaces) | [optional] 
 **team_watermarking** | **bool**| Toggle watermarking (feature availability in workspaces) | [optional] 
 **team_suppress_emails** | **bool**| Toggle email invites | [optional] [default to true]

### Return type

[**Team**](Team.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_teams_id_memberships**
> Membership post_teams_id_memberships(id, user_id)

Add team member

Add team member

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.TeamsApi()
id = 56 # int | ID of team to which user will be added
user_id = 56 # int | ID of user to add

try: 
    # Add team member
    api_response = api_instance.post_teams_id_memberships(id, user_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->post_teams_id_memberships: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of team to which user will be added | 
 **user_id** | **int**| ID of user to add | 

### Return type

[**Membership**](Membership.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_teams_id**
> Team put_teams_id(id, team_name=team_name, team_team_owner_id=team_team_owner_id, team_allowed_workspaces=team_allowed_workspaces, team_allowed_admins=team_allowed_admins, team_drm_enabled=team_drm_enabled, team_watermarking=team_watermarking, team_suppress_emails=team_suppress_emails)

Update team

Update team. Includes option to designate a new Team Owner.

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.TeamsApi()
id = 56 # int | ID of team to update
team_name = 'team_name_example' # str | Name of the team (optional)
team_team_owner_id = 56 # int | User ID of the team owner (optional)
team_allowed_workspaces = 56 # int | Maximum workspaces for team (optional)
team_allowed_admins = 56 # int | Maximum number of admins for team (optional)
team_drm_enabled = true # bool | Toggle DRM (feature availability in workspaces) (optional)
team_watermarking = true # bool | Toggle watermarking (feature availability in workspaces) (optional)
team_suppress_emails = true # bool | Toggle email invites (optional)

try: 
    # Update team
    api_response = api_instance.put_teams_id(id, team_name=team_name, team_team_owner_id=team_team_owner_id, team_allowed_workspaces=team_allowed_workspaces, team_allowed_admins=team_allowed_admins, team_drm_enabled=team_drm_enabled, team_watermarking=team_watermarking, team_suppress_emails=team_suppress_emails)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->put_teams_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of team to update | 
 **team_name** | **str**| Name of the team | [optional] 
 **team_team_owner_id** | **int**| User ID of the team owner | [optional] 
 **team_allowed_workspaces** | **int**| Maximum workspaces for team | [optional] 
 **team_allowed_admins** | **int**| Maximum number of admins for team | [optional] 
 **team_drm_enabled** | **bool**| Toggle DRM (feature availability in workspaces) | [optional] 
 **team_watermarking** | **bool**| Toggle watermarking (feature availability in workspaces) | [optional] 
 **team_suppress_emails** | **bool**| Toggle email invites | [optional] 

### Return type

[**Team**](Team.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

