# VentureLeap\ConfigurationService\ApplicationApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApplicationItem**](ApplicationApi.md#deleteapplicationitem) | **DELETE** /configuration/applications/{uuid} | Removes the Application resource.
[**getApplicationCollection**](ApplicationApi.md#getapplicationcollection) | **GET** /configuration/applications | Retrieves the collection of Application resources.
[**getApplicationItem**](ApplicationApi.md#getapplicationitem) | **GET** /configuration/applications/{uuid} | Retrieves a Application resource.
[**postApplicationCollection**](ApplicationApi.md#postapplicationcollection) | **POST** /configuration/applications | Creates a Application resource.
[**putApplicationItem**](ApplicationApi.md#putapplicationitem) | **PUT** /configuration/applications/{uuid} | Replaces the Application resource.

# **deleteApplicationItem**
> deleteApplicationItem($uuid)

Removes the Application resource.

Removes the Application resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = "uuid_example"; // string | Resource identifier

try {
    $apiInstance->deleteApplicationItem($uuid);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->deleteApplicationItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| Resource identifier |

### Return type

void (empty response body)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApplicationCollection**
> \VentureLeap\ConfigurationService\Model\InlineResponse200 getApplicationCollection($page)

Retrieves the collection of Application resources.

Retrieves the collection of Application resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->getApplicationCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->getApplicationCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**\VentureLeap\ConfigurationService\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApplicationItem**
> \VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationRead getApplicationItem($uuid)

Retrieves a Application resource.

Retrieves a Application resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = "uuid_example"; // string | Resource identifier

try {
    $result = $apiInstance->getApplicationItem($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->getApplicationItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| Resource identifier |

### Return type

[**\VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationRead**](../Model/ApplicationJsonldAppplicationRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApplicationCollection**
> \VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationRead postApplicationCollection($body)

Creates a Application resource.

Creates a Application resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationWrite(); // \VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationWrite | The new Application resource

try {
    $result = $apiInstance->postApplicationCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->postApplicationCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationWrite**](../Model/ApplicationJsonldAppplicationWrite.md)| The new Application resource |

### Return type

[**\VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationRead**](../Model/ApplicationJsonldAppplicationRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApplicationItem**
> \VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationRead putApplicationItem($body, $uuid)

Replaces the Application resource.

Replaces the Application resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationWrite(); // \VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationWrite | The updated Application resource
$uuid = "uuid_example"; // string | Resource identifier

try {
    $result = $apiInstance->putApplicationItem($body, $uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->putApplicationItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationWrite**](../Model/ApplicationJsonldAppplicationWrite.md)| The updated Application resource |
 **uuid** | **string**| Resource identifier |

### Return type

[**\VentureLeap\ConfigurationService\Model\ApplicationJsonldAppplicationRead**](../Model/ApplicationJsonldAppplicationRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

