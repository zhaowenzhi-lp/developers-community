---
pagename: Accessing LivePerson APIs
sitesection: Documents
categoryname: "Getting Started"
documentname: Essential Resources
permalink: essential-resources-accessing-liveperson-apis.html
order: 11
indicator: both
---

Some of our APIs require authorization before you can use them. This is done via either of the following methods: 1) common oAuth2.0 scenarios for web server applications. 2) server to server authrization via either a) API Key which uses the OAuth 1.0 methodology or b) oAuth2.0 for server to server interations. Every API uses either of the two methods (or both), as listed in its overview (for example, the [Audit Trail API](/audit-trail-api-introduction.html)

What follows is a general overview of these two authorization methods and how they work.

### Authorizing web server applications

Web server applications are traditional web apps that perform most of their application logic on the server. This OAuth 2.0 flow is specifically for user authorization. It is designed for applications that can store confidential information and maintain state. A properly authorized web server application can access LivePerson's APIs while the user interacts with the application.
 
In order to accomplish this, you will need to implement the LiveEngage Applications Authorization API (which uses the OAuth 2.0 methodology as explained above). [More information on how to do that can be found here](/authorizing-liveengage-applications-overview.html).

### Authorizing server to server interactions

#### OAuth 1.0 App Keys

This method uses API keys pre-generated by an administrator on your account through the LiveEngage UI. For more information on how to create, retrieve and manage these keys, [please see this document](/essential-resources-create-api-keys.html).

#### OAuth 2.0 (App-JWT)
This method uses the OAuth 2.0 client credentials grant (specified in RFC 6749), sometimes called two-legged OAuth, to access LivePerson APIs by using the identity of an application. This type of grant is commonly used for server to server interactions that must run in the background.
[please see this document](/connector-api-send-api-authorization-and-authentication.html#get-appjwt)