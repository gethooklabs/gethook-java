# AuthApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**login**](AuthApi.md#login) | **POST** /v1/auth/login | Login with email and password |
| [**register**](AuthApi.md#register) | **POST** /v1/auth/register | Register with email and password |


<a id="login"></a>
# **login**
> AccountBootstrapData login(loginRequest)

Login with email and password

Authenticates with email/password and returns a fresh API key on success.

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.models.*;
import dev.gethook.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");

    AuthApi apiInstance = new AuthApi(defaultClient);
    LoginRequest loginRequest = new LoginRequest(); // LoginRequest | Login credentials
    try {
      AccountBootstrapData result = apiInstance.login(loginRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#login");
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
| **loginRequest** | [**LoginRequest**](LoginRequest.md)| Login credentials | |

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
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **401** | Unauthorized |  -  |

<a id="register"></a>
# **register**
> AccountBootstrapData register(registerRequest)

Register with email and password

Creates a new account with email/password credentials and returns a bootstrap API key.

### Example
```java
// Import classes:
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.models.*;
import dev.gethook.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080");

    AuthApi apiInstance = new AuthApi(defaultClient);
    RegisterRequest registerRequest = new RegisterRequest(); // RegisterRequest | Registration details
    try {
      AccountBootstrapData result = apiInstance.register(registerRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#register");
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
| **registerRequest** | [**RegisterRequest**](RegisterRequest.md)| Registration details | |

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
| **409** | Conflict |  -  |

