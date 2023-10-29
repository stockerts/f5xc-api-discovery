# F5 Distributed Cloud - Simple API Discovery

Simple method for providing API Discovery via Distributed Cloud for APIs that are not proxied by Distributed Cloud.

## Table of Contents
1. [Flow](##Flow)
2. [Outcomes](##Outcomes)
3. [Limitations](##Limitations)
4. [Requirements](##Requirements)
5. [Example Discovery](##Example Discovery)
6. [Guide](##Guide)
7. [Load Balancer Templates](##Load Balancer Templates)

## Flow

![Object Flow](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/flow.png)

## Outcomes

Path Discovery (Leaf Creation)

Request Sensitive Data Detection (PUT, POST)

## Limitations

No Response Sensitive Data Detection

No Authentication Detection

No Performance Statistics

## Requirements

HTTP(S) Web Request

Distributed Cloud Tenant

•	Load Balancer

•	API Discovery

•	Route

## Example Discovery

![Path](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/leaf.jpg)

![Detection](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/discovery.jpg)

## Guide

Created a HTTP Load Balancer, specifying your desired configuration

•	Load Balancer Name

•	Domains

•	Load Balancer Type

Create a Route within the Load Balancer

![Route](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route.jpg)

Update Response Type, Edit Direct Reponse configuration

![Route Response Type](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route_type_response.jpg)

Updated Response Body (JSON Format)

![Response Body](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/response_body.jpg)

Confirm Route List

![Route Response List](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route_response.jpg)

## Load Balancer Templates (JSON)

HTTP without Managed DNS

[lb_template_http](lb_template_http.json)

HTTP with Managed DNS

[lb_template_http_dns](lb_template_http_dns.json)

HTTPS with Auto Certificate

[lb_template_https_auto_cert](lb_template_https_auto_cert.json)

HTTPS with Custom Certificate (Multiple Certificate)

[lb_template_https_multi_cert](lb_template_https_multi_cert.json)