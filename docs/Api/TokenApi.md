# VentureLeap\ConfigurationService\TokenApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**postCredentialsItem**](TokenApi.md#postcredentialsitem) | **POST** /get-token | Get JWT token to login.

# **postCredentialsItem**
> \VentureLeap\ConfigurationService\Model\Token postCredentialsItem($body)

Get JWT token to login.

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
$body = new \VentureLeap\ConfigurationService\Model\Credentials(); // \VentureLeap\ConfigurationService\Model\Credentials | Create new JWT Token

try {
    $result = $apiInstance->postCredentialsItem($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenApi->postCredentialsItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\ConfigurationService\Model\Credentials**](../Model/Credentials.md)| Create new JWT Token | [optional]

### Return type

[**\VentureLeap\ConfigurationService\Model\Token**](../Model/Token.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

