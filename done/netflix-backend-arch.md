# [Netflix System Design- Backend Architecture](https://dev.to/gbengelebs/netflix-system-design-backend-architecture-10i3)

## Backend Architechture

### All in AWS
> When the user loads the Netflix app all requests are handled by the backend server in AWS Eg: Login, recommendations, the home page, users history, billing, customer support. Some of these backend services include (AWS EC2 instances, AWS S3, AWS DynamoDB, Cassandra, Hadoop, Kafka, etc)

### Microservice based
> Every component of their system is a collection of loosely coupled services collaborating. The microservice architecture enables the rapid, frequent and reliable delivery of large, complex applications

> Microservices are mostly stateless small programs

> Microservices can save or get data from a data store during this process

### Uses ELB and API Gateway
> dynamic routing, traffic monitoring, and security, resilience to failures at the edge of the cloud deployment

### Stream Processing Pipeline
> Microservices can send events [...] to the Stream Processing Pipeline for either real-time processing [...] or batch processing of business intelligence tasks.

> The data coming out of the Stream Processing Pipeline can be persistent to other data stores such as AWS S3, Hadoop HDFS, Cassandra, etc

https://www.confluent.io/blog/how-kafka-is-used-by-netflix/

## Open Connect Appliences (OCA)
It's a custom CDN used to deliver the content and placed insige Internet service providers and Internet Exchange Locations (ISPs and IXPs)

> 1. OCAs ping AWS instances to report their health, the routes they have learned, and the files they have on them.
> 2. A user on a client device requests playback of a title (TV show or movie) from the Netflix application in AWS.
> 3. The Netflix playback service checks for the user's authorization, permission, and licensing, then chooses which files to serve the client taking into account the current network speed and client resolution.
> 4. The steering service picks the OCA that the files should be served from, generates URLs for these OCAs, and hands it back to the playback service.
> 5. The playback service hands over the URLs of the OCA to the client, The client requests for the video files from that OCA

### Cache
They have caching on SSD instead of RAM due to cost :interesting:

### Cassandra
> All user collected event metrics are stored on Cassandra.

> In effect, a single global Cassandra cluster can simultaneously service applications and asynchronously replicate data across multiple geographic locations