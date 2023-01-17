# [Building Twitter’s ad platform architecture for the future](https://blog.twitter.com/engineering/en_us/topics/infrastructure/2020/building-twitters-ad-platform-architecture-for-the-future)

## Legacy infrastructure problems

### New products were hardcoded and not congfigurable
The steps to add a new Ad were strict and coupled

### Data access 
Very sensitive to add new user data due to very low latency required.

### Technical debt
The complexity increased in a way developers didn't have confidence to do simple changes that could lead to unintended changes in funcionality

## Solution arch

They've identified horizontal services that could be shared across different types of Ads and provided than as a horizontal platform.

Considering this, a new type of Ad would required developers just to plug in the horizontal services they need.

