---
title: Scuttlebot
---

- GitHub: [https://github.com/ssbc/scuttlebot](https://github.com/ssbc/scuttlebot)
- FAQ: [https://ssbc.github.io/docs/ssb/faq.html](https://ssbc.github.io/docs/ssb/faq.html)

## Message Ordering

> **Is there a global total order in SSB?**
>
> No. There is, however, a global partial order.
> 
> An individual feed has an internal total order. Every message contains a sequence number and a pointer to the previous message in that feed.
> 
> If feed A posts a message that links to a message in feed B, then we know that A's message is after B's. That is, message-links imply a happens-before relationship. (This is because, in order to know the hash of an object, that object must already exist.)
> 
> Messages contain monotonically increasing UTC timestamps and sequence numbers. This means you can assign an order to any two messages. However, be aware that there is no way to ensure that the timestamp is accurate.
