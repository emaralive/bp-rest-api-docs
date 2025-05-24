# Reference

Just like the WordPress REST API, the BP REST API is organized around [REST](http://en.wikipedia.org/wiki/Representational_state_transfer), and is designed to have predictable, resource-oriented URLs and to use HTTP response codes to indicate API errors. The API uses built-in HTTP features, like HTTP authentication and HTTP verbs, which can be understood by off-the-shelf HTTP clients, and supports cross-origin resource sharing to allow you to interact securely with the API from a client-side web application.

The BP REST API uses JSON exclusively as the request and response format, including error responses.

The BP REST API provides public data accessible to any client anonymously, as well as private data only available after [authentication](https://developer.buddypress.org/bp-rest-api/#about-authentification). Once authenticated the BP REST API supports most BuddyPress community actions, allowing you to enhance your plugins with more responsive management tools, or build complex single-page applications.

This API reference provides information on the specific endpoints available through the API, their parameters, and their response data format.

## Developer Endpoint Reference

| Resource | Base Route |
| --- | --- |
| [Components](https://developer.buddypress.org/bp-rest-api/reference/components/) | `/buddypress/v1/components` |
| [Members](https://developer.buddypress.org/bp-rest-api/reference/members/) | `/buddypress/v1/members` |


