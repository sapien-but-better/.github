# Sapien API Platform

The SAP system originally started because I wanted to be able to add features to the BSFC Sapien system that it did not have. Most of these centred around the idea of having a sleek frontend powered by an efficient backend that is able to interact with a robust API. These are divided into two core repositories, the actual website application and the API.

⚠️ Please note that all of the repositories are currently private, and therefore are un-accessible unless you're apart of the Development team and logged in.

## [Website Application](https://github.com/sapien-but-better/app)

The main website application is built on a completely custom framework, designed to be uncompromising on performance with an event based component design. This is powered by a built-from-scratch application. I created this because I did not like the design layout of Laravel which I was originally using. The system uses a callback driven event system which is based on components. This means that each component has access to interact directly with the core via the event responses.

## [API](https://github.com/sapien-but-better/api)

The main API that is the direct interface to Sapien. This is essentially a browser based scrape engine designed with instance pooling to feed semantic data to the website application. This compiles the data into semantic JSON that can then be read by the backend web application. Authentication should never be directly handled by the API, Instead the backend application should ensure correct authentication is sent for the user. This API will instead directly and blindly forward any provided authentication credentials to the Sapien page, allowing the page to return its own response.
