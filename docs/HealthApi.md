# HealthApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**healthz**](HealthApi.md#healthz) | **GET** /healthz | Liveness check |
| [**readyz**](HealthApi.md#readyz) | **GET** /readyz | Readiness check |


<a id="healthz"></a>
# **healthz**
> Map&lt;String, String&gt; healthz()

Liveness check

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.models.*;
import dev.gethook.api.HealthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");

    HealthApi apiInstance = new HealthApi(defaultClient);
    try {
      Map<String, String> result = apiInstance.healthz();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HealthApi#healthz");
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

**Map&lt;String, String&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="readyz"></a>
# **readyz**
> Map&lt;String, String&gt; readyz()

Readiness check

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.models.*;
import dev.gethook.api.HealthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");

    HealthApi apiInstance = new HealthApi(defaultClient);
    try {
      Map<String, String> result = apiInstance.readyz();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HealthApi#readyz");
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

**Map&lt;String, String&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **503** | Service Unavailable |  -  |

