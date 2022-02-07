# Dvelop.Sdk.MicroserviceTemplate.Api.MovieWatchlistApi

All URIs are relative to *http://localhost:8080/microservicetemplate*

Method | HTTP request | Description
------------- | ------------- | -------------
[**MoviesGet**](MovieWatchlistApi.md#moviesget) | **GET** /movies | Return all movies
[**MoviesIdDelete**](MovieWatchlistApi.md#moviesiddelete) | **DELETE** /movies/{id} | Delete an movie by ID
[**MoviesIdGet**](MovieWatchlistApi.md#moviesidget) | **GET** /movies/{id} | Returns an movie by ID
[**MoviesIdPatch**](MovieWatchlistApi.md#moviesidpatch) | **PATCH** /movies/{id} | Update an movie by ID
[**MoviesIdPut**](MovieWatchlistApi.md#moviesidput) | **PUT** /movies/{id} | Update an movie by ID
[**MoviesPost**](MovieWatchlistApi.md#moviespost) | **POST** /movies | Create a new movie


<a name="moviesget"></a>
# **MoviesGet**
> List&lt;Movie&gt; MoviesGet ()

Return all movies

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Dvelop.Sdk.MicroserviceTemplate.Api;
using Dvelop.Sdk.MicroserviceTemplate.Client;
using Dvelop.Sdk.MicroserviceTemplate.Model;

namespace Example
{
    public class MoviesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080/microservicetemplate";
            var apiInstance = new MovieWatchlistApi(config);

            try
            {
                // Return all movies
                List<Movie> result = apiInstance.MoviesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MovieWatchlistApi.MoviesGet: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;Movie&gt;**](Movie.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | movies response |  -  |
| **0** | unexpected error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="moviesiddelete"></a>
# **MoviesIdDelete**
> void MoviesIdDelete (Guid id)

Delete an movie by ID

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Dvelop.Sdk.MicroserviceTemplate.Api;
using Dvelop.Sdk.MicroserviceTemplate.Client;
using Dvelop.Sdk.MicroserviceTemplate.Model;

namespace Example
{
    public class MoviesIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080/microservicetemplate";
            var apiInstance = new MovieWatchlistApi(config);
            var id = "id_example";  // Guid | ID of movie

            try
            {
                // Delete an movie by ID
                apiInstance.MoviesIdDelete(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MovieWatchlistApi.MoviesIdDelete: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Guid**| ID of movie | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | movie deleted |  -  |
| **0** | unexpected error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="moviesidget"></a>
# **MoviesIdGet**
> Movie MoviesIdGet (Guid id)

Returns an movie by ID

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Dvelop.Sdk.MicroserviceTemplate.Api;
using Dvelop.Sdk.MicroserviceTemplate.Client;
using Dvelop.Sdk.MicroserviceTemplate.Model;

namespace Example
{
    public class MoviesIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080/microservicetemplate";
            var apiInstance = new MovieWatchlistApi(config);
            var id = "id_example";  // Guid | ID of movie

            try
            {
                // Returns an movie by ID
                Movie result = apiInstance.MoviesIdGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MovieWatchlistApi.MoviesIdGet: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Guid**| ID of movie | 

### Return type

[**Movie**](Movie.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | movie response |  -  |
| **0** | unexpected error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="moviesidpatch"></a>
# **MoviesIdPatch**
> Movie MoviesIdPatch (Guid id, Movie movie)

Update an movie by ID

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Dvelop.Sdk.MicroserviceTemplate.Api;
using Dvelop.Sdk.MicroserviceTemplate.Client;
using Dvelop.Sdk.MicroserviceTemplate.Model;

namespace Example
{
    public class MoviesIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080/microservicetemplate";
            var apiInstance = new MovieWatchlistApi(config);
            var id = "id_example";  // Guid | ID of movie
            var movie = new Movie(); // Movie | Updated movie

            try
            {
                // Update an movie by ID
                Movie result = apiInstance.MoviesIdPatch(id, movie);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MovieWatchlistApi.MoviesIdPatch: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Guid**| ID of movie | 
 **movie** | [**Movie**](Movie.md)| Updated movie | 

### Return type

[**Movie**](Movie.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful updated movie |  -  |
| **0** | unexpected error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="moviesidput"></a>
# **MoviesIdPut**
> Movie MoviesIdPut (Guid id, Movie movie)

Update an movie by ID

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Dvelop.Sdk.MicroserviceTemplate.Api;
using Dvelop.Sdk.MicroserviceTemplate.Client;
using Dvelop.Sdk.MicroserviceTemplate.Model;

namespace Example
{
    public class MoviesIdPutExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080/microservicetemplate";
            var apiInstance = new MovieWatchlistApi(config);
            var id = "id_example";  // Guid | ID of movie
            var movie = new Movie(); // Movie | Updated movie

            try
            {
                // Update an movie by ID
                Movie result = apiInstance.MoviesIdPut(id, movie);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MovieWatchlistApi.MoviesIdPut: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Guid**| ID of movie | 
 **movie** | [**Movie**](Movie.md)| Updated movie | 

### Return type

[**Movie**](Movie.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful updated movie |  -  |
| **0** | unexpected error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="moviespost"></a>
# **MoviesPost**
> Movie MoviesPost (Movie movie)

Create a new movie

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Dvelop.Sdk.MicroserviceTemplate.Api;
using Dvelop.Sdk.MicroserviceTemplate.Client;
using Dvelop.Sdk.MicroserviceTemplate.Model;

namespace Example
{
    public class MoviesPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080/microservicetemplate";
            var apiInstance = new MovieWatchlistApi(config);
            var movie = new Movie(); // Movie | Movie to storage

            try
            {
                // Create a new movie
                Movie result = apiInstance.MoviesPost(movie);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MovieWatchlistApi.MoviesPost: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **movie** | [**Movie**](Movie.md)| Movie to storage | 

### Return type

[**Movie**](Movie.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | created movie response |  -  |
| **0** | unexpected error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

