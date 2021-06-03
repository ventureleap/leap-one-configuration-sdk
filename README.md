# SwaggerClient-php
No description provided (generated by Swagger Codegen https://github.com/swagger-api/swagger-codegen)

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 2.0.0
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
      "url": "https://github.com/ventureleap/leap-one-configuration-sdk.git"
    }
  ],
  "require": {
    "ventureleap/leap-one-configuration-sdk": "*@dev"
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

## Documentation for API Endpoints

All URIs are relative to */*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ApplicationApi* | [**deleteApplicationItem**](docs/Api/ApplicationApi.md#deleteapplicationitem) | **DELETE** /configuration/applications/{uuid} | Removes the Application resource.
*ApplicationApi* | [**getApplicationCollection**](docs/Api/ApplicationApi.md#getapplicationcollection) | **GET** /configuration/applications | Retrieves the collection of Application resources.
*ApplicationApi* | [**getApplicationItem**](docs/Api/ApplicationApi.md#getapplicationitem) | **GET** /configuration/applications/{uuid} | Retrieves a Application resource.
*ApplicationApi* | [**postApplicationCollection**](docs/Api/ApplicationApi.md#postapplicationcollection) | **POST** /configuration/applications | Creates a Application resource.
*ApplicationApi* | [**putApplicationItem**](docs/Api/ApplicationApi.md#putapplicationitem) | **PUT** /configuration/applications/{uuid} | Replaces the Application resource.
*ConfigurationEntryApi* | [**deleteConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#deleteconfigurationentryitem) | **DELETE** /configuration/configuration_entries/{uuid} | Removes the ConfigurationEntry resource.
*ConfigurationEntryApi* | [**getConfigurationEntryCollection**](docs/Api/ConfigurationEntryApi.md#getconfigurationentrycollection) | **GET** /configuration/configuration_entries | Retrieves the collection of ConfigurationEntry resources.
*ConfigurationEntryApi* | [**getConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#getconfigurationentryitem) | **GET** /configuration/configuration_entries/{uuid} | Retrieves a ConfigurationEntry resource.
*ConfigurationEntryApi* | [**postConfigurationEntryCollection**](docs/Api/ConfigurationEntryApi.md#postconfigurationentrycollection) | **POST** /configuration/configuration_entries | Creates a ConfigurationEntry resource.
*ConfigurationEntryApi* | [**putConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#putconfigurationentryitem) | **PUT** /configuration/configuration_entries/{uuid} | Replaces the ConfigurationEntry resource.

## Documentation For Models

 - [ApplicationJsonldAppplicationRead](docs/Model/ApplicationJsonldAppplicationRead.md)
 - [ApplicationJsonldAppplicationWrite](docs/Model/ApplicationJsonldAppplicationWrite.md)
 - [ConfigurationEntryJsonldConfigurationRead](docs/Model/ConfigurationEntryJsonldConfigurationRead.md)
 - [ConfigurationEntryJsonldConfigurationWrite](docs/Model/ConfigurationEntryJsonldConfigurationWrite.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [InlineResponse2001](docs/Model/InlineResponse2001.md)
 - [InlineResponse200Hydrasearch](docs/Model/InlineResponse200Hydrasearch.md)
 - [InlineResponse200HydrasearchHydramapping](docs/Model/InlineResponse200HydrasearchHydramapping.md)
 - [InlineResponse200Hydraview](docs/Model/InlineResponse200Hydraview.md)
 - [OneOfApplicationJsonldAppplicationReadContext](docs/Model/OneOfApplicationJsonldAppplicationReadContext.md)
 - [OneOfApplicationJsonldAppplicationWriteContext](docs/Model/OneOfApplicationJsonldAppplicationWriteContext.md)
 - [OneOfConfigurationEntryJsonldConfigurationReadContext](docs/Model/OneOfConfigurationEntryJsonldConfigurationReadContext.md)
 - [OneOfConfigurationEntryJsonldConfigurationWriteContext](docs/Model/OneOfConfigurationEntryJsonldConfigurationWriteContext.md)

## Documentation For Authorization


## apiKey

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author



