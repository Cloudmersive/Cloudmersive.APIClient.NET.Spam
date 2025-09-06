# Cloudmersive.APIClient.NET.Spam.Model.SpamDetectionAdvancedResponse
Result of detecting spam using AI

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CleanResult** | **bool** | True if the result is not spam (clean), and false otherwise | [optional] 
**SpamRiskLevel** | **double** | Overall spam risk level between 0.0 and 1.0 | [optional] 
**ContainsSpam** | **bool** | True if the input text contains spam, false otherwise | [optional] 
**ContainsUnsolicitedSales** | **bool** | True if the input text contains unsolicited sales, false otherwise | [optional] 
**ContainsPromotionalContent** | **bool** | True if the input text contains promotional content, false otherwise | [optional] 
**ContainsPhishingAttempt** | **bool** | True if the input text contains a phishing attempt, false otherwise | [optional] 
**AnalysisRationale** | **string** | Rationale for why the conclusion was formed | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

