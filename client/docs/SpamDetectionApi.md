# Cloudmersive.APIClient.NET.Spam.Api.SpamDetectionApi

All URIs are relative to *https://api.cloudmersive.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SpamDetectFileAdvancedPost**](SpamDetectionApi.md#spamdetectfileadvancedpost) | **POST** /spam/detect/file/advanced | Perform advanced AI spam detection and classification against input text file. |
| [**SpamDetectFilePost**](SpamDetectionApi.md#spamdetectfilepost) | **POST** /spam/detect/file | Perform AI spam detection and classification on an input image or document (PDF or DOCX) |
| [**SpamDetectFormSubmissionAdvancedPost**](SpamDetectionApi.md#spamdetectformsubmissionadvancedpost) | **POST** /spam/detect/form-submission/advanced | Perform advanced AI spam detection and classification against a form submission |
| [**SpamDetectTextStringAdvancedPost**](SpamDetectionApi.md#spamdetecttextstringadvancedpost) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string |
| [**SpamDetectTextStringPost**](SpamDetectionApi.md#spamdetecttextstringpost) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string |

<a id="spamdetectfileadvancedpost"></a>
# **SpamDetectFileAdvancedPost**
> SpamDetectionAdvancedResponse SpamDetectFileAdvancedPost (string model = null, string preprocessing = null, bool? allowPhishing = null, bool? allowUnsolicitedSales = null, bool? allowPromotionalContent = null, string customPolicyId = null, FileParameter inputFile = null)

Perform advanced AI spam detection and classification against input text file.

Analyzes input content as well as embedded URLs with AI deep learning to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.  Supported file formats include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
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
            config.BasePath = "https://api.cloudmersive.com";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SpamDetectionApi(httpClient, config, httpClientHandler);
            var model = "\"Advanced\"";  // string | Optional: Specify which AI model to use.  Possible choices are Normal and Advanced.  Default is Advanced. (optional)  (default to "Advanced")
            var preprocessing = "\"Auto\"";  // string | Optional: Specify which preprocessing to Use.  Possible choices are None, Compatability and Auto.  Default is Auto. (optional)  (default to "Auto")
            var allowPhishing = false;  // bool? | True if phishing should be allowed, false otherwise (optional)  (default to false)
            var allowUnsolicitedSales = false;  // bool? | True if unsolicited sales should be allowed, false otherwise (optional)  (default to false)
            var allowPromotionalContent = true;  // bool? | True if promotional content should be allowed, false otherwise (optional)  (default to true)
            var customPolicyId = "customPolicyId_example";  // string | Apply a Custom Policy for Spam Enforcement by providing the ID; to create a Custom Policy, navigate to the Cloudmersive Management Portal and select Custom Policies.  Requires Managed Instance or Private Cloud (optional) 
            var inputFile = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter |  (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against input text file.
                SpamDetectionAdvancedResponse result = apiInstance.SpamDetectFileAdvancedPost(model, preprocessing, allowPhishing, allowUnsolicitedSales, allowPromotionalContent, customPolicyId, inputFile);
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
    // Perform advanced AI spam detection and classification against input text file.
    ApiResponse<SpamDetectionAdvancedResponse> response = apiInstance.SpamDetectFileAdvancedPostWithHttpInfo(model, preprocessing, allowPhishing, allowUnsolicitedSales, allowPromotionalContent, customPolicyId, inputFile);
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
| **model** | **string** | Optional: Specify which AI model to use.  Possible choices are Normal and Advanced.  Default is Advanced. | [optional] [default to &quot;Advanced&quot;] |
| **preprocessing** | **string** | Optional: Specify which preprocessing to Use.  Possible choices are None, Compatability and Auto.  Default is Auto. | [optional] [default to &quot;Auto&quot;] |
| **allowPhishing** | **bool?** | True if phishing should be allowed, false otherwise | [optional] [default to false] |
| **allowUnsolicitedSales** | **bool?** | True if unsolicited sales should be allowed, false otherwise | [optional] [default to false] |
| **allowPromotionalContent** | **bool?** | True if promotional content should be allowed, false otherwise | [optional] [default to true] |
| **customPolicyId** | **string** | Apply a Custom Policy for Spam Enforcement by providing the ID; to create a Custom Policy, navigate to the Cloudmersive Management Portal and select Custom Policies.  Requires Managed Instance or Private Cloud | [optional]  |
| **inputFile** | **FileParameter****FileParameter** |  | [optional]  |

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
> SpamDetectionResponse SpamDetectFilePost (string model = null, FileParameter inputFile = null)

Perform AI spam detection and classification on an input image or document (PDF or DOCX)

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.  Supported file formats include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
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
            config.BasePath = "https://api.cloudmersive.com";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SpamDetectionApi(httpClient, config, httpClientHandler);
            var model = "\"Advanced\"";  // string | Model to use; default setting is Advanced (optional)  (default to "Advanced")
            var inputFile = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter |  (optional) 

            try
            {
                // Perform AI spam detection and classification on an input image or document (PDF or DOCX)
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
    // Perform AI spam detection and classification on an input image or document (PDF or DOCX)
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
| **inputFile** | **FileParameter****FileParameter** |  | [optional]  |

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

<a id="spamdetectformsubmissionadvancedpost"></a>
# **SpamDetectFormSubmissionAdvancedPost**
> SpamDetectionFormSubmissionAdvancedResponse SpamDetectFormSubmissionAdvancedPost (SpamDetectionAdvancedFormSubmissionRequest body = null)

Perform advanced AI spam detection and classification against a form submission

Analyzes form input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Cloudmersive.APIClient.NET.Spam.Api;
using Cloudmersive.APIClient.NET.Spam.Client;
using Cloudmersive.APIClient.NET.Spam.Model;

namespace Example
{
    public class SpamDetectFormSubmissionAdvancedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.cloudmersive.com";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SpamDetectionApi(httpClient, config, httpClientHandler);
            var body = new SpamDetectionAdvancedFormSubmissionRequest(); // SpamDetectionAdvancedFormSubmissionRequest | Spam detection request (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against a form submission
                SpamDetectionFormSubmissionAdvancedResponse result = apiInstance.SpamDetectFormSubmissionAdvancedPost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFormSubmissionAdvancedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SpamDetectFormSubmissionAdvancedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Perform advanced AI spam detection and classification against a form submission
    ApiResponse<SpamDetectionFormSubmissionAdvancedResponse> response = apiInstance.SpamDetectFormSubmissionAdvancedPostWithHttpInfo(body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFormSubmissionAdvancedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **body** | [**SpamDetectionAdvancedFormSubmissionRequest**](SpamDetectionAdvancedFormSubmissionRequest.md) | Spam detection request | [optional]  |

### Return type

[**SpamDetectionFormSubmissionAdvancedResponse**](SpamDetectionFormSubmissionAdvancedResponse.md)

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

<a id="spamdetecttextstringadvancedpost"></a>
# **SpamDetectTextStringAdvancedPost**
> SpamDetectionAdvancedResponse SpamDetectTextStringAdvancedPost (SpamDetectionAdvancedRequest body = null)

Perform advanced AI spam detection and classification against input text string

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
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
            config.BasePath = "https://api.cloudmersive.com";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SpamDetectionApi(httpClient, config, httpClientHandler);
            var body = new SpamDetectionAdvancedRequest(); // SpamDetectionAdvancedRequest | Spam detection request (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against input text string
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
    // Perform advanced AI spam detection and classification against input text string
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

Perform AI spam detection and classification against input text string

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
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
            config.BasePath = "https://api.cloudmersive.com";
            // Configure API key authorization: Apikey
            config.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("Apikey", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SpamDetectionApi(httpClient, config, httpClientHandler);
            var body = new SpamDetectionRequest(); // SpamDetectionRequest | Spam detection request (optional) 

            try
            {
                // Perform AI spam detection and classification against input text string
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
    // Perform AI spam detection and classification against input text string
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

