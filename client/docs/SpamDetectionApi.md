# Cloudmersive.APIClient.NET.Spam.Api.SpamDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**SpamDetectTextStringAdvancedPost**](SpamDetectionApi.md#spamdetecttextstringadvancedpost) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.
[**SpamDetectTextStringPost**](SpamDetectionApi.md#spamdetecttextstringpost) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.


<a name="spamdetecttextstringadvancedpost"></a>
# **SpamDetectTextStringAdvancedPost**
> SpamDetectionAdvancedResponse SpamDetectTextStringAdvancedPost (SpamDetectionAdvancedRequest body = null)

Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NET.Spam.Api;
using Cloudmersive.APIClient.NET.Spam.Client;
using Cloudmersive.APIClient.NET.Spam.Model;

namespace Example
{
    public class SpamDetectTextStringAdvancedPostExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi();
            var body = new SpamDetectionAdvancedRequest(); // SpamDetectionAdvancedRequest | Spam detection request (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.
                SpamDetectionAdvancedResponse result = apiInstance.SpamDetectTextStringAdvancedPost(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectTextStringAdvancedPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionAdvancedRequest**](SpamDetectionAdvancedRequest.md)| Spam detection request | [optional] 

### Return type

[**SpamDetectionAdvancedResponse**](SpamDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="spamdetecttextstringpost"></a>
# **SpamDetectTextStringPost**
> SpamDetectionResponse SpamDetectTextStringPost (SpamDetectionAdvancedRequest body = null)

Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NET.Spam.Api;
using Cloudmersive.APIClient.NET.Spam.Client;
using Cloudmersive.APIClient.NET.Spam.Model;

namespace Example
{
    public class SpamDetectTextStringPostExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi();
            var body = new SpamDetectionAdvancedRequest(); // SpamDetectionAdvancedRequest | Spam detection request (optional) 

            try
            {
                // Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.
                SpamDetectionResponse result = apiInstance.SpamDetectTextStringPost(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectTextStringPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionAdvancedRequest**](SpamDetectionAdvancedRequest.md)| Spam detection request | [optional] 

### Return type

[**SpamDetectionResponse**](SpamDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

