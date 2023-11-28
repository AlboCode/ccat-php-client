# Swagger\Client\PluginsApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deletePlugin**](PluginsApi.md#deleteplugin) | **DELETE** /plugins/{plugin_id} | Delete Plugin
[**getPluginDetails**](PluginsApi.md#getplugindetails) | **GET** /plugins/{plugin_id} | Get Plugin Details
[**getPluginSettings**](PluginsApi.md#getpluginsettings) | **GET** /plugins/settings/{plugin_id} | Get Plugin Settings
[**getPluginsSettings**](PluginsApi.md#getpluginssettings) | **GET** /plugins/settings/ | Get Plugins Settings
[**installPlugin**](PluginsApi.md#installplugin) | **POST** /plugins/upload/ | Install Plugin
[**installPluginFromRegistry**](PluginsApi.md#installpluginfromregistry) | **POST** /plugins/upload/registry | Install Plugin From Registry
[**listAvailablePlugins**](PluginsApi.md#listavailableplugins) | **GET** /plugins/ | List Available Plugins
[**togglePlugin**](PluginsApi.md#toggleplugin) | **PUT** /plugins/toggle/{plugin_id} | Toggle Plugin
[**upsertPluginSettings**](PluginsApi.md#upsertpluginsettings) | **PUT** /plugins/settings/{plugin_id} | Upsert Plugin Settings

# **deletePlugin**
> \Swagger\Client\Model\DeleteResponse deletePlugin($plugin_id)

Delete Plugin

Physically remove a plugin

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$plugin_id = "plugin_id_example"; // string | 

try {
    $result = $apiInstance->deletePlugin($plugin_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->deletePlugin: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **plugin_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\DeleteResponse**](../Model/DeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPluginDetails**
> \Swagger\Client\Model\Plugin getPluginDetails($plugin_id)

Get Plugin Details

Returns information on a single plugin

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$plugin_id = "plugin_id_example"; // string | 

try {
    $result = $apiInstance->getPluginDetails($plugin_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->getPluginDetails: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **plugin_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\Plugin**](../Model/Plugin.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPluginSettings**
> \Swagger\Client\Model\InlineResponse200 getPluginSettings($plugin_id)

Get Plugin Settings

Returns the settings of a specific plugin

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$plugin_id = "plugin_id_example"; // string | 

try {
    $result = $apiInstance->getPluginSettings($plugin_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->getPluginSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **plugin_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPluginsSettings**
> \Swagger\Client\Model\SettingsResponse getPluginsSettings()

Get Plugins Settings

Returns the settings of all the plugins

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getPluginsSettings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->getPluginsSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\SettingsResponse**](../Model/SettingsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **installPlugin**
> \Swagger\Client\Model\FileResponse installPlugin($file)

Install Plugin

Install a new plugin from a zip file

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$file = "file_example"; // string | 

try {
    $result = $apiInstance->installPlugin($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->installPlugin: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **string****string**|  |

### Return type

[**\Swagger\Client\Model\FileResponse**](../Model/FileResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **installPluginFromRegistry**
> \Swagger\Client\Model\FileResponse installPluginFromRegistry($body)

Install Plugin From Registry

Install a new plugin from external repository

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\BodyUploadUrl(); // \Swagger\Client\Model\BodyUploadUrl | 

try {
    $result = $apiInstance->installPluginFromRegistry($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->installPluginFromRegistry: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\BodyUploadUrl**](../Model/BodyUploadUrl.md)|  |

### Return type

[**\Swagger\Client\Model\FileResponse**](../Model/FileResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listAvailablePlugins**
> \Swagger\Client\Model\PluginsList listAvailablePlugins($query)

List Available Plugins

List both installed and registry plugins

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$query = "query_example"; // string | 

try {
    $result = $apiInstance->listAvailablePlugins($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->listAvailablePlugins: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\PluginsList**](../Model/PluginsList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **togglePlugin**
> \Swagger\Client\Model\ToggleResponse togglePlugin($plugin_id)

Toggle Plugin

Enable or disable a single plugin

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$plugin_id = "plugin_id_example"; // string | 

try {
    $result = $apiInstance->togglePlugin($plugin_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->togglePlugin: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **plugin_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\ToggleResponse**](../Model/ToggleResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **upsertPluginSettings**
> \Swagger\Client\Model\Setting upsertPluginSettings($body, $plugin_id)

Upsert Plugin Settings

Updates the settings of a specific plugin

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PluginsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \stdClass; // object | 
$plugin_id = "plugin_id_example"; // string | 

try {
    $result = $apiInstance->upsertPluginSettings($body, $plugin_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginsApi->upsertPluginSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**object**](../Model/object.md)|  |
 **plugin_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\Setting**](../Model/Setting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

