# ![LOGO](logo.png) Request Baskets **flow**ground Connector

## Description

A generated **flow**ground connector for the Request Baskets API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/rbaskets.in/1.0.0/swagger.json<br/>
Generated at: 2019-06-06T16:13:05+03:00

## API Description

RESTful API of [Request Baskets](https://rbaskets.in) service.

Request Baskets is an open source project of a service to collect HTTP requests and inspect them via RESTful
API or web UI.

Check out the [project page](https://github.com/darklynx/request-baskets) for more detailed description.


## Authorization

Supported authorization schemes:
- API Key- API Key
## Actions

### Get baskets

> Fetches a list of basket names managed by service. Require master token.

*Tags:* `baskets`

#### Input Parameters
* `max` - _optional_ - Maximum number of basket names to return; default 20
* `skip` - _optional_ - Number of basket names to skip; default 0
* `q` - _optional_ - Query string to filter result, only those basket names that match the query will be included in response

### Delete basket

> Permanently deletes this basket and all collected requests.

*Tags:* `baskets`

#### Input Parameters
* `name` - _required_ - The basket name

### Get basket settings

> Retrieves configuration settings of this basket.

*Tags:* `baskets`

#### Input Parameters
* `name` - _required_ - The basket name

### Create new basket

> Creates a new basket with this name.

*Tags:* `baskets`

#### Input Parameters
* `name` - _required_ - The name of new basket

### Update basket settings

> Updates configuration settings of this basket.<br/>
> <br/>
> Special configuration parameters for request forwarding:<br/>
>   * `insecure_tls` controls certificate verification when forwarding requests. Setting this parameter to `true`<br/>
>   allows to forward collected HTTP requests via HTTPS protocol even if the forward end-point is configured with<br/>
>   self-signed TLS/SSL certificate. **Warning:** enabling this feature has known security implications.<br/>
>   * `expand_path` changes the logic of constructing taget URL when forwarding requests. If this parameter is<br/>
>   set to `true` the forward URL path will be expanded when original HTTP request contains compound path. For<br/>
>   example, a basket with name **server1** is configured to forward all requests to `http://server1.intranet:8001/myservice`<br/>
>   and it has received an HTTP request like `GET http://baskets.example.com/server1/component/123/events?status=OK`<br/>
>   then depending on `expand_path` settings the request will be forwarded to:<br/>
>     * `true` => `GET http://server1.intranet:8001/myservice/component/123/events?status=OK`<br/>
>     * `false` => `GET http://server1.intranet:8001/myservice?status=OK`

*Tags:* `baskets`

#### Input Parameters
* `name` - _required_ - The basket name

### Delete all requests

> Deletes all requests collected by this basket.

*Tags:* `requests`

#### Input Parameters
* `name` - _required_ - The basket name

### Get collected requests

> Fetches collection of requests collected by this basket.

*Tags:* `requests`

#### Input Parameters
* `name` - _required_ - The basket name
* `max` - _optional_ - Maximum number of requests to return; default 20
* `skip` - _optional_ - Number of requests to skip; default 0
* `q` - _optional_ - Query string to filter result, only requests that match the query will be included in response
* `in` - _optional_ - Defines what is taken into account when filtering is applied: `body` - search in content body of collected requests,
`query` - search among query parameters of collected requests, `headers` - search among request header values,
`any` - search anywhere; default `any`

    Possible values: any, body, query, headers.

### Get response settings

> Retrieves information about configured response of the basket. Service will reply with this response to any<br/>
> HTTP request sent to the basket with appropriate HTTP method.<br/>
> <br/>
> If nothing is configured, the default response is HTTP 200 - OK with empty content.

*Tags:* `responses`

#### Input Parameters
* `name` - _required_ - The basket name
* `method` - _required_ - The HTTP method this response is configured for
    Possible values: GET, HEAD, POST, PUT, PATCH, DELETE, CONNECT, OPTIONS, TRACE.

### Update response settings

> Allows to configure HTTP response of this basket. The service will reply with configured response to any HTTP<br/>
> request sent to the basket with appropriate HTTP method.<br/>
> <br/>
> If nothing is configured, the default response is HTTP 200 - OK with empty content.

*Tags:* `responses`

#### Input Parameters
* `name` - _required_ - The basket name
* `method` - _required_ - The HTTP method this response is configured for
    Possible values: GET, HEAD, POST, PUT, PATCH, DELETE, CONNECT, OPTIONS, TRACE.

### Get baskets statistics

> Get service statistics about baskets and collected HTTP requests. Require master token.

*Tags:* `baskets`

#### Input Parameters
* `max` - _optional_ - Maximum number of basket names to return; default 5

### Get service version

> Get service version.

*Tags:* `service`

### Get baskets

> Fetches a list of basket names managed by service. Require master token.

*Tags:* `baskets`

#### Input Parameters
* `max` - _optional_ - Maximum number of basket names to return; default 20
* `skip` - _optional_ - Number of basket names to skip; default 0
* `q` - _optional_ - Query string to filter result, only those basket names that match the query will be included in response

### Delete basket

> Permanently deletes this basket and all collected requests.

*Tags:* `baskets`

#### Input Parameters
* `name` - _required_ - The basket name

### Get basket settings

> Retrieves configuration settings of this basket.

*Tags:* `baskets`

#### Input Parameters
* `name` - _required_ - The basket name

### Create new basket

> Creates a new basket with this name.

*Tags:* `baskets`

#### Input Parameters
* `name` - _required_ - The name of new basket

### Update basket settings

> Updates configuration settings of this basket.<br/>
> <br/>
> Special configuration parameters for request forwarding:<br/>
>   * `insecure_tls` controls certificate verification when forwarding requests. Setting this parameter to `true`<br/>
>   allows to forward collected HTTP requests via HTTPS protocol even if the forward end-point is configured with<br/>
>   self-signed TLS/SSL certificate. **Warning:** enabling this feature has known security implications.<br/>
>   * `expand_path` changes the logic of constructing taget URL when forwarding requests. If this parameter is<br/>
>   set to `true` the forward URL path will be expanded when original HTTP request contains compound path. For<br/>
>   example, a basket with name **server1** is configured to forward all requests to `http://server1.intranet:8001/myservice`<br/>
>   and it has received an HTTP request like `GET http://baskets.example.com/server1/component/123/events?status=OK`<br/>
>   then depending on `expand_path` settings the request will be forwarded to:<br/>
>     * `true` => `GET http://server1.intranet:8001/myservice/component/123/events?status=OK`<br/>
>     * `false` => `GET http://server1.intranet:8001/myservice?status=OK`

*Tags:* `baskets`

#### Input Parameters
* `name` - _required_ - The basket name

### Delete all requests

> Deletes all requests collected by this basket.

*Tags:* `requests`

#### Input Parameters
* `name` - _required_ - The basket name

### Get collected requests

> Fetches collection of requests collected by this basket.

*Tags:* `requests`

#### Input Parameters
* `name` - _required_ - The basket name
* `max` - _optional_ - Maximum number of requests to return; default 20
* `skip` - _optional_ - Number of requests to skip; default 0
* `q` - _optional_ - Query string to filter result, only requests that match the query will be included in response
* `in` - _optional_ - Defines what is taken into account when filtering is applied: `body` - search in content body of collected requests,
`query` - search among query parameters of collected requests, `headers` - search among request header values,
`any` - search anywhere; default `any`

    Possible values: any, body, query, headers.

### Get response settings

> Retrieves information about configured response of the basket. Service will reply with this response to any<br/>
> HTTP request sent to the basket with appropriate HTTP method.<br/>
> <br/>
> If nothing is configured, the default response is HTTP 200 - OK with empty content.

*Tags:* `responses`

#### Input Parameters
* `name` - _required_ - The basket name
* `method` - _required_ - The HTTP method this response is configured for
    Possible values: GET, HEAD, POST, PUT, PATCH, DELETE, CONNECT, OPTIONS, TRACE.

### Update response settings

> Allows to configure HTTP response of this basket. The service will reply with configured response to any HTTP<br/>
> request sent to the basket with appropriate HTTP method.<br/>
> <br/>
> If nothing is configured, the default response is HTTP 200 - OK with empty content.

*Tags:* `responses`

#### Input Parameters
* `name` - _required_ - The basket name
* `method` - _required_ - The HTTP method this response is configured for
    Possible values: GET, HEAD, POST, PUT, PATCH, DELETE, CONNECT, OPTIONS, TRACE.

## License

**flow**ground :- Telekom iPaaS / rbaskets-in-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
