# Swagger\Client\EmbedderApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getEmbedderSettings**](EmbedderApi.md#getembeddersettings) | **GET** /embedder/settings/{languageEmbedderName}/ | Get Embedder Settings
[**getEmbeddersSettings**](EmbedderApi.md#getembedderssettings) | **GET** /embedder/settings/ | Get Embedders Settings
[**upsertEmbedderSetting**](EmbedderApi.md#upsertembeddersetting) | **PUT** /embedder/settings/{languageEmbedderName}/ | Upsert Embedder Setting

# **getEmbedderSettings**
> \Swagger\Client\Model\Setting getEmbedderSettings($language_embedder_name)

Get Embedder Settings

Get settings and schema of the specified Embedder

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\EmbedderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$language_embedder_name = "language_embedder_name_example"; // string | 

try {
    $result = $apiInstance->getEmbedderSettings($language_embedder_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmbedderApi->getEmbedderSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **language_embedder_name** | **string**|  |

### Return type

[**\Swagger\Client\Model\Setting**](../Model/Setting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getEmbeddersSettings**
> \Swagger\Client\Model\SettingsResponse getEmbeddersSettings()

Get Embedders Settings

Get the list of the Embedders

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\EmbedderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getEmbeddersSettings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmbedderApi->getEmbeddersSettings: ', $e->getMessage(), PHP_EOL;
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

# **upsertEmbedderSetting**
> \Swagger\Client\Model\Setting upsertEmbedderSetting($body, $language_embedder_name)

Upsert Embedder Setting

Upsert the Embedder setting

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\EmbedderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \stdClass; // object | 
$language_embedder_name = "language_embedder_name_example"; // string | 

try {
    $result = $apiInstance->upsertEmbedderSetting($body, $language_embedder_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmbedderApi->upsertEmbedderSetting: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**object**](../Model/object.md)|  |
 **language_embedder_name** | **string**|  |

### Return type

[**\Swagger\Client\Model\Setting**](../Model/Setting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

