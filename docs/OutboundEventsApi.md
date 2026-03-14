# OutboundEventsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getOutboundEvent**](OutboundEventsApi.md#getOutboundEvent) | **GET** /v1/outbound-events/{id} | Get outbound event |
| [**listOutboundEvents**](OutboundEventsApi.md#listOutboundEvents) | **GET** /v1/outbound-events | List outbound events |
| [**publishOutboundEvent**](OutboundEventsApi.md#publishOutboundEvent) | **POST** /v1/outbound-events | Publish outbound event |
| [**replayOutboundEvent**](OutboundEventsApi.md#replayOutboundEvent) | **POST** /v1/outbound-events/{id}/replay | Replay outbound event |


<a id="getOutboundEvent"></a>
# **getOutboundEvent**
> EventDetailData getOutboundEvent(id)

Get outbound event

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.OutboundEventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    OutboundEventsApi apiInstance = new OutboundEventsApi(defaultClient);
    String id = "id_example"; // String | Event UUID
    try {
      EventDetailData result = apiInstance.getOutboundEvent(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OutboundEventsApi#getOutboundEvent");
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
| **id** | **String**| Event UUID | |

### Return type

[**EventDetailData**](EventDetailData.md)

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

<a id="listOutboundEvents"></a>
# **listOutboundEvents**
> EventListData listOutboundEvents(limit, offset)

List outbound events

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.OutboundEventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    OutboundEventsApi apiInstance = new OutboundEventsApi(defaultClient);
    Integer limit = 56; // Integer | Max results (default 25, max 200)
    Integer offset = 56; // Integer | Pagination offset
    try {
      EventListData result = apiInstance.listOutboundEvents(limit, offset);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OutboundEventsApi#listOutboundEvents");
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
| **limit** | **Integer**| Max results (default 25, max 200) | [optional] |
| **offset** | **Integer**| Pagination offset | [optional] |

### Return type

[**EventListData**](EventListData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="publishOutboundEvent"></a>
# **publishOutboundEvent**
> PublishOutboundData publishOutboundEvent(publishOutboundEventRequest)

Publish outbound event

Queues a new outbound event for delivery to all matching route destinations.

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.OutboundEventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    OutboundEventsApi apiInstance = new OutboundEventsApi(defaultClient);
    PublishOutboundEventRequest publishOutboundEventRequest = new PublishOutboundEventRequest(); // PublishOutboundEventRequest | Event payload
    try {
      PublishOutboundData result = apiInstance.publishOutboundEvent(publishOutboundEventRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OutboundEventsApi#publishOutboundEvent");
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
| **publishOutboundEventRequest** | [**PublishOutboundEventRequest**](PublishOutboundEventRequest.md)| Event payload | |

### Return type

[**PublishOutboundData**](PublishOutboundData.md)

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

<a id="replayOutboundEvent"></a>
# **replayOutboundEvent**
> ReplayEventData replayOutboundEvent(id)

Replay outbound event

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.auth.*;
import dev.gethook.models.*;
import dev.gethook.api.OutboundEventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    OutboundEventsApi apiInstance = new OutboundEventsApi(defaultClient);
    String id = "id_example"; // String | Event UUID
    try {
      ReplayEventData result = apiInstance.replayOutboundEvent(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OutboundEventsApi#replayOutboundEvent");
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
| **id** | **String**| Event UUID | |

### Return type

[**ReplayEventData**](ReplayEventData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Accepted |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

