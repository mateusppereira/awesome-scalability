# [How Slack Built Shared Channels](https://slack.engineering/how-slack-built-shared-channels/)

> The idea of shared channels challenged Slack’s fundamental assumption that the workspace is the atomic unit of partitioning customer data, however

There were no cross workspace data.

The workspace defines the shard all the data will be,

> In essence, the workspace was the unit of tenancy in the multi-tenant service, used for data partitioning and segmentation.

They decided not try to keep a copy of the data on both shards due to the volume of data that this would generate and to the potential of inconsistencies between those.

The approach they end was to store channel data in origin shard and have a reference to the other workspace that would have the same channel.


This showed the challenge that we have when using a sharded architecture and we need to keep in mind that one day cross shard communication will be needed