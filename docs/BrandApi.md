# BrandApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getBrandSettings**](BrandApi.md#getBrandSettings) | **GET** /v1/brand-settings | Get brand settings |
| [**upsertBrandSettings**](BrandApi.md#upsertBrandSettings) | **POST** /v1/brand-settings | Upsert brand settings |


<a id="getBrandSettings"></a>
# **getBrandSettings**
> BrandSettings getBrandSettings()

Get brand settings

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.BrandApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BrandApi apiInstance = new BrandApi(defaultClient);
    try {
      BrandSettings result = apiInstance.getBrandSettings();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandApi#getBrandSettings");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**BrandSettings**](BrandSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="upsertBrandSettings"></a>
# **upsertBrandSettings**
> BrandSettings upsertBrandSettings(upsertBrandSettingsRequest)

Upsert brand settings

Creates or replaces white-label brand settings for the account.

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.BrandApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BrandApi apiInstance = new BrandApi(defaultClient);
    UpsertBrandSettingsRequest upsertBrandSettingsRequest = new UpsertBrandSettingsRequest(); // UpsertBrandSettingsRequest | Brand settings
    try {
      BrandSettings result = apiInstance.upsertBrandSettings(upsertBrandSettingsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandApi#upsertBrandSettings");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **upsertBrandSettingsRequest** | [**UpsertBrandSettingsRequest**](UpsertBrandSettingsRequest.md)| Brand settings | |

### Return type

[**BrandSettings**](BrandSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

