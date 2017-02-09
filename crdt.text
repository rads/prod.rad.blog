---
title: CRDT
---

An acronym for **Conflict-free Replicated Data Type**.

## Getting Started

This talk by Marc Shapiro is an excellent introduction to what CRDTs are and how they work:

<iframe width="560" height="315" src="https://www.youtube.com/embed/ebWVLVhiaiY" frameborder="0" allowfullscreen></iframe>

## References

- [*A comprehensive study of Convergent and Commutative Replicated Data Types*](http://hal.upmc.fr/inria-00555588/document) (2011)
- [*Decoupling conflicts for configurable resolution in an open replication system*](https://arxiv.org/pdf/1508.05545.pdf) (2016)

## Related Terms

[Replication](replication)

## Implementations

- Clojure
    - [replikativ](http://replikativ.io/) ([Bliki](replikativ))
        - replikativ is a library that offers many CRDTs including LWWR, G-Set, OR-Map, and CDVCS (an append-only graph)
- Erlang
    - [CouchDB](https://couchdb.readthedocs.io/en/latest/replication/protocol.html)
- JavaScript
    - [hyperlog](https://github.com/mafintosh/hyperlog) ([Bliki](hyperlog))
        - hyperlog is a CRDT because two append-only Merkle DAGs can inherently be merged in either order. In other words, the internal replication updates among hyperlogs are commutative.
    - [Scuttlebot](https://github.com/ssbc/scuttlebot) ([Bliki](scuttlebot))
        - Scuttlebot is a CRDT because a) writes to concurrent streams do not conflict with each other and b) conflicts within streams are handled using (as far as I know) last-write-wins semantics using the message's locally-recorded timestamp.
    - [PouchDB](https://pouchdb.com/)
        - A client for CouchDB in JavaScript.
        - [Decentralized, not distributed](distributed-systems): PouchDB relies on an external CouchDB server to talk to other peers.
