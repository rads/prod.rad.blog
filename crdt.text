---
title: CRDT
---

An acronym for **Conflict-free Replicated Data Type**.

## Getting Started

<figure class="right">
  <a href="https://www.youtube.com/watch?v=ebWVLVhiaiY">
    <img src="shapiro.jpg" width="469">
  </a>
  <caption>Marc Shapiro</caption>
</figure>

See [this talk on YouTube][talk] by Marc Shapiro for an excellent introduction on what CRDTs are and how they work.

[talk]: https://www.youtube.com/watch?v=ebWVLVhiaiY

## References

- [*A comprehensive study of Convergent and Commutative Replicated Data Types*](http://hal.upmc.fr/inria-00555588/document) (2011)
- [*Decoupling conflicts for configurable resolution in an open replication system*](https://arxiv.org/pdf/1508.05545.pdf) (2016)

## Related Terms

[Replication](replication)

## Implementations

See [TodoP2P][todop2p] for example projects using some of these libraries.

[todop2p]: https://github.com/rads/todop2p

- Clojure
    - [replikativ](http://replikativ.io/) ([Bliki](replikativ))
        - replikativ is a library that offers many CRDTs including LWWR, G-Set, OR-Map, and CDVCS (an append-only graph)
        - Uses WebSockets as wire
- Erlang
    - [CouchDB](https://couchdb.readthedocs.io/en/latest/replication/protocol.html)
        - CouchDB uses a Merkle DAG like hyperlog and Git
- JavaScript
    - [hyperlog](https://github.com/mafintosh/hyperlog) ([Bliki](hyperlog))
        - hyperlog is a CRDT because two append-only Merkle DAGs can inherently be merged in either order. In other words, the internal replication updates among hyperlogs are commutative.
        - Uses Node.js streams as wire
    - [Scuttlebot](https://github.com/ssbc/scuttlebot) ([Bliki](scuttlebot))
        - Scuttlebot is a CRDT because a) writes to concurrent streams do not conflict with each other and b) conflicts within streams are handled using (as far as I know) last-write-wins semantics using the message's locally-recorded timestamp.
    - [PouchDB](https://pouchdb.com/)
        - A client for CouchDB in JavaScript.
        - [Decentralized, not distributed](distributed-systems): PouchDB relies on an external CouchDB server to talk to other peers.
        - Uses HTTP as wire
