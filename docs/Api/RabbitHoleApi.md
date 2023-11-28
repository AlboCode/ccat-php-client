# Swagger\Client\RabbitHoleApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAllowedMimetypes**](RabbitHoleApi.md#getallowedmimetypes) | **GET** /rabbithole/allowed-mimetypes/ | Get Allowed Mimetypes
[**uploadFile**](RabbitHoleApi.md#uploadfile) | **POST** /rabbithole/ | Upload File
[**uploadMemory**](RabbitHoleApi.md#uploadmemory) | **POST** /rabbithole/memory/ | Upload Memory
[**uploadUrl**](RabbitHoleApi.md#uploadurl) | **POST** /rabbithole/web/ | Upload URL

# **getAllowedMimetypes**
> \Swagger\Client\Model\ResponseGetAllowedMimetypes getAllowedMimetypes()

Get Allowed Mimetypes

Retrieve the allowed mimetypes that can be ingested by the Rabbit Hole

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\RabbitHoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getAllowedMimetypes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RabbitHoleApi->getAllowedMimetypes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ResponseGetAllowedMimetypes**](../Model/ResponseGetAllowedMimetypes.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **uploadFile**
> \Swagger\Client\Model\FileResponse uploadFile($file)

Upload File

Upload a file containing text (.txt, .md, .pdf, etc.). File content will be extracted and segmented into chunks. Chunks will be then vectorized and stored into documents memory.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\RabbitHoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$file = "file_example"; // string | 

try {
    $result = $apiInstance->uploadFile($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RabbitHoleApi->uploadFile: ', $e->getMessage(), PHP_EOL;
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

# **uploadMemory**
> object uploadMemory($file)

Upload Memory

Upload a memory json file to the cat memory

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\RabbitHoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$file = "file_example"; // string | 

try {
    $result = $apiInstance->uploadMemory($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RabbitHoleApi->uploadMemory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **string****string**|  |

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **uploadUrl**
> \Swagger\Client\Model\WebResponse uploadUrl($body)

Upload URL

Upload a URL. Website content will be extracted and segmented into chunks. Chunks will be then vectorized and stored into documents memory.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\RabbitHoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\BodyUploadUrl(); // \Swagger\Client\Model\BodyUploadUrl | 

try {
    $result = $apiInstance->uploadUrl($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RabbitHoleApi->uploadUrl: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\BodyUploadUrl**](../Model/BodyUploadUrl.md)|  |

### Return type

[**\Swagger\Client\Model\WebResponse**](../Model/WebResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

