
# Getting Started with Cypress Test API

## Introduction

This is a sample API to demonstrate an OpenAPI spec with multiple endpoints and a custom model.

## Install the Package

Install the SDK by adding the following dependency in your project's pom.xml file:

```xml
<dependency>
  <groupId>io.github.zahran444</groupId>
  <artifactId>uta-cotton-sdk</artifactId>
  <version>6.6.7</version>
</dependency>
```

You can also view the package at:
https://central.sonatype.com/artifact/io.github.zahran444/uta-cotton-sdk/6.6.7

## Test the SDK

The generated code and the server can be tested using automatically generated test cases.
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project CypressTestAPILib from the package explorer.
2. Select `Run -> Run as -> JUnit Test` or use `Alt + Shift + X` followed by `T` to run the Tests.

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| defaultHost | `String` | *Default*: `"www.example.com"` |
| environment | `Environment` | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |

The API client can be initialized as follows:

```java
import com.example.www.CypressTestAPIClient;
import com.example.www.Environment;
import com.example.www.exceptions.ApiException;
import java.io.IOException;

public class Program {
    public static void main(String[] args) {
        CypressTestAPIClient client = new CypressTestAPIClient.Builder()
            .httpClientConfig(configBuilder -> configBuilder
                    .timeout(0))
            .environment(Environment.PRODUCTION)
            .defaultHost("www.example.com")
            .build();

    }
}
```

## List of APIs

* [API](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/controllers/api.md)

## SDK Infrastructure

### Configuration

* [Configuration Interface](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/configuration-interface.md)
* [HttpClientConfiguration](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-client-configuration.md)
* [HttpClientConfiguration.Builder](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-client-configuration-builder.md)
* [HttpProxyConfiguration](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-proxy-configuration.md)
* [HttpProxyConfiguration.Builder](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-proxy-configuration-builder.md)

### HTTP

* [Headers](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/headers.md)
* [HttpCallback Interface](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-callback-interface.md)
* [HttpContext](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-context.md)
* [HttpBodyRequest](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-body-request.md)
* [HttpRequest](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-request.md)
* [HttpResponse](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-response.md)
* [HttpStringResponse](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/http-string-response.md)

### Utilities

* [ApiException](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/api-exception.md)
* [ApiHelper](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/api-helper.md)
* [FileWrapper](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/file-wrapper.md)
* [DateTimeHelper](https://www.github.com/ZahraN444/uta-cotton-java-sdk/tree/6.6.7/doc/date-time-helper.md)

