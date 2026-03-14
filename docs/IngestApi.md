# IngestApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**ingest**](IngestApi.md#ingest) | **POST** /ingest/{token} | Ingest webhook event |


<a id="ingest"></a>
# **ingest**
> IngestAcceptedData ingest(token)

Ingest webhook event

Accepts an inbound webhook. The path token authenticates the source — no Bearer header required.

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.models.*;
import dev.gethook.api.IngestApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");

    IngestApi apiInstance = new IngestApi(defaultClient);
    String token = "token_example"; // String | Source path token (src_...)
    try {
      IngestAcceptedData result = apiInstance.ingest(token);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IngestApi#ingest");
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
| **token** | **String**| Source path token (src_...) | |

### Return type

[**IngestAcceptedData**](IngestAcceptedData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Accepted |  -  |
| **404** | Not Found |  -  |

