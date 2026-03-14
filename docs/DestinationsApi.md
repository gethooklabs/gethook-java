# DestinationsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDestination**](DestinationsApi.md#createDestination) | **POST** /v1/destinations | Create destination |
| [**getDestination**](DestinationsApi.md#getDestination) | **GET** /v1/destinations/{id} | Get destination |
| [**listDestinationPresets**](DestinationsApi.md#listDestinationPresets) | **GET** /v1/destination-presets | List destination presets |
| [**listDestinations**](DestinationsApi.md#listDestinations) | **GET** /v1/destinations | List destinations |
| [**rotateDestinationSecret**](DestinationsApi.md#rotateDestinationSecret) | **POST** /v1/destinations/{id}/rotate-secret | Rotate destination signing secret |
| [**updateDestination**](DestinationsApi.md#updateDestination) | **PATCH** /v1/destinations/{id} | Update destination |


<a id="createDestination"></a>
# **createDestination**
> Destination createDestination(createDestinationRequest)

Create destination

Creates a new webhook delivery destination. The signing_secret is encrypted at rest and never returned.

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.DestinationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DestinationsApi apiInstance = new DestinationsApi(defaultClient);
    CreateDestinationRequest createDestinationRequest = new CreateDestinationRequest(); // CreateDestinationRequest | Destination config
    try {
      Destination result = apiInstance.createDestination(createDestinationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DestinationsApi#createDestination");
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
| **createDestinationRequest** | [**CreateDestinationRequest**](CreateDestinationRequest.md)| Destination config | |

### Return type

[**Destination**](Destination.md)

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

<a id="getDestination"></a>
# **getDestination**
> Destination getDestination(id)

Get destination

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.DestinationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DestinationsApi apiInstance = new DestinationsApi(defaultClient);
    String id = "id_example"; // String | Destination UUID
    try {
      Destination result = apiInstance.getDestination(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DestinationsApi#getDestination");
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
| **id** | **String**| Destination UUID | |

### Return type

[**Destination**](Destination.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

<a id="listDestinationPresets"></a>
# **listDestinationPresets**
> List&lt;DestinationPreset&gt; listDestinationPresets()

List destination presets

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.models.*;
import dev.gethook.api.DestinationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");

    DestinationsApi apiInstance = new DestinationsApi(defaultClient);
    try {
      List<DestinationPreset> result = apiInstance.listDestinationPresets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DestinationsApi#listDestinationPresets");
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

[**List&lt;DestinationPreset&gt;**](DestinationPreset.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listDestinations"></a>
# **listDestinations**
> List&lt;Destination&gt; listDestinations()

List destinations

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.DestinationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DestinationsApi apiInstance = new DestinationsApi(defaultClient);
    try {
      List<Destination> result = apiInstance.listDestinations();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DestinationsApi#listDestinations");
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

[**List&lt;Destination&gt;**](Destination.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="rotateDestinationSecret"></a>
# **rotateDestinationSecret**
> Object rotateDestinationSecret(id, body)

Rotate destination signing secret

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.DestinationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DestinationsApi apiInstance = new DestinationsApi(defaultClient);
    String id = "id_example"; // String | Destination UUID
    Object body = null; // Object | New signing secret
    try {
      Object result = apiInstance.rotateDestinationSecret(id, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DestinationsApi#rotateDestinationSecret");
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
| **id** | **String**| Destination UUID | |
| **body** | **Object**| New signing secret | |

### Return type

**Object**

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
| **404** | Not Found |  -  |

<a id="updateDestination"></a>
# **updateDestination**
> Destination updateDestination(id, updateDestinationRequest)

Update destination

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.DestinationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DestinationsApi apiInstance = new DestinationsApi(defaultClient);
    String id = "id_example"; // String | Destination UUID
    UpdateDestinationRequest updateDestinationRequest = new UpdateDestinationRequest(); // UpdateDestinationRequest | Fields to update
    try {
      Destination result = apiInstance.updateDestination(id, updateDestinationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DestinationsApi#updateDestination");
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
| **id** | **String**| Destination UUID | |
| **updateDestinationRequest** | [**UpdateDestinationRequest**](UpdateDestinationRequest.md)| Fields to update | |

### Return type

[**Destination**](Destination.md)

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
| **404** | Not Found |  -  |

