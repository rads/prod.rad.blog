---
title: hyperlog
---

GitHub: [https://github.com/mafintosh/hyperlog](https://github.com/mafintosh/hyperlog)

## Replication Protocol

> - Every user has their own scuttlebutt like log (append-only log).
> - When a user insert a new node into the graph they also add this node to their own log. If their graph node has a link to another users log they'll record that in an index (lets call this index A).
> - When replicating you look at the heads of your graph (the nodes that no one points to). You'll send back a scuttlebutt like handshake for each of the logs that head nodes are stored in.
> - If the remote user doesn't have the head log, or if their latest node is this log is older than the seq returned in the handshake they'll send a request for the diff.
> - If you send back a node that has a reference to another feed in index A, send back the scuttlebutt handshake for that particular log.
> 
> So when a user does hyperlog.add(links, node) hyperlog will lookup the nodes referenced by the links array and see which logs they belong too. If any of those logs are different than our own local log that information is stored in an internal index.
