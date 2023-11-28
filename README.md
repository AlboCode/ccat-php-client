# SwaggerClient-php
Customizable AI architecture

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 0.0.5
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/AlboCode/ccat-php-client.git"
    }
  ],
  "require": {
    "albocode/ccat-php-client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to */*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*EmbedderApi* | [**getEmbedderSettings**](docs/Api/EmbedderApi.md#getembeddersettings) | **GET** /embedder/settings/{languageEmbedderName}/ | Get Embedder Settings
*EmbedderApi* | [**getEmbeddersSettings**](docs/Api/EmbedderApi.md#getembedderssettings) | **GET** /embedder/settings/ | Get Embedders Settings
*EmbedderApi* | [**upsertEmbedderSetting**](docs/Api/EmbedderApi.md#upsertembeddersetting) | **PUT** /embedder/settings/{languageEmbedderName}/ | Upsert Embedder Setting
*LargeLanguageModelApi* | [**getLlmSettings**](docs/Api/LargeLanguageModelApi.md#getllmsettings) | **GET** /llm/settings/{languageModelName}/ | Get Llm Settings
*LargeLanguageModelApi* | [**getLlmsSettings**](docs/Api/LargeLanguageModelApi.md#getllmssettings) | **GET** /llm/settings/ | Get LLMs Settings
*LargeLanguageModelApi* | [**upsertLlmSetting**](docs/Api/LargeLanguageModelApi.md#upsertllmsetting) | **PUT** /llm/settings/{languageModelName}/ | Upsert LLM Setting
*MemoryApi* | [**deletePointInMemory**](docs/Api/MemoryApi.md#deletepointinmemory) | **DELETE** /memory/collections/{collection_id}/points/{memory_id}/ | Delete Point In Memory
*MemoryApi* | [**getCollections**](docs/Api/MemoryApi.md#getcollections) | **GET** /memory/collections/ | Get Collections
*MemoryApi* | [**getConversationHistory**](docs/Api/MemoryApi.md#getconversationhistory) | **GET** /memory/conversation_history/ | Get Conversation History
*MemoryApi* | [**recallMemoriesFromText**](docs/Api/MemoryApi.md#recallmemoriesfromtext) | **GET** /memory/recall/ | Recall Memories From Text
*MemoryApi* | [**wipeCollections**](docs/Api/MemoryApi.md#wipecollections) | **DELETE** /memory/collections/ | Wipe Collections
*MemoryApi* | [**wipeConversationHistory**](docs/Api/MemoryApi.md#wipeconversationhistory) | **DELETE** /memory/conversation_history/ | Wipe Conversation History
*MemoryApi* | [**wipeMemoryPoints**](docs/Api/MemoryApi.md#wipememorypoints) | **DELETE** /memory/collections/{collection_id}/points/ | Wipe Memory Points By Metadata
*MemoryApi* | [**wipeSingleCollection**](docs/Api/MemoryApi.md#wipesinglecollection) | **DELETE** /memory/collections/{collection_id}/ | Wipe Single Collection
*PluginsApi* | [**deletePlugin**](docs/Api/PluginsApi.md#deleteplugin) | **DELETE** /plugins/{plugin_id} | Delete Plugin
*PluginsApi* | [**getPluginDetails**](docs/Api/PluginsApi.md#getplugindetails) | **GET** /plugins/{plugin_id} | Get Plugin Details
*PluginsApi* | [**getPluginSettings**](docs/Api/PluginsApi.md#getpluginsettings) | **GET** /plugins/settings/{plugin_id} | Get Plugin Settings
*PluginsApi* | [**getPluginsSettings**](docs/Api/PluginsApi.md#getpluginssettings) | **GET** /plugins/settings/ | Get Plugins Settings
*PluginsApi* | [**installPlugin**](docs/Api/PluginsApi.md#installplugin) | **POST** /plugins/upload/ | Install Plugin
*PluginsApi* | [**installPluginFromRegistry**](docs/Api/PluginsApi.md#installpluginfromregistry) | **POST** /plugins/upload/registry | Install Plugin From Registry
*PluginsApi* | [**listAvailablePlugins**](docs/Api/PluginsApi.md#listavailableplugins) | **GET** /plugins/ | List Available Plugins
*PluginsApi* | [**togglePlugin**](docs/Api/PluginsApi.md#toggleplugin) | **PUT** /plugins/toggle/{plugin_id} | Toggle Plugin
*PluginsApi* | [**upsertPluginSettings**](docs/Api/PluginsApi.md#upsertpluginsettings) | **PUT** /plugins/settings/{plugin_id} | Upsert Plugin Settings
*RabbitHoleApi* | [**getAllowedMimetypes**](docs/Api/RabbitHoleApi.md#getallowedmimetypes) | **GET** /rabbithole/allowed-mimetypes/ | Get Allowed Mimetypes
*RabbitHoleApi* | [**uploadFile**](docs/Api/RabbitHoleApi.md#uploadfile) | **POST** /rabbithole/ | Upload File
*RabbitHoleApi* | [**uploadMemory**](docs/Api/RabbitHoleApi.md#uploadmemory) | **POST** /rabbithole/memory/ | Upload Memory
*RabbitHoleApi* | [**uploadUrl**](docs/Api/RabbitHoleApi.md#uploadurl) | **POST** /rabbithole/web/ | Upload URL
*SettingsApi* | [**createSetting**](docs/Api/SettingsApi.md#createsetting) | **POST** /settings/ | Create Setting
*SettingsApi* | [**deleteSetting**](docs/Api/SettingsApi.md#deletesetting) | **DELETE** /settings/{settingId}/ | Delete Setting
*SettingsApi* | [**getSetting**](docs/Api/SettingsApi.md#getsetting) | **GET** /settings/{settingId}/ | Get Setting
*SettingsApi* | [**getSettings**](docs/Api/SettingsApi.md#getsettings) | **GET** /settings/ | Get Settings
*SettingsApi* | [**updateSetting**](docs/Api/SettingsApi.md#updatesetting) | **PUT** /settings/{settingId}/ | Update Setting
*StatusApi* | [**home**](docs/Api/StatusApi.md#home) | **GET** / | Home

## Documentation For Models

 - [BodyInstallPlugin](docs/Model/BodyInstallPlugin.md)
 - [BodyUploadFile](docs/Model/BodyUploadFile.md)
 - [BodyUploadMemory](docs/Model/BodyUploadMemory.md)
 - [BodyUploadUrl](docs/Model/BodyUploadUrl.md)
 - [Collection](docs/Model/Collection.md)
 - [CollectionData](docs/Model/CollectionData.md)
 - [CollectionsList](docs/Model/CollectionsList.md)
 - [ConversationHistory](docs/Model/ConversationHistory.md)
 - [ConversationMessage](docs/Model/ConversationMessage.md)
 - [DeleteResponse](docs/Model/DeleteResponse.md)
 - [Detail](docs/Model/Detail.md)
 - [FileResponse](docs/Model/FileResponse.md)
 - [Filters](docs/Model/Filters.md)
 - [HTTPValidationError](docs/Model/HTTPValidationError.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [MemoryRecall](docs/Model/MemoryRecall.md)
 - [MetaData](docs/Model/MetaData.md)
 - [OneOfDeleteResponseDeleted](docs/Model/OneOfDeleteResponseDeleted.md)
 - [Plugin](docs/Model/Plugin.md)
 - [PluginHooks](docs/Model/PluginHooks.md)
 - [PluginTools](docs/Model/PluginTools.md)
 - [PluginsList](docs/Model/PluginsList.md)
 - [QueryData](docs/Model/QueryData.md)
 - [ResponseGetAllowedMimetypes](docs/Model/ResponseGetAllowedMimetypes.md)
 - [Setting](docs/Model/Setting.md)
 - [SettingBody](docs/Model/SettingBody.md)
 - [SettingsResponse](docs/Model/SettingsResponse.md)
 - [Status](docs/Model/Status.md)
 - [ToggleResponse](docs/Model/ToggleResponse.md)
 - [VectorsData](docs/Model/VectorsData.md)
 - [WebResponse](docs/Model/WebResponse.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author



