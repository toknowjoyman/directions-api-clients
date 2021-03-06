# SWGSolutionApi

All URIs are relative to *https://graphhopper.com/api/1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSolution**](SWGSolutionApi.md#getsolution) | **GET** /vrp/solution/{jobId} | Return the solution associated to the jobId


# **getSolution**
```objc
-(NSURLSessionTask*) getSolutionWithKey: (NSString*) key
    jobId: (NSString*) jobId
        completionHandler: (void (^)(SWGResponse* output, NSError* error)) handler;
```

Return the solution associated to the jobId

This endpoint returns the solution of a large problems. You can fetch it with the job_id, you have been sent. 

### Example 
```objc

NSString* key = @"key_example"; // your API key
NSString* jobId = @"jobId_example"; // Request solution with jobId

SWGSolutionApi*apiInstance = [[SWGSolutionApi alloc] init];

// Return the solution associated to the jobId
[apiInstance getSolutionWithKey:key
              jobId:jobId
          completionHandler: ^(SWGResponse* output, NSError* error) {
                        if (output) {
                            NSLog(@"%@", output);
                        }
                        if (error) {
                            NSLog(@"Error calling SWGSolutionApi->getSolution: %@", error);
                        }
                    }];
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **NSString***| your API key | 
 **jobId** | **NSString***| Request solution with jobId | 

### Return type

[**SWGResponse***](SWGResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

