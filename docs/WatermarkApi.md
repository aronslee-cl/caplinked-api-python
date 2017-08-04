# caplinked.WatermarkApi

All URIs are relative to *https://sandbox.caplinked.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_watermark_id**](WatermarkApi.md#delete_watermark_id) | **DELETE** /watermark/{id} | Delete custom watermark
[**get_watermark_id**](WatermarkApi.md#get_watermark_id) | **GET** /watermark/{id} | Get custom watermark setting
[**post_watermark**](WatermarkApi.md#post_watermark) | **POST** /watermark | Add custom watermark
[**put_watermark_id**](WatermarkApi.md#put_watermark_id) | **PUT** /watermark/{id} | Update custom watermark


# **delete_watermark_id**
> StatusMessage delete_watermark_id(id)

Delete custom watermark

Delete custom watermark

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.WatermarkApi()
id = 56 # int | ID of the watermark setting to delete

try: 
    # Delete custom watermark
    api_response = api_instance.delete_watermark_id(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WatermarkApi->delete_watermark_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the watermark setting to delete | 

### Return type

[**StatusMessage**](StatusMessage.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_watermark_id**
> CustomWatermarkSetting get_watermark_id(id)

Get custom watermark setting

Get custom watermark setting

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.WatermarkApi()
id = 56 # int | ID of the watermark setting

try: 
    # Get custom watermark setting
    api_response = api_instance.get_watermark_id(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WatermarkApi->get_watermark_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the watermark setting | 

### Return type

[**CustomWatermarkSetting**](CustomWatermarkSetting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_watermark**
> CustomWatermarkSetting post_watermark(team_id, custom_text, color=color, opacity=opacity, font_size=font_size, rotation=rotation, hposition=hposition, vposition=vposition, display_user_name=display_user_name, display_user_email=display_user_email, display_ip_address=display_ip_address, display_time=display_time, display_workspace_name=display_workspace_name)

Add custom watermark

Add custom watermark

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.WatermarkApi()
team_id = 56 # int | ID of the team
custom_text = 'custom_text_example' # str | Custom watermark text
color = '#333333' # str | Hexadecimal color value (i.e. #eee, #e1e1e1) (optional) (default to #333333)
opacity = 0.5 # float | Opacity 0 to 1.0 (optional) (default to 0.5)
font_size = 18 # int | Font size in pixels (optional) (default to 18)
rotation = 0 # int | Rotation degrees (-90 to 90) (optional) (default to 0)
hposition = 'center' # str | Horizontal position (left, center, right) (optional) (default to center)
vposition = 'center' # str | Vertical position (top, center, bottom) (optional) (default to center)
display_user_name = true # bool | Display user name (optional) (default to true)
display_user_email = true # bool | Display user email address (optional) (default to true)
display_ip_address = true # bool | Display user IP address (optional) (default to true)
display_time = true # bool | Display time (optional) (default to true)
display_workspace_name = true # bool | Display workspace name (optional)

try: 
    # Add custom watermark
    api_response = api_instance.post_watermark(team_id, custom_text, color=color, opacity=opacity, font_size=font_size, rotation=rotation, hposition=hposition, vposition=vposition, display_user_name=display_user_name, display_user_email=display_user_email, display_ip_address=display_ip_address, display_time=display_time, display_workspace_name=display_workspace_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WatermarkApi->post_watermark: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **team_id** | **int**| ID of the team | 
 **custom_text** | **str**| Custom watermark text | 
 **color** | **str**| Hexadecimal color value (i.e. #eee, #e1e1e1) | [optional] [default to #333333]
 **opacity** | **float**| Opacity 0 to 1.0 | [optional] [default to 0.5]
 **font_size** | **int**| Font size in pixels | [optional] [default to 18]
 **rotation** | **int**| Rotation degrees (-90 to 90) | [optional] [default to 0]
 **hposition** | **str**| Horizontal position (left, center, right) | [optional] [default to center]
 **vposition** | **str**| Vertical position (top, center, bottom) | [optional] [default to center]
 **display_user_name** | **bool**| Display user name | [optional] [default to true]
 **display_user_email** | **bool**| Display user email address | [optional] [default to true]
 **display_ip_address** | **bool**| Display user IP address | [optional] [default to true]
 **display_time** | **bool**| Display time | [optional] [default to true]
 **display_workspace_name** | **bool**| Display workspace name | [optional] 

### Return type

[**CustomWatermarkSetting**](CustomWatermarkSetting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_watermark_id**
> CustomWatermarkSetting put_watermark_id(id, custom_text=custom_text, color=color, opacity=opacity, font_size=font_size, rotation=rotation, hposition=hposition, vposition=vposition, display_user_name=display_user_name, display_user_email=display_user_email, display_ip_address=display_ip_address, display_time=display_time, display_workspace_name=display_workspace_name)

Update custom watermark

Update custom watermark

### Example 
```python
from __future__ import print_function
import time
import caplinked
from caplinked.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = caplinked.WatermarkApi()
id = 56 # int | ID of the watermark setting to update
custom_text = 'custom_text_example' # str | Custom watermark text (optional)
color = 'color_example' # str | Hexadecimal color value (i.e. #eee, #e1e1e1) (optional)
opacity = 3.4 # float | Opacity 0 to 1.0 (optional)
font_size = 56 # int | Font size in pixels (optional)
rotation = 56 # int | Rotation degrees (-90 to 90) (optional)
hposition = 'hposition_example' # str | Horizontal position (left, center, right) (optional)
vposition = 'vposition_example' # str | Vertical position (top, center, bottom) (optional)
display_user_name = true # bool | Display user name (optional)
display_user_email = true # bool | Display user email address (optional)
display_ip_address = true # bool | Display user IP address (optional)
display_time = true # bool | Display time (optional)
display_workspace_name = true # bool | Display workspace name (optional)

try: 
    # Update custom watermark
    api_response = api_instance.put_watermark_id(id, custom_text=custom_text, color=color, opacity=opacity, font_size=font_size, rotation=rotation, hposition=hposition, vposition=vposition, display_user_name=display_user_name, display_user_email=display_user_email, display_ip_address=display_ip_address, display_time=display_time, display_workspace_name=display_workspace_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WatermarkApi->put_watermark_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the watermark setting to update | 
 **custom_text** | **str**| Custom watermark text | [optional] 
 **color** | **str**| Hexadecimal color value (i.e. #eee, #e1e1e1) | [optional] 
 **opacity** | **float**| Opacity 0 to 1.0 | [optional] 
 **font_size** | **int**| Font size in pixels | [optional] 
 **rotation** | **int**| Rotation degrees (-90 to 90) | [optional] 
 **hposition** | **str**| Horizontal position (left, center, right) | [optional] 
 **vposition** | **str**| Vertical position (top, center, bottom) | [optional] 
 **display_user_name** | **bool**| Display user name | [optional] 
 **display_user_email** | **bool**| Display user email address | [optional] 
 **display_ip_address** | **bool**| Display user IP address | [optional] 
 **display_time** | **bool**| Display time | [optional] 
 **display_workspace_name** | **bool**| Display workspace name | [optional] 

### Return type

[**CustomWatermarkSetting**](CustomWatermarkSetting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

