# Swagger\Client\StatusApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**home**](StatusApi.md#home) | **GET** / | Home

# **home**
> \Swagger\Client\Model\Status home()

Home

Server status

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\StatusApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->home();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusApi->home: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Status**](../Model/Status.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

