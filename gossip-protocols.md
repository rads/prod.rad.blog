---
title: Gossip Protocols
---

## References

- ["Gossip protocol" on Wikipedia](https://en.wikipedia.org/wiki/Gossip_protocol)
    - A good starting point.
- [*Epidemic Algorithms for Replicated Database Maintenance*](https://pdfs.semanticscholar.org/49ed/15db181c74c7067ec01800fb5392411c868c.pdf) (1987)
    - The pioneering paper of gossip protocols (but out-of-date)
- [*Lightweight Probabalistic Broadcast*](http://perso.telecom-paristech.fr/~kuznetso/pubs/Lpbcast_tocs.pdf) (2003)
    - More research needed
- [*HyParView: a membership protocol for reliable gossip-based broadcast*](http://asc.di.fct.unl.pt/~jleitao/pdf/dsn07-leitao.pdf) (2007)
    - Used as part of the paper below
- [*Epidemic Broadcast Trees*](http://www.gsd.inesc-id.pt/~jleitao/pdf/srds07-leitao.pdf) (2007)
    - More research needed
    - Not sure how efficient this is compared to Scuttlebutt
- [*Efficient Reconciliation and Flow Control for Anti-Entropy Protocols*](https://www.cs.cornell.edu/home/rvr/papers/flowgossip.pdf) (2008)
    - Also known as Scuttlebutt
    - Easy to implement, modern algorithm
- [*EpTO: An Epidemic Total Order Algorithm for Large-Scale Distributed Systems*](http://haslab.uminho.pt/mmatos/files/p100-matos.pdf) (2015)
    - More research needed
- [*Epidemic Algorithms for Log Sharing with Onyx*](https://www.dropbox.com/s/vs2gmpq32dtszwd/Project_Report_Sondre_Basma.pdf?dl=0) (2016)
    - More research needed
- ["ArchitectureGossip" on the Cassandra Wiki](https://wiki.apache.org/cassandra/ArchitectureGossip)
    - Describes Cassandra's membership protocol (based on Scuttlebutt)
