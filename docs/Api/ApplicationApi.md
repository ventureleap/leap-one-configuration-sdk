# VentureLeap\ConfigurationService\ApplicationApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApplicationItem**](ApplicationApi.md#deleteapplicationitem) | **DELETE** /applications/{id} | Removes the Application resource.
[**getApplicationCollection**](ApplicationApi.md#getapplicationcollection) | **GET** /applications | Retrieves the collection of Application resources.
[**getApplicationItem**](ApplicationApi.md#getapplicationitem) | **GET** /applications/{id} | Retrieves a Application resource.
[**getTokenPost**](ApplicationApi.md#gettokenpost) | **POST** /get-token | 
[**postApplicationCollection**](ApplicationApi.md#postapplicationcollection) | **POST** /applications | Creates a Application resource.
[**putApplicationItem**](ApplicationApi.md#putapplicationitem) | **PUT** /applications/{id} | Replaces the Application resource.

# **deleteApplicationItem**
> deleteApplicationItem($id)

Removes the Application resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApplicationItem($id);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->deleteApplicationItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApplicationCollection**
> \VentureLeap\ConfigurationService\Model\InlineResponse200 getApplicationCollection($page)

Retrieves the collection of Application resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


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

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApplicationItem**
> \VentureLeap\ConfigurationService\Model\ApplicationJsonldRead getApplicationItem($id)

Retrieves a Application resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getApplicationItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->getApplicationItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\ConfigurationService\Model\ApplicationJsonldRead**](../Model/ApplicationJsonldRead.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTokenPost**
> \VentureLeap\ConfigurationService\Model\ApplicationJsonldRead getTokenPost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite(); // \VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite | 

try {
    $result = $apiInstance->getTokenPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->getTokenPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite**](../Model/ApplicationJsonldWrite.md)|  | [optional]

### Return type

[**\VentureLeap\ConfigurationService\Model\ApplicationJsonldRead**](../Model/ApplicationJsonldRead.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json
 - **Accept**: application/ld+json, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTokenPost**
> \VentureLeap\ConfigurationService\Model\ApplicationJsonldRead getTokenPost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\ConfigurationService\Model\Credentials(); // \VentureLeap\ConfigurationService\Model\Credentials | 

try {
    $result = $apiInstance->getTokenPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->getTokenPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\ConfigurationService\Model\Credentials**](../Model/Credentials.md)|  | [optional]

### Return type

[**\VentureLeap\ConfigurationService\Model\ApplicationJsonldRead**](../Model/ApplicationJsonldRead.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json
 - **Accept**: application/ld+json, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApplicationCollection**
> \VentureLeap\ConfigurationService\Model\ApplicationJsonldRead postApplicationCollection($body)

Creates a Application resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite(); // \VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite | The new Application resource

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
 **body** | [**\VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite**](../Model/ApplicationJsonldWrite.md)| The new Application resource | [optional]

### Return type

[**\VentureLeap\ConfigurationService\Model\ApplicationJsonldRead**](../Model/ApplicationJsonldRead.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApplicationItem**
> \VentureLeap\ConfigurationService\Model\ApplicationJsonldRead putApplicationItem($id, $body)

Replaces the Application resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\ConfigurationService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\ConfigurationService\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite(); // \VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite | The updated Application resource

try {
    $result = $apiInstance->putApplicationItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->putApplicationItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\VentureLeap\ConfigurationService\Model\ApplicationJsonldWrite**](../Model/ApplicationJsonldWrite.md)| The updated Application resource | [optional]

### Return type

[**\VentureLeap\ConfigurationService\Model\ApplicationJsonldRead**](../Model/ApplicationJsonldRead.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

