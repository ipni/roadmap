# Project Progress

Work in progress. See [project goals](/goals.md) for more detail on which outcome(s) each work item supports.

## Work Items

1. P1: Double-cursor Ingest
    a. Supports: reliable, expectations
       1. Target: allow new replicas to go from startup to offloading traffic load from the system w/i 2 days
    b. This component will support shortened recovery time
1. P1.5: Compaction-free KV Store
    a. Supports: reduced operational overhead of long-lived KV backbone of IPNI
    b. Target: significantly decrease the operational footprint and resource consumption of IPNI for better IO utilisation.
2. P1: Car-mirror upkeep
    a. Supports: reliable, decentralized
    b. Target: exposed full car mirror other instances can use to start up faster
        1. This component will support shortened recovery time
3. P1.25: Per-provider metering / billing
    a. Supports: up-front expectations, responsive, simple
    b. Target: we know what fraction of overall resources are attributable to each provider
4. P2: Indexer Auto-Discovery
    a. Supports: decentralized, Nearby
    b. Target: Library allows querying without cid.contat hardcoded, able to be integrated into IPFS web&desktop clients w/ buy-in from shipyard
5. P1.5: Additional Instance
    a. Supports: decentralized, nearby
    b. Target: Additional full instance running from other entity