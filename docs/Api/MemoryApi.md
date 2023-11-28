# Swagger\Client\MemoryApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deletePointInMemory**](MemoryApi.md#deletepointinmemory) | **DELETE** /memory/collections/{collection_id}/points/{memory_id}/ | Delete Point In Memory
[**getCollections**](MemoryApi.md#getcollections) | **GET** /memory/collections/ | Get Collections
[**getConversationHistory**](MemoryApi.md#getconversationhistory) | **GET** /memory/conversation_history/ | Get Conversation History
[**recallMemoriesFromText**](MemoryApi.md#recallmemoriesfromtext) | **GET** /memory/recall/ | Recall Memories From Text
[**wipeCollections**](MemoryApi.md#wipecollections) | **DELETE** /memory/collections/ | Wipe Collections
[**wipeConversationHistory**](MemoryApi.md#wipeconversationhistory) | **DELETE** /memory/conversation_history/ | Wipe Conversation History
[**wipeMemoryPoints**](MemoryApi.md#wipememorypoints) | **DELETE** /memory/collections/{collection_id}/points/ | Wipe Memory Points By Metadata
[**wipeSingleCollection**](MemoryApi.md#wipesinglecollection) | **DELETE** /memory/collections/{collection_id}/ | Wipe Single Collection

# **deletePointInMemory**
> \Swagger\Client\Model\DeleteResponse deletePointInMemory($collection_id, $memory_id)

Delete Point In Memory

Delete specific point in memory

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MemoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$collection_id = "collection_id_example"; // string | 
$memory_id = "memory_id_example"; // string | 

try {
    $result = $apiInstance->deletePointInMemory($collection_id, $memory_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MemoryApi->deletePointInMemory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_id** | **string**|  |
 **memory_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\DeleteResponse**](../Model/DeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCollections**
> \Swagger\Client\Model\CollectionsList getCollections()

Get Collections

Get list of available collections

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MemoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getCollections();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MemoryApi->getCollections: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\CollectionsList**](../Model/CollectionsList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConversationHistory**
> \Swagger\Client\Model\ConversationHistory getConversationHistory()

Get Conversation History

Get the specified user's conversation history from working memory

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MemoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getConversationHistory();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MemoryApi->getConversationHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ConversationHistory**](../Model/ConversationHistory.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **recallMemoriesFromText**
> \Swagger\Client\Model\MemoryRecall recallMemoriesFromText($text, $k)

Recall Memories From Text

Search k memories similar to given text.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MemoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$text = "text_example"; // string | Find memories similar to this text.
$k = 100; // int | How many memories to return.

try {
    $result = $apiInstance->recallMemoriesFromText($text, $k);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MemoryApi->recallMemoriesFromText: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **text** | **string**| Find memories similar to this text. |
 **k** | **int**| How many memories to return. | [optional] [default to 100]

### Return type

[**\Swagger\Client\Model\MemoryRecall**](../Model/MemoryRecall.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **wipeCollections**
> \Swagger\Client\Model\DeleteResponse wipeCollections()

Wipe Collections

Delete and create all collections

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MemoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->wipeCollections();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MemoryApi->wipeCollections: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\DeleteResponse**](../Model/DeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **wipeConversationHistory**
> \Swagger\Client\Model\DeleteResponse wipeConversationHistory()

Wipe Conversation History

Delete the specified user's conversation history from working memory

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MemoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->wipeConversationHistory();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MemoryApi->wipeConversationHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\DeleteResponse**](../Model/DeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **wipeMemoryPoints**
> \Swagger\Client\Model\DeleteResponse wipeMemoryPoints($collection_id, $body)

Wipe Memory Points By Metadata

Delete points in memory by filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MemoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$collection_id = "collection_id_example"; // string | 
$body = new \stdClass; // object | 

try {
    $result = $apiInstance->wipeMemoryPoints($collection_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MemoryApi->wipeMemoryPoints: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_id** | **string**|  |
 **body** | [**object**](../Model/object.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\DeleteResponse**](../Model/DeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **wipeSingleCollection**
> \Swagger\Client\Model\DeleteResponse wipeSingleCollection($collection_id)

Wipe Single Collection

Delete and recreate a collection

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MemoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$collection_id = "collection_id_example"; // string | 

try {
    $result = $apiInstance->wipeSingleCollection($collection_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MemoryApi->wipeSingleCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\DeleteResponse**](../Model/DeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

