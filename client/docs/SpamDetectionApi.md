# Cloudmersive.APIClient.NET.Spam.Api.SpamDetectionApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SpamDetectTextStringAdvancedPost**](SpamDetectionApi.md#spamdetecttextstringadvancedpost) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content. |
| [**SpamDetectTextStringPost**](SpamDetectionApi.md#spamdetecttextstringpost) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content. |

<a id="spamdetecttextstringadvancedpost"></a>
# **SpamDetectTextStringAdvancedPost**
> SpamDetectionAdvancedResponse SpamDetectTextStringAdvancedPost (SpamDetectionAdvancedRequest body = null)

Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.

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
                // Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.
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
    // Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.
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
> SpamDetectionResponse SpamDetectTextStringPost (SpamDetectionAdvancedRequest body = null)

Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.

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
            var body = new SpamDetectionAdvancedRequest(); // SpamDetectionAdvancedRequest | Spam detection request (optional) 

            try
            {
                // Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.
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
    // Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.
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
| **body** | [**SpamDetectionAdvancedRequest**](SpamDetectionAdvancedRequest.md) | Spam detection request | [optional]  |

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

