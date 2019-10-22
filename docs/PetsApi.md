# PetsApi

All URIs are relative to *http://petstore.swagger.io/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPets**](PetsApi.md#createPets) | **POST** /pets | Create a pet
[**listPets**](PetsApi.md#listPets) | **GET** /pets | List all pets
[**showPetById**](PetsApi.md#showPetById) | **GET** /pets/{petId} | Info for a specific pet



## createPets

> createPets()

Create a pet

### Example

```java
// Import classes:
import com.petstore.api.invoker.ApiClient;
import com.petstore.api.invoker.ApiException;
import com.petstore.api.invoker.Configuration;
import com.petstore.api.invoker.models.*;
import com.petstore.api.PetsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("http://petstore.swagger.io/v1");

        PetsApi apiInstance = new PetsApi(defaultClient);
        try {
            apiInstance.createPets();
        } catch (ApiException e) {
            System.err.println("Exception when calling PetsApi#createPets");
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

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Null response |  -  |
| **0** | unexpected error |  -  |


## listPets

> List&lt;Pet&gt; listPets(limit)

List all pets

### Example

```java
// Import classes:
import com.petstore.api.invoker.ApiClient;
import com.petstore.api.invoker.ApiException;
import com.petstore.api.invoker.Configuration;
import com.petstore.api.invoker.models.*;
import com.petstore.api.PetsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("http://petstore.swagger.io/v1");

        PetsApi apiInstance = new PetsApi(defaultClient);
        Integer limit = 56; // Integer | How many items to return at one time (max 100)
        try {
            List<Pet> result = apiInstance.listPets(limit);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling PetsApi#listPets");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Integer**| How many items to return at one time (max 100) | [optional]

### Return type

[**List&lt;Pet&gt;**](Pet.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A paged array of pets |  * x-next - A link to the next page of responses <br>  |
| **0** | unexpected error |  -  |


## showPetById

> Pet showPetById(petId)

Info for a specific pet

### Example

```java
// Import classes:
import com.petstore.api.invoker.ApiClient;
import com.petstore.api.invoker.ApiException;
import com.petstore.api.invoker.Configuration;
import com.petstore.api.invoker.models.*;
import com.petstore.api.PetsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("http://petstore.swagger.io/v1");

        PetsApi apiInstance = new PetsApi(defaultClient);
        String petId = "petId_example"; // String | The id of the pet to retrieve
        try {
            Pet result = apiInstance.showPetById(petId);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling PetsApi#showPetById");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **String**| The id of the pet to retrieve |

### Return type

[**Pet**](Pet.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Expected response to a valid request |  -  |
| **0** | unexpected error |  -  |

