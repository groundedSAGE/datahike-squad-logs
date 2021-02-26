- Related:: [[Product Vision]]
- ## This is currently a work in progress!!
    - We also want to try and put a timeframe on when we plan to reach said releases
- ### 0.4.0
    - [[Epics/Make Datahike Development Transparent]]
    - [[epic/ClojureScript Support]]
    - [[epic/Distributed Connection Management]]
    - [[epic/Query Planner and Optimizer]]
    - [[epic/Dev Tooling]]
- ### Future Opportunities
    - [[epic/Optionally use [[core.async]] to Handle Storage IO]]
    - [[epic/Transaction Monitoring]]
    - [[epic/CRDT Type Schema Support]]
    - [[epic/Identity and Access Management]]
    - [[epic/Support Optimistic Write Support Through Attributes with Conflict Resolution (CRDT-like)]]
    - [[epic/GraalVM Native Binary]]
    - [[epic/Native Support for Datahike on CLR]]
    - [[epic/Native Support for Datahike on BEAM]]
- ---
- What is ready?
- GC is nearly ready. not really an epic.  A story that relates to query planner and distributed connection management
- ---
- Roadmap from Github
    - ### 0.4.0
        - identity and access management
        - CRDT type schema support
        - fast redis backend support
        - query planner and optimizer
        - transaction monitoring
    - ### 0.5.0
        - optionally use core.async to handle storage IO
        - ^^ClojureScript support both in the browser and on node^^
    - ### 0.6.0
        - support GC or eager deletion of fragments
        - use hitchhiker-tree synchronization for replication
        - run comprehensive query suite and compare to DataScript and Datomic
        - support anomaly errors (?)
    - ### 1.0.0
        - support optimistic write support through attributes with conflict resolution (CRDT-like)
        - investigate https://github.com/usethesource/capsule for faster hh-tree durability
- From Christian
    - Roadmap suggestion
 
 0.4.1
    -  - GC
 - query performance improvements
 - updating of all konserve backends including DynamoDB/S3
     

__***__* 0.4.2
- better error messages
     - safe Datalog clause reorderings (static analysis)
     - GraalVM support (if possible)

__***__ 0.5.0 
- ClojureScript support on IndexedDB
    - remote connection support for datahike-server transactor
    - general URI based address scheme for databases globally
    - cross-platform joins between frontend and backend databases

   
__***__ 0.6.0 
- RDF compatible schemas and translation (semantic web)
    - resource/cost model for query execution and planning
    - general interface definitions and semantics independent of Clojure
    - attribute-based CRDT support (preview)
    - 
    __***__ 1.0.0 
  - full CRDT support including fully decentralized P2P version
    - run queries on distributed infrastructure
    - JIT compiled Datalog runtime for Clojure/ClojureScript
    - integration of Datalog for static analysis in Clojure compiler/macroexpander
    - non-Clojure Datalog query runtime implementation for e.g. Julia, Python,
      Ruby or Rust

  
- CLJS branch
    - ### 0.4.1
        - GC
        - query performance improvements
        - updating of all konserve backends including DynamoDB/S3
    - ### [](https://github.com/replikativ/datahike/tree/206-cljs-support#042)0.4.2
        - better error messages
        - safe Datalog clause reorderings (static analysis)
        - GraalVM support (if possible)
    - ### [](https://github.com/replikativ/datahike/tree/206-cljs-support#050)0.5.0
        - ClojureScript support on IndexedDB
        - remote connection support for datahike-server transactor
        - general URI based address scheme for databases globally
        - cross-platform joins between frontend and backend databases
    - ### [](https://github.com/replikativ/datahike/tree/206-cljs-support#060)0.6.0
        - RDF compatible schemas and translation (semantic web)
        - resource/cost model for query execution and planning
        - general interface definitions and semantics independent of Clojure
        - attribute-based CRDT support (preview)
    - ### [](https://github.com/replikativ/datahike/tree/206-cljs-support#100)1.0.0
        - full CRDT support including fully decentralized P2P version
        - run queries on distributed infrastructure
        - JIT compiled Datalog runtime for Clojure/ClojureScript
        - integration of Datalog for static analysis in Clojure compiler/macroexpander
        - non-Clojure Datalog query runtime implementation for e.g. Julia, Python, Ruby or Rust
- [[Archived Content]]
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamAgile%2FOF7H8b78CH.png?alt=media&token=291ef1fc-a579-42f9-aecc-35ae579a7e5b)
        - Read: [Epics | Atlassian](https://www.atlassian.com/agile/project-management/epics)
