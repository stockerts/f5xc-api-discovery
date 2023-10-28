# F5 Distributed Cloud - Simple App Discovery

Simple method for providing API Discovery via Distributed Cloud for APIs that are not proxied by Distributed Cloud.

## Flow

![Object Flow](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/object_flow.jpg?width="200")

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

Created a HTTP Load Balancer, specifying your desired configuration

•	Load Balancer Name

•	Domains

•	Load Balancer Type

Create a Route within the Load Balancer

![Route](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route.jpg?width="200")

Update Response Type, Edit Direct Reponse configuration

![Route Response Type](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route_type_response.jpg?width="200")

Updated Response Body (JSON Forma)

![Response Body](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/response_body.jpg?width="200")

Confirm Route List

![Route Response List](https://github.com/stockerts/f5xc-app-discovery/blob/main/static/route_response.jpg?width="200")
