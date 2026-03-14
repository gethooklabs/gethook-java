# CustomDomainsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCustomDomain**](CustomDomainsApi.md#createCustomDomain) | **POST** /v1/custom-domains | Create custom domain |
| [**listCustomDomains**](CustomDomainsApi.md#listCustomDomains) | **GET** /v1/custom-domains | List custom domains |


<a id="createCustomDomain"></a>
# **createCustomDomain**
> CustomDomain createCustomDomain(createCustomDomainRequest)

Create custom domain

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.CustomDomainsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CustomDomainsApi apiInstance = new CustomDomainsApi(defaultClient);
    CreateCustomDomainRequest createCustomDomainRequest = new CreateCustomDomainRequest(); // CreateCustomDomainRequest | Domain details
    try {
      CustomDomain result = apiInstance.createCustomDomain(createCustomDomainRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomDomainsApi#createCustomDomain");
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
| **createCustomDomainRequest** | [**CreateCustomDomainRequest**](CreateCustomDomainRequest.md)| Domain details | |

### Return type

[**CustomDomain**](CustomDomain.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Bad Request |  -  |

<a id="listCustomDomains"></a>
# **listCustomDomains**
> List&lt;CustomDomain&gt; listCustomDomains()

List custom domains

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.CustomDomainsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CustomDomainsApi apiInstance = new CustomDomainsApi(defaultClient);
    try {
      List<CustomDomain> result = apiInstance.listCustomDomains();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomDomainsApi#listCustomDomains");
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

[**List&lt;CustomDomain&gt;**](CustomDomain.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

