# Swagger\Client\LargeLanguageModelApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getLlmSettings**](LargeLanguageModelApi.md#getllmsettings) | **GET** /llm/settings/{languageModelName}/ | Get Llm Settings
[**getLlmsSettings**](LargeLanguageModelApi.md#getllmssettings) | **GET** /llm/settings/ | Get LLMs Settings
[**upsertLlmSetting**](LargeLanguageModelApi.md#upsertllmsetting) | **PUT** /llm/settings/{languageModelName}/ | Upsert LLM Setting

# **getLlmSettings**
> \Swagger\Client\Model\Setting getLlmSettings($language_model_name)

Get Llm Settings

Get settings and schema of the specified Large Language Model

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LargeLanguageModelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$language_model_name = "language_model_name_example"; // string | 

try {
    $result = $apiInstance->getLlmSettings($language_model_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LargeLanguageModelApi->getLlmSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **language_model_name** | **string**|  |

### Return type

[**\Swagger\Client\Model\Setting**](../Model/Setting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLlmsSettings**
> \Swagger\Client\Model\SettingsResponse getLlmsSettings()

Get LLMs Settings

Get the list of the Large Language Models

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LargeLanguageModelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getLlmsSettings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LargeLanguageModelApi->getLlmsSettings: ', $e->getMessage(), PHP_EOL;
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

# **upsertLlmSetting**
> \Swagger\Client\Model\Setting upsertLlmSetting($body, $language_model_name)

Upsert LLM Setting

Upsert the Large Language Model setting

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LargeLanguageModelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \stdClass; // object | 
$language_model_name = "language_model_name_example"; // string | 

try {
    $result = $apiInstance->upsertLlmSetting($body, $language_model_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LargeLanguageModelApi->upsertLlmSetting: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**object**](../Model/object.md)|  |
 **language_model_name** | **string**|  |

### Return type

[**\Swagger\Client\Model\Setting**](../Model/Setting.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

