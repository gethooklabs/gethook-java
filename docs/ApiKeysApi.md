# ApiKeysApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createApiKey**](ApiKeysApi.md#createApiKey) | **POST** /v1/api-keys | Create API key |
| [**deleteApiKey**](ApiKeysApi.md#deleteApiKey) | **DELETE** /v1/api-keys/{id} | Revoke API key |
| [**listApiKeys**](ApiKeysApi.md#listApiKeys) | **GET** /v1/api-keys | List API keys |


<a id="createApiKey"></a>
# **createApiKey**
> APIKeyWithSecret createApiKey(createAPIKeyRequest)

Create API key

Creates a new API key for the authenticated account. The full key is only returned once.

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    CreateAPIKeyRequest createAPIKeyRequest = new CreateAPIKeyRequest(); // CreateAPIKeyRequest | Key name
    try {
      APIKeyWithSecret result = apiInstance.createApiKey(createAPIKeyRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#createApiKey");
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
| **createAPIKeyRequest** | [**CreateAPIKeyRequest**](CreateAPIKeyRequest.md)| Key name | |

### Return type

[**APIKeyWithSecret**](APIKeyWithSecret.md)

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

<a id="deleteApiKey"></a>
# **deleteApiKey**
> deleteApiKey(id)

Revoke API key

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    String id = "id_example"; // String | API key UUID
    try {
      apiInstance.deleteApiKey(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#deleteApiKey");
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
| **id** | **String**| API key UUID | |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | No Content |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

<a id="listApiKeys"></a>
# **listApiKeys**
> List&lt;APIKey&gt; listApiKeys()

List API keys

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    try {
      List<APIKey> result = apiInstance.listApiKeys();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#listApiKeys");
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

[**List&lt;APIKey&gt;**](APIKey.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

