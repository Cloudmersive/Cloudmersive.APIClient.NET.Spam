# Cloudmersive.APIClient.NET.Spam.Model.SpamDetectionAdvancedRequest
AI advanced spam detection request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**InputString** | **string** | Input text string to detect spam against | [optional] 
**Model** | **string** | Optional: Specify which AI model to use.  Possible choices are Normal and Advanced.  Default is Advanced. | [optional] 
**AllowUnsolicitedSales** | **bool** | True if unsolicited sales should be allowed, false otherwise | [optional] 
**AllowPromotionalContent** | **bool** | True if promotional content should be allowed, false otherwise | [optional] 
**AllowPhishing** | **bool** | True if phishing should be allowed, false otherwise | [optional] 
**CustomPolicyID** | **string** | Apply a Custom Policy for Spam Enforcement by providing the ID; to create a Custom Policy, navigate to the Cloudmersive Management Portal and select Custom Policies.  Requires Managed Instance or Private Cloud | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

