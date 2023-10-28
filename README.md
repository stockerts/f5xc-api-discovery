# F5 Distributed Cloud - Simple App Discovery

Simple method for providing Application and API Discovery via Distributed Cloud for Applications & APIs that are not proxied by Distributed Cloud.

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

## Guide

![Object Flow](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/object_flow.jpg?raw=true)

Created a HTTP Load Balancer, specifying your desired configuration

•	Load Balancer Name

•	Domains

•	Load Balancer Type

Create a Route within the Load Balancer

![Route](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route.jpg?raw=true)

![Route Response List](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route_response.jpg?raw=true)

![Route Response Type](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route_type_response.jpg?raw=true)

![Response Body](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/response_body.jpg?raw=true)
