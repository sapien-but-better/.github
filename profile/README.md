# Sapien API Platform

The SAP system originally started because I wanted to be able to add features to the BSFC Sapien system that it did not have. Most of these centred around the idea of having a sleek frontend powered by an efficient backend that is able to interact with a robust API. These are divided into two core repositories, the actual website application and the API.

⚠️ Please note that all of the repositories are currently private, and therefore are un-accessible unless you're apart of the Development team and logged in.

## [Website Application](https://github.com/sapien-but-better/app)

This is the main website application is built on a completely custom framework, designed to be uncompromising on performance with an event based component design, Powered by a built-from-scratch framwork. I created this since I did not like the design layout of Laravel, which I was originally using. The callback driven event system, which is based on a compartmentalised component design, means that each component has access to interact directly with the core via the their responses.

## [API](https://github.com/sapien-but-better/api)

This is the main API that preforms the direct interfacing with Sapien. This is essentially a browser based scrape engine designed with instance pooling to feed semantic data to the website application. Authentication should never be directly handled by the API, Instead the backend application should ensure correct authentication is sent for the user. This API will instead directly and blindly forward any provided authentication credentials to the Sapien page, allowing the page to return its own response.

## [Wrapper](https://github.com/sapien-but-better/wrapper)

The wrapper is a very simplistic asynchronous Python interface to the Sapien API. It is used for internal tools such as Network Management/Monitoring and the load balancing array. It will be subject to breaking changes without warning due to its nature of being an internal tool. If you decide to use the [API](https://github.com/sapien-but-better/api) in anyway, you should consider writing your own wrapper.
