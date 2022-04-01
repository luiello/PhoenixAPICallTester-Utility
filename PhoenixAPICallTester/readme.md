# PhoenixAPICallTester

PhoenixAPICallTester is a Desktop Application used for API Testing.

# About

With the impossibility of installing new applications on servers, it was necessary to create a standalone .exe application to test API requests.

In addition, this application also makes possible testing API requests using proxy and credentials authentication with custom code, changing calls behavior for testing if needed.

### Features:
 - Request:
	 - Method
	 - Parameters List (read-only)
	 - Proxy/Credentials settings
 - Response:
	 - Body
	 - Cookies
	 - Headers
	 - Logs
 - Asynchronous calls (application will not freeze waiting for a response)

### Not implemented yet:

 - Request:
	 - Headers
	 - Body

## Requirements

- .Net Framework 4.5.2
- NuGet packages:
	- [Humanizer.Core (2.14.1)](https://www.nuget.org/packages/Humanizer.Core/2.14.1)
	- [RestSharp (105.2.3)](https://www.nuget.org/packages/RestSharp/105.2.3)

*It was necessary to use same Framework version than Phoenix for a better simulation.*

## Structure

The application can run normally using one of the following folders structures:

Using a library folder for dlls

    |   PhoenixAPICallTester.exe
    |   PhoenixAPICallTester.exe.config
    |
    \---lib
            Humanizer.dll
            Humanizer.xml
            RestSharp.dll
            RestSharp.xml
            System.Runtime.InteropServices.RuntimeInformation.dll

All files in the same folder

    Humanizer.dll
    Humanizer.xml
    PhoenixAPICallTester.exe
    PhoenixAPICallTester.exe.config
    RestSharp.dll
    RestSharp.xml
    System.Runtime.InteropServices.RuntimeInformation.dll

## PhoenixAPICallTester.exe.config

|Key| Information |
|--|--|
| default_url_encoded| Default URL (Encoded) |
| default_proxy_host| Default Proxy Host |
| default_proxy_port| Default Proxy Port |
| default_credentials_user| Default User Credentials for Proxy |
| default_credentials_password| Default Password Credentials for Proxy |
| default_credentials_domain| Default Domain Credentials for Proxy (if needed) |