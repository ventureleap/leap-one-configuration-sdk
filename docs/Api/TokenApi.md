# VentureLeap\ConfigurationService\TokenApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTokenPost**](TokenApi.md#gettokenpost) | **POST** /get-token | 

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


$apiInstance = new VentureLeap\ConfigurationService\Api\TokenApi(
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
    echo 'Exception when calling TokenApi->getTokenPost: ', $e->getMessage(), PHP_EOL;
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


$apiInstance = new VentureLeap\ConfigurationService\Api\TokenApi(
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
    echo 'Exception when calling TokenApi->getTokenPost: ', $e->getMessage(), PHP_EOL;
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

