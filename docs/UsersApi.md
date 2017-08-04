# caplinked.UsersApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_users**](UsersApi.md#delete_users) | **DELETE** /users | Delete user
[**get_users_me**](UsersApi.md#get_users_me) | **GET** /users/me | Get user information
[**post_users**](UsersApi.md#post_users) | **POST** /users | Create user
[**put_users_me**](UsersApi.md#put_users_me) | **PUT** /users/me | Update a user


# **delete_users**
> StatusMessage delete_users(user_id)

Delete user

Delete user

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.UsersApi()
user_id = 56 # int | ID of the user you want to delete

try: 
    # Delete user
    api_response = api_instance.delete_users(user_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UsersApi->delete_users: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**| ID of the user you want to delete | 

### Return type

[**StatusMessage**](StatusMessage.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_users_me**
> User get_users_me()

Get user information

Get user information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.UsersApi()

try: 
    # Get user information
    api_response = api_instance.get_users_me()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UsersApi->get_users_me: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_users**
> User post_users(user_email, user_first_name, user_last_name, user_time_zone=user_time_zone)

Create user

Create user

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.UsersApi()
user_email = 'user_email_example' # str | Email of new user
user_first_name = 'user_first_name_example' # str | First of new user
user_last_name = 'user_last_name_example' # str | Last name of new user
user_time_zone = 'user_time_zone_example' # str | Time zone of new user (optional)

try: 
    # Create user
    api_response = api_instance.post_users(user_email, user_first_name, user_last_name, user_time_zone=user_time_zone)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UsersApi->post_users: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_email** | **str**| Email of new user | 
 **user_first_name** | **str**| First of new user | 
 **user_last_name** | **str**| Last name of new user | 
 **user_time_zone** | **str**| Time zone of new user | [optional] 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_users_me**
> User put_users_me(user_email=user_email, user_first_name=user_first_name, user_last_name=user_last_name, user_time_zone=user_time_zone)

Update a user

Update a user

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.UsersApi()
user_email = 'user_email_example' # str | Email of user to update (optional)
user_first_name = 'user_first_name_example' # str | First name of user to update (optional)
user_last_name = 'user_last_name_example' # str | Last name of user to update (optional)
user_time_zone = 'user_time_zone_example' # str | Time zone of user to update (optional)

try: 
    # Update a user
    api_response = api_instance.put_users_me(user_email=user_email, user_first_name=user_first_name, user_last_name=user_last_name, user_time_zone=user_time_zone)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UsersApi->put_users_me: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_email** | **str**| Email of user to update | [optional] 
 **user_first_name** | **str**| First name of user to update | [optional] 
 **user_last_name** | **str**| Last name of user to update | [optional] 
 **user_time_zone** | **str**| Time zone of user to update | [optional] 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

