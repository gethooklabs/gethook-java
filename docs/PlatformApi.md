# PlatformApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getPlatformStats**](PlatformApi.md#getPlatformStats) | **GET** /v1/platform-stats | Public platform statistics |


<a id="getPlatformStats"></a>
# **getPlatformStats**
> PlatformStats getPlatformStats()

Public platform statistics

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.models.*;
import dev.gethook.api.PlatformApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");

    PlatformApi apiInstance = new PlatformApi(defaultClient);
    try {
      PlatformStats result = apiInstance.getPlatformStats();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PlatformApi#getPlatformStats");
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

[**PlatformStats**](PlatformStats.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

