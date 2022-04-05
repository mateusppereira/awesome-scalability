# Designing and Implementing AWS Networks

## VPC
networking environment dedicated to a single customer

components:
  - route tables
  - internet gateways
  - access controll (inbound and outbound)
  - vpn components
  - nat gateways
  - elastic ip addesses

vpc is dedicated to only one region (us-east-1, sa-east-1, ...)

vpc can have multiple subnets and each of them is dedicated to only one Avalilability Zone (us-east-1a, us-east-1b, us-east-1c, ...)

vpc has a route table (?)

benefits of connectiing aws vpc over go through internet:
  - secure (your data transfer on an private clound)
  - lower latency
  - cheap (no transfer-out costs)

### Multiple VPC's

using multiple vpc infrastructure enable you to have multi region, different aws accounts and isolated environments

to use muiltiple vpc you need to configure route table for vpc peering (manual/static route table)

another way to communicate vpc is using transit gateway

### Route 53

used primary for name resolution


### Cloudfront

content delivery network (CDN)

improve performance: reduce latency and cache content

improve availability: cache content


### Elastic Load Balancing

share incoming request to N instances assuring certain instance dont become a bottleneck

improve availability: dont send traffic to unhealth instances


[ref](https://app.pluralsight.com/library/courses/designing-implementing-aws-networks/table-of-contents)
