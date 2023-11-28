# Swagger\Client\SettingsApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSetting**](SettingsApi.md#createsetting) | **POST** /settings/ | Create Setting
[**deleteSetting**](SettingsApi.md#deletesetting) | **DELETE** /settings/{settingId}/ | Delete Setting
[**getSetting**](SettingsApi.md#getsetting) | **GET** /settings/{settingId}/ | Get Setting
[**getSettings**](SettingsApi.md#getsettings) | **GET** /settings/ | Get Settings
[**updateSetting**](SettingsApi.md#updatesetting) | **PUT** /settings/{settingId}/ | Update Setting

# **createSetting**
> \Swagger\Client\Model\Setting createSetting($body)

Create Setting

Create a new setting in the database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\SettingBody(); // \Swagger\Client\Model\SettingBody | 

try {
    $result = $apiInstance->createSetting($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->createSetting: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\SettingBody**](../Model/SettingBody.md)|  |

### Return type

[**\Swagger\Client\Model\Setting**](../Model/Setting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteSetting**
> deleteSetting($setting_id)

Delete Setting

Delete a specific setting in the database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$setting_id = "setting_id_example"; // string | 

try {
    $apiInstance->deleteSetting($setting_id);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->deleteSetting: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **setting_id** | **string**|  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSetting**
> \Swagger\Client\Model\Setting getSetting($setting_id)

Get Setting

Get the a specific setting from the database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$setting_id = "setting_id_example"; // string | 

try {
    $result = $apiInstance->getSetting($setting_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getSetting: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **setting_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\Setting**](../Model/Setting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSettings**
> \Swagger\Client\Model\SettingsResponse getSettings($search)

Get Settings

Get the entire list of settings available in the database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$search = ""; // string | The setting to search

try {
    $result = $apiInstance->getSettings($search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search** | **string**| The setting to search | [optional]

### Return type

[**\Swagger\Client\Model\SettingsResponse**](../Model/SettingsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateSetting**
> \Swagger\Client\Model\Setting updateSetting($body, $setting_id)

Update Setting

Update a specific setting in the database if it exists

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\SettingBody(); // \Swagger\Client\Model\SettingBody | 
$setting_id = "setting_id_example"; // string | 

try {
    $result = $apiInstance->updateSetting($body, $setting_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->updateSetting: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\SettingBody**](../Model/SettingBody.md)|  |
 **setting_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\Setting**](../Model/Setting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

