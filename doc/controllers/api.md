# API

```java
APIController aPIController = client.getAPIController();
```

## Class Name

`APIController`

## Methods

* [Createanitem](../../doc/controllers/api.md#createanitem)
* [Getanitemby ID](../../doc/controllers/api.md#getanitemby-id)
* [Create O Auth Token](../../doc/controllers/api.md#create-o-auth-token)
* [Test Endpointwith Arrays](../../doc/controllers/api.md#test-endpointwith-arrays)


# Createanitem

Creates a new resource in the system.

```java
CompletableFuture<Object> createanitemAsync(
    final Status11Enum status,
    final Item body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status11Enum`](../../doc/models/status-11-enum.md) | Template, Required | The status of the items to filter by. |
| `body` | [`Item`](../../doc/models/item.md) | Body, Optional | Custom model with additional properties |

## Response Type

`Object`

## Example Usage

```java
Status11Enum status = Status11Enum.ENUMVALUE3;
Item body = new Item.Builder(
    UUID.fromString("550e8400-e29b-41d4-a716-446655440000"),
    "John Doe",
    DateTimeHelper.fromSimpleDate("2024-05-24"),
    DateTimeHelper.fromRfc8601DateTime("05/24/2024 12:00:00"),
    1234.56D,
    1234567890123L,
    true,
    CustomEnum.VALUE3,
    ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    new LinkedHashMap<String, Message>() {{
        put("key0", new Message.Builder(
            246,
            "text4"
        )
        .build());
        put("key1", new Message.Builder(
            246,
            "text4"
        )
        .build());
    }}
)
.build();

aPIController.createanitemAsync(status, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response

```
{
  "match": "client_mac",
  "name": "cameras",
  "type": "match",
  "values": [
    "010203040506",
    "abcdef*"
  ]
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Syntax | `ApiException` |
| 401 | Unauthorized | `ApiException` |
| 403 | Permission Denied | `ApiException` |


# Getanitemby ID

```java
CompletableFuture<Item> getanitembyIDAsync(
    final String id,
    final String value)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | The ID of the item to retrieve |
| `value` | `String` | Query, Required | The value of the item to retrieve |

## Response Type

[`Item`](../../doc/models/item.md)

## Example Usage

```java
String id = "id0";
String value = "value2";

aPIController.getanitembyIDAsync(id, value).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Create O Auth Token

Generates a new OAuth token with the specified scopes.

```java
CompletableFuture<Void> createOAuthTokenAsync(
    final TokensRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`TokensRequest`](../../doc/models/tokens-request.md) | Body, Optional | - |

## Response Type

`void`

## Example Usage

```java
aPIController.createOAuthTokenAsync(null).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request | `ApiException` |


# Test Endpointwith Arrays

This endpoint accepts a complex structure with multiple arrays.

```java
CompletableFuture<Void> testEndpointwithArraysAsync(
    final MultipleArraysRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`MultipleArraysRequest`](../../doc/models/multiple-arrays-request.md) | Body, Optional | - |

## Response Type

`void`

## Example Usage

```java
aPIController.testEndpointwithArraysAsync(null).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request | `ApiException` |

