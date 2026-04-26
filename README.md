# gethook-java — Java SDK

Java client for the [GetHook](https://gethook.io) Webhook Reliability Gateway API.

## Installation

**Maven:**
```xml
<dependency>
  <groupId>dev.gethook</groupId>
  <artifactId>gethook-java</artifactId>
  <version>0.1.0</version>
</dependency>
```

**Gradle:**
```groovy
implementation 'dev.gethook:gethook-java:0.1.0'
```

## Usage

```java
import dev.gethook.ApiClient;
import dev.gethook.ApiException;
import dev.gethook.Configuration;
import dev.gethook.api.SourcesApi;
import dev.gethook.auth.ApiKeyAuth;

ApiClient client = Configuration.getDefaultApiClient();
client.setBasePath("https://api.gethook.to");

ApiKeyAuth auth = (ApiKeyAuth) client.getAuthentication("ApiKeyAuth");
auth.setApiKey("hk_your_api_key");

SourcesApi api = new SourcesApi(client);
List<Source> sources = api.listSources();
```

## Documentation

Full API reference: https://docs.gethook.to/reference

## Development

This SDK is auto-generated from the OpenAPI spec via `make sync` in the main [gethook](https://github.com/gethook/gethook) repo.
