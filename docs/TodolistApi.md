# TodolistApi

All URIs are relative to *https://{environment}.programmingwithiko.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**todolistGet**](TodolistApi.md#todolistGet) | **GET** /todolist | Get All Todolist
[**todolistPost**](TodolistApi.md#todolistPost) | **POST** /todolist | Create New Todolist
[**todollistTodolistIdDelete**](TodolistApi.md#todollistTodolistIdDelete) | **DELETE** /todollist/{todolistId} | Delete existing Todolist
[**todollistTodolistIdPut**](TodolistApi.md#todollistTodolistIdPut) | **PUT** /todollist/{todolistId} | Update existing Todolist

<a name="todolistGet"></a>
# **todolistGet**
> ArrayTodolist todolistGet(includeDone, name)

Get All Todolist

Get all todolist by default

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TodolistApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: TodolistAuth
ApiKeyAuth TodolistAuth = (ApiKeyAuth) defaultClient.getAuthentication("TodolistAuth");
TodolistAuth.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.setApiKeyPrefix("Token");

TodolistApi apiInstance = new TodolistApi();
Boolean includeDone = false; // Boolean | Include done todolist in the result
String name = "name_example"; // String | Filter todolist by name
try {
    ArrayTodolist result = apiInstance.todolistGet(includeDone, name);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TodolistApi#todolistGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **includeDone** | **Boolean**| Include done todolist in the result | [optional] [default to false]
 **name** | **String**| Filter todolist by name | [optional]

### Return type

[**ArrayTodolist**](ArrayTodolist.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="todolistPost"></a>
# **todolistPost**
> Todolist todolistPost(body)

Create New Todolist

Create new todolist to database

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TodolistApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: TodolistAuth
ApiKeyAuth TodolistAuth = (ApiKeyAuth) defaultClient.getAuthentication("TodolistAuth");
TodolistAuth.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.setApiKeyPrefix("Token");

TodolistApi apiInstance = new TodolistApi();
CreateOrUpdateTodolist body = new CreateOrUpdateTodolist(); // CreateOrUpdateTodolist | 
try {
    Todolist result = apiInstance.todolistPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TodolistApi#todolistPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CreateOrUpdateTodolist**](CreateOrUpdateTodolist.md)|  |

### Return type

[**Todolist**](Todolist.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="todollistTodolistIdDelete"></a>
# **todollistTodolistIdDelete**
> InlineResponse200 todollistTodolistIdDelete(todolistId)

Delete existing Todolist

Delete existing todolist in database

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TodolistApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: TodolistAuth
ApiKeyAuth TodolistAuth = (ApiKeyAuth) defaultClient.getAuthentication("TodolistAuth");
TodolistAuth.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.setApiKeyPrefix("Token");

TodolistApi apiInstance = new TodolistApi();
String todolistId = "todolistId_example"; // String | Todolist id for updated
try {
    InlineResponse200 result = apiInstance.todollistTodolistIdDelete(todolistId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TodolistApi#todollistTodolistIdDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **todolistId** | **String**| Todolist id for updated |

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="todollistTodolistIdPut"></a>
# **todollistTodolistIdPut**
> Todolist todollistTodolistIdPut(body, todolistId)

Update existing Todolist

Update existing todolist in database

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TodolistApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: TodolistAuth
ApiKeyAuth TodolistAuth = (ApiKeyAuth) defaultClient.getAuthentication("TodolistAuth");
TodolistAuth.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.setApiKeyPrefix("Token");

TodolistApi apiInstance = new TodolistApi();
CreateOrUpdateTodolist body = new CreateOrUpdateTodolist(); // CreateOrUpdateTodolist | 
String todolistId = "todolistId_example"; // String | Todolist id for updated
try {
    Todolist result = apiInstance.todollistTodolistIdPut(body, todolistId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TodolistApi#todollistTodolistIdPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CreateOrUpdateTodolist**](CreateOrUpdateTodolist.md)|  |
 **todolistId** | **String**| Todolist id for updated |

### Return type

[**Todolist**](Todolist.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

