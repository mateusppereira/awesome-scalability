# [Scalability Worst Practices](https://www.infoq.com/articles/scalability-worst-practices/)

## Golden Hammer

Same solution to different problems.

e.g. SQL database will neves scale for a key value storage as a non-relational database will

## Resource abuse

Caution with shared resources.

e.g. connection pool to a database

## Dependencies

Backwards-compatible changes. Versioning.

## No timing manage

> Regardless of implementation language or architecture, proper latency management is imperative

## Hero pattern

> The Hero often understands service dependencies when no formal specification exists. [...] **The Hero is crucial but the Hero should not be an individual**

## Non effective monitoring

> The lack of visibility into the internals of a running system [...] jeopardizes the ability to make accurate and critical decisions about where to look and what to look for


