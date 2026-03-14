# AccountsApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAccount**](AccountsApi.md#createAccount) | **POST** /v1/accounts | Create account |


<a id="createAccount"></a>
# **createAccount**
> AccountBootstrapData createAccount(createAccountRequest)

Create account

Creates a new account and returns a bootstrap API key. No authentication required.

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.models.*;
import dev.gethook.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    CreateAccountRequest createAccountRequest = new CreateAccountRequest(); // CreateAccountRequest | Account name
    try {
      AccountBootstrapData result = apiInstance.createAccount(createAccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#createAccount");
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
| **createAccountRequest** | [**CreateAccountRequest**](CreateAccountRequest.md)| Account name | |

### Return type

[**AccountBootstrapData**](AccountBootstrapData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Bad Request |  -  |

