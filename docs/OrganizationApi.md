# caplinked.OrganizationApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_organization_memberships**](OrganizationApi.md#delete_organization_memberships) | **DELETE** /organization/memberships | Remove organization admin membership
[**get_organization**](OrganizationApi.md#get_organization) | **GET** /organization | Get organization information
[**get_organization_memberships**](OrganizationApi.md#get_organization_memberships) | **GET** /organization/memberships | Show all organization members
[**post_organization_memberships**](OrganizationApi.md#post_organization_memberships) | **POST** /organization/memberships | Add organization admin membership
[**put_organization**](OrganizationApi.md#put_organization) | **PUT** /organization | Update organization information
[**put_organization_support_information**](OrganizationApi.md#put_organization_support_information) | **PUT** /organization/support_information | Update support information of organization


# **delete_organization_memberships**
> delete_organization_memberships(user_id)

Remove organization admin membership

Remove organization admin membership

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.OrganizationApi()
user_id = 56 # int | ID of user to be removed as an organization admin

try: 
    # Remove organization admin membership
    api_instance.delete_organization_memberships(user_id)
except ApiException as e:
    print("Exception when calling OrganizationApi->delete_organization_memberships: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**| ID of user to be removed as an organization admin | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_organization**
> Organization get_organization()

Get organization information

Get organization information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.OrganizationApi()

try: 
    # Get organization information
    api_response = api_instance.get_organization()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrganizationApi->get_organization: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Organization**](Organization.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_organization_memberships**
> User get_organization_memberships()

Show all organization members

Show all organization members

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.OrganizationApi()

try: 
    # Show all organization members
    api_response = api_instance.get_organization_memberships()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrganizationApi->get_organization_memberships: %s\n" % e)
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

# **post_organization_memberships**
> OrganizationMembership post_organization_memberships(user_id)

Add organization admin membership

Add organization admin membership

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.OrganizationApi()
user_id = 56 # int | ID of user to be added as an organization admin

try: 
    # Add organization admin membership
    api_response = api_instance.post_organization_memberships(user_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrganizationApi->post_organization_memberships: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**| ID of user to be added as an organization admin | 

### Return type

[**OrganizationMembership**](OrganizationMembership.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_organization**
> Organization put_organization(name=name, description=description, location=location, billing_email=billing_email, url=url)

Update organization information

Update organization information

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.OrganizationApi()
name = 'name_example' # str | Name of the organization to update (optional)
description = 'description_example' # str | Description of the organization to update (optional)
location = 'location_example' # str | Location of the organization to update (optional)
billing_email = 'billing_email_example' # str | Billing email address of the organization to update (optional)
url = 'url_example' # str | Website of the organization to update (optional)

try: 
    # Update organization information
    api_response = api_instance.put_organization(name=name, description=description, location=location, billing_email=billing_email, url=url)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrganizationApi->put_organization: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| Name of the organization to update | [optional] 
 **description** | **str**| Description of the organization to update | [optional] 
 **location** | **str**| Location of the organization to update | [optional] 
 **billing_email** | **str**| Billing email address of the organization to update | [optional] 
 **url** | **str**| Website of the organization to update | [optional] 

### Return type

[**Organization**](Organization.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_organization_support_information**
> SupportInformation put_organization_support_information(phone_number=phone_number, email=email, website=website)

Update support information of organization

Update support information of organization

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.OrganizationApi()
phone_number = 'phone_number_example' # str | Support phone number of the organization to update (optional)
email = 'email_example' # str | Support email of the organization to update (optional)
website = 'website_example' # str | Support website of the organization to update (optional)

try: 
    # Update support information of organization
    api_response = api_instance.put_organization_support_information(phone_number=phone_number, email=email, website=website)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrganizationApi->put_organization_support_information: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **phone_number** | **str**| Support phone number of the organization to update | [optional] 
 **email** | **str**| Support email of the organization to update | [optional] 
 **website** | **str**| Support website of the organization to update | [optional] 

### Return type

[**SupportInformation**](SupportInformation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

