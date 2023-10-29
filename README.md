# F5 Distributed Cloud - Simple API Discovery

Simple method for providing API Discovery via Distributed Cloud for APIs that are not proxied by Distributed Cloud.

## Table of Contents
1. [Flow](#flow)
2. [Outcomes](#outcomes)
3. [Limitations](#limitations)
4. [Requirements](#requirements)
5. [Example Discovery](#example-discovery)
6. [Guide](#guide)
7. [Load Balancer Templates](#load-balancer-templates)

## Flow

![Object Flow](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/flow.png)

## Outcomes

- Path Discovery (Leaf Creation)

- Request Sensitive Data Detection (PUT, POST)

## Limitations

- No Response Sensitive Data Detection

- No Authentication Detection

- No Performance Statistics

## Requirements

- HTTP(S) Web Request

- Distributed Cloud Tenant

  -	Load Balancer

  -	Route

  -	API Discovery

## Example Discovery

Path Discovery (Leaf Creation)

![Path](static/leaf.jpg)

Request Sensitive Data Detection (PUT, POST)

![Detection](static/discovery.jpg)

## Guide

Created a HTTP Load Balancer, specifying your desired configuration
-	Load Balancer Name
-	Domains
-	Load Balancer Type

_Additional References @ [F5 Tech Docs - HTTP Load Balacer](https://docs.cloud.f5.com/docs/how-to/app-networking/http-load-balancer)_

Create a Route within the Load Balancer

![Route](static/route.jpg)

Update Response Type, Edit Direct Reponse configuration

![Route Response Type](static/route_type_response.jpg)

Updated Response Body (JSON Format)

![Response Body](static/response_body.jpg)

Confirm Route List

![Route Response List](static/route_response.jpg)

Enable API Dicovery

![Route Response List](static/discovery_enabled.jpg)

## Load Balancer Templates (JSON)

HTTP without Managed DNS

[lb_template_http](lb_template_http.json)

HTTP with Managed DNS

[lb_template_http_dns](lb_template_http_dns.json)

HTTPS with Auto Certificate

[lb_template_https_auto_cert](lb_template_https_auto_cert.json)

HTTPS with Custom Certificate (Multiple Certificate)

[lb_template_https_multi_cert](lb_template_https_multi_cert.json)