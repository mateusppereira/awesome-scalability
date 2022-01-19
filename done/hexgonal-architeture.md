# Ready for changes with hexagonal architecture

inputs and outputs at the edges of our design. Business logic should not depend on whether we expose a REST or a GraphQL API, and it should not depend on where we get data from — a database, a microservice API exposed via gRPC or REST, or just a simple CSV file

One of the main advantages we also saw in having an app with clear boundaries is our testing strategy

### Core concpts

Entities: domain objects (no knowledge of how they are stored)

Repositories: interfaces to get, store and change entities on any data source

Interactors: where business logic lives (services)

Data sources: implementation to fetch and push data (DB communication, CSV reader, resp api interface)

Transport layer: inputs for the system. HTTP API layer, message consuming listener, cronjob, command line


---
https://netflixtechblog.com/ready-for-changes-with-hexagonal-architecture-b315ec967749