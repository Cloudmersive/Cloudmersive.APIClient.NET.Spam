# Cloudmersive.APIClient.NET.Spam.Api.SpamDetectionApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SpamDetectFileAdvancedPost**](SpamDetectionApi.md#spamdetectfileadvancedpost) | **POST** /spam/detect/file/advanced | Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected. |
| [**SpamDetectFilePost**](SpamDetectionApi.md#spamdetectfilepost) | **POST** /spam/detect/file | Perform AI spam detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 100-125 API calls depending on model selected. |
| [**SpamDetectTextStringAdvancedPost**](SpamDetectionApi.md#spamdetecttextstringadvancedpost) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected. |
| [**SpamDetectTextStringPost**](SpamDetectionApi.md#spamdetecttextstringpost) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected. |

<a id="spamdetectfileadvancedpost"></a>
# **SpamDetectFileAdvancedPost**
> SpamDetectionAdvancedResponse SpamDetectFileAdvancedPost (string model = null, bool? allowPhishing = null, bool? allowUnsolicitedSales = null, bool? allowPromotionalContent = null, System.IO.Stream inputFile = null)

Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Cloudmersive.APIClient.NET.Spam.Api;
using Cloudmersive.APIClient.NET.Spam.Client;
using Cloudmersive.APIClient.NET.Spam.Model;

namespace Example
{
    public class SpamDetectFileAdvancedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi(config);
            var model = "\"Advanced\"";  // string |  (optional)  (default to "Advanced")
            var allowPhishing = false;  // bool? |  (optional)  (default to false)
            var allowUnsolicitedSales = false;  // bool? |  (optional)  (default to false)
            var allowPromotionalContent = false;  // bool? |  (optional)  (default to false)
            var inputFile = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream |  (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
                SpamDetectionAdvancedResponse result = apiInstance.SpamDetectFileAdvancedPost(model, allowPhishing, allowUnsolicitedSales, allowPromotionalContent, inputFile);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFileAdvancedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SpamDetectFileAdvancedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
    ApiResponse<SpamDetectionAdvancedResponse> response = apiInstance.SpamDetectFileAdvancedPostWithHttpInfo(model, allowPhishing, allowUnsolicitedSales, allowPromotionalContent, inputFile);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFileAdvancedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **model** | **string** |  | [optional] [default to &quot;Advanced&quot;] |
| **allowPhishing** | **bool?** |  | [optional] [default to false] |
| **allowUnsolicitedSales** | **bool?** |  | [optional] [default to false] |
| **allowPromotionalContent** | **bool?** |  | [optional] [default to false] |
| **inputFile** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |

### Return type

[**SpamDetectionAdvancedResponse**](SpamDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="spamdetectfilepost"></a>
# **SpamDetectFilePost**
> SpamDetectionResponse SpamDetectFilePost (string model = null, System.IO.Stream inputFile = null)

Perform AI spam detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Cloudmersive.APIClient.NET.Spam.Api;
using Cloudmersive.APIClient.NET.Spam.Client;
using Cloudmersive.APIClient.NET.Spam.Model;

namespace Example
{
    public class SpamDetectFilePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi(config);
            var model = "\"Advanced\"";  // string | Model to use; default setting is Advanced (optional)  (default to "Advanced")
            var inputFile = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream |  (optional) 

            try
            {
                // Perform AI spam detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.
                SpamDetectionResponse result = apiInstance.SpamDetectFilePost(model, inputFile);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFilePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SpamDetectFilePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Perform AI spam detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.
    ApiResponse<SpamDetectionResponse> response = apiInstance.SpamDetectFilePostWithHttpInfo(model, inputFile);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFilePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **model** | **string** | Model to use; default setting is Advanced | [optional] [default to &quot;Advanced&quot;] |
| **inputFile** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |

### Return type

[**SpamDetectionResponse**](SpamDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="spamdetecttextstringadvancedpost"></a>
# **SpamDetectTextStringAdvancedPost**
> SpamDetectionAdvancedResponse SpamDetectTextStringAdvancedPost (SpamDetectionAdvancedRequest body = null)

Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Cloudmersive.APIClient.NET.Spam.Api;
using Cloudmersive.APIClient.NET.Spam.Client;
using Cloudmersive.APIClient.NET.Spam.Model;

namespace Example
{
    public class SpamDetectTextStringAdvancedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi(config);
            var body = new SpamDetectionAdvancedRequest(); // SpamDetectionAdvancedRequest | Spam detection request (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
                SpamDetectionAdvancedResponse result = apiInstance.SpamDetectTextStringAdvancedPost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectTextStringAdvancedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SpamDetectTextStringAdvancedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
    ApiResponse<SpamDetectionAdvancedResponse> response = apiInstance.SpamDetectTextStringAdvancedPostWithHttpInfo(body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpamDetectionApi.SpamDetectTextStringAdvancedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **body** | [**SpamDetectionAdvancedRequest**](SpamDetectionAdvancedRequest.md) | Spam detection request | [optional]  |

### Return type

[**SpamDetectionAdvancedResponse**](SpamDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="spamdetecttextstringpost"></a>
# **SpamDetectTextStringPost**
> SpamDetectionResponse SpamDetectTextStringPost (SpamDetectionRequest body = null)

Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Cloudmersive.APIClient.NET.Spam.Api;
using Cloudmersive.APIClient.NET.Spam.Client;
using Cloudmersive.APIClient.NET.Spam.Model;

namespace Example
{
    public class SpamDetectTextStringPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi(config);
            var body = new SpamDetectionRequest(); // SpamDetectionRequest | Spam detection request (optional) 

            try
            {
                // Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.
                SpamDetectionResponse result = apiInstance.SpamDetectTextStringPost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectTextStringPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SpamDetectTextStringPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.
    ApiResponse<SpamDetectionResponse> response = apiInstance.SpamDetectTextStringPostWithHttpInfo(body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpamDetectionApi.SpamDetectTextStringPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **body** | [**SpamDetectionRequest**](SpamDetectionRequest.md) | Spam detection request | [optional]  |

### Return type

[**SpamDetectionResponse**](SpamDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

