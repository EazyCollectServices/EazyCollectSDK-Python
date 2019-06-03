# EazySDK - Python client
Welcome to the **EazySDK** repository.  EazySDK is an integration of the [Eazy Collect API version 3](https://eazycollectservices.github.io/EazyCollectAPIv3/) built in Python. Its core purpose is to provide a framework for developers already working with Eazy Collect to integrate Eazy Customer Manager into their platform. The framework provides functions designed to speed up the integration process between a developers Customer Relationship Manager and Eazy Collect. Getting started is as simple as providing user specific settings, and making your first call to Eazy Customer Manager should take less than a minute.

## Requirements

 - requests (2.21.0 >=)
 - python (3.7+)

## Integrating EazySDK into your application
The integration process is simple, and involves importing EazySDK into your virtual environment and configuring some settings. The most basic configuration can be seen below.

    >> pip install eazysdk
     
    import eazysdk
     
    eazysdk.settings.current_environment['env'] = 'sandbox'  
    eazysdk.settings.sandbox_client_details['client_code'] = '{client_code}'  
    eazysdk.settings.sandbox_client_details['api_key'] = '{api_key}'
     
    client = eazysdk.EazySDK()
    response = client.get.customers()
    
    print(response)

