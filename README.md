# F5 Distributed Cloud - Simple API Discovery

Simple method for providing API Discovery via Distributed Cloud for APIs that are not proxied by Distributed Cloud.

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

![LB Template HTTP](https://github.com/stockerts/f5xc-app-discovery/blob/main/lb_template_http.json)

HTTP with Managed DNS

![LB Template HTTP](https://github.com/stockerts/f5xc-app-discovery/blob/main/lb_template_http_dns.json)

HTTPS with Auto Certificate

![LB Template HTTP](https://github.com/stockerts/f5xc-app-discovery/blob/main/lb_template_https_auto_cert.json)

HTTPS with Custom Certificate (multi)

![LB Template HTTP](https://github.com/stockerts/f5xc-app-discovery/blob/main/lb_template_https_multi_cert.json)