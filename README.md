# F5 Distributed Cloud - Simple API Discovery

Simple method for providing API Discovery via Distributed Cloud for APIs that are not proxied by Distributed Cloud.

This approach doesn't require an actual service response, only request traffic.

## Table of Contents
1. [Flow](#flow)
2. [Outcome](#outcome)
3. [Outcome Example](#outcome-example)
4. [Limitations](#limitations)
5. [Requirements](#requirements)
6. [Guide](#guide)
7. [Load Balancer Templates](#load-balancer-templates)

## Flow

![Object Flow](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/object_flow.jpg)

## Outcome

- Path Discovery (Leaf Creation)

- Request Sensitive Data Detection (PUT, POST)

_Note - Sensitive Data Detection requires request format of JSON_

## Outcome Example

Path Discovery (Leaf Creation)

![Path](static/leaf.jpg)

Request Sensitive Data Detection (PUT, POST)

![Detection](static/discovery.jpg)

## Limitations

- No Response Sensitive Data Detection

- No Authentication Detection

- No Performance Statistics

_Note - Limitation(s) are not a result of platform capability, but an outcome of not having a proper service response_

## Requirements

- HTTP(S) Request Traffic

- Distributed Cloud Tenant

  -	Load Balancer

  -	Route

  -	API Discovery

## Guide

Create a Custom Route

![Custom Route](static/custom_route_name.jpg)

Add Route Matching configuration

![Route Match](static/custom_route_match.jpg)

Add Route Action, Direct Response

![Direct Response](static/custom_route_direct_config.jpg)

Updated Response Body (JSON Format)

![Response Body](static/response_body.jpg)

[response body content](response_body.json)

Expand Advanced Options, Add Response Header

![Adv Response Header](static/custom_route_adv_add_header.jpg)

Update Response Header

![Header Config](static/custom_route_adv_add_header.jpg)

Save and Exit

-------------------------------------------------------------------

Created a HTTP Load Balancer, specifying your desired configuration
-	Load Balancer Name
-	Domains
-	Load Balancer Type

_Additional References @ [F5 Tech Docs - HTTP Load Balacer](https://docs.cloud.f5.com/docs/how-to/app-networking/http-load-balancer)_

Create a Route within the Load Balancer

![Route](static/route.jpg)

Attach Custom Route

![Route](static/attach_custom_route.jpg)

Enable API Discovery

![Route Response List](static/discovery_enabled.jpg)

## Load Balancer Templates

HTTP without Managed DNS

[lb_template_http](lb_template_http.json)

HTTP with Managed DNS

[lb_template_http_dns](lb_template_http_dns.json)

HTTPS with Auto Certificate

[lb_template_https_auto_cert](lb_template_https_auto_cert.json)

HTTPS with Custom Certificate (Multiple Certificate)

[lb_template_https_multi_cert](lb_template_https_multi_cert.json)