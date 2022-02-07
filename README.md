# Dvelop.Sdk.MicroserviceTemplate - the C# library for the Microservice template

Mircoservice template with movie watchlist example

This C# SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- SDK version: 1.0.0
- Build package: org.openapitools.codegen.languages.CSharpNetCoreClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET Core >=1.0
- .NET Framework >=4.6
- Mono/Xamarin >=vNext

<a name="dependencies"></a>
## Dependencies

- [RestSharp](https://www.nuget.org/packages/RestSharp) - 106.13.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 12.0.3 or later
- [JsonSubTypes](https://www.nuget.org/packages/JsonSubTypes/) - 1.8.0 or later
- [System.ComponentModel.Annotations](https://www.nuget.org/packages/System.ComponentModel.Annotations) - 5.0.0 or later

The DLLs included in the package may not be the latest version. We recommend using [NuGet](https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package RestSharp
Install-Package Newtonsoft.Json
Install-Package JsonSubTypes
Install-Package System.ComponentModel.Annotations
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742).
NOTE: RestSharp for .Net Core creates a new socket for each api call, which can lead to a socket exhaustion problem. See [RestSharp#1406](https://github.com/restsharp/RestSharp/issues/1406).

<a name="installation"></a>
## Installation
Generate the DLL using your preferred tool (e.g. `dotnet build`)

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using Dvelop.Sdk.MicroserviceTemplate.Api;
using Dvelop.Sdk.MicroserviceTemplate.Client;
using Dvelop.Sdk.MicroserviceTemplate.Model;
```
<a name="usage"></a>
## Usage

To use the API client with a HTTP proxy, setup a `System.Net.WebProxy`
```csharp
Configuration c = new Configuration();
System.Net.WebProxy webProxy = new System.Net.WebProxy("http://myProxyUrl:80/");
webProxy.Credentials = System.Net.CredentialCache.DefaultCredentials;
c.Proxy = webProxy;
```

<a name="getting-started"></a>
## Getting Started

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Dvelop.Sdk.MicroserviceTemplate.Api;
using Dvelop.Sdk.MicroserviceTemplate.Client;
using Dvelop.Sdk.MicroserviceTemplate.Model;

namespace Example
{
    public class Example
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
            catch (ApiException e)
            {
                Debug.Print("Exception when calling MovieWatchlistApi.MoviesGet: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }

        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *http://localhost:8080/microservicetemplate*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*MovieWatchlistApi* | [**MoviesGet**](docs/MovieWatchlistApi.md#moviesget) | **GET** /movies | Return all movies
*MovieWatchlistApi* | [**MoviesIdDelete**](docs/MovieWatchlistApi.md#moviesiddelete) | **DELETE** /movies/{id} | Delete an movie by ID
*MovieWatchlistApi* | [**MoviesIdGet**](docs/MovieWatchlistApi.md#moviesidget) | **GET** /movies/{id} | Returns an movie by ID
*MovieWatchlistApi* | [**MoviesIdPatch**](docs/MovieWatchlistApi.md#moviesidpatch) | **PATCH** /movies/{id} | Update an movie by ID
*MovieWatchlistApi* | [**MoviesIdPut**](docs/MovieWatchlistApi.md#moviesidput) | **PUT** /movies/{id} | Update an movie by ID
*MovieWatchlistApi* | [**MoviesPost**](docs/MovieWatchlistApi.md#moviespost) | **POST** /movies | Create a new movie


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.Error](docs/Error.md)
 - [Model.Movie](docs/Movie.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

All endpoints do not require authorization.
