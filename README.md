# roadmap

Current information on the roadmap for improvements to the IPNI system.
See [project goals](/goals.md) for context.

Work for which funding has been approved is detailed in [progress](/progress.md).
Backlog work awaiting funding and/or staffing commitments is detailed in the [backlog](/backlog.md)

## Project Goals

IPNI is a content routing system optimized to take billions of CIDs from large data providers, and provide fast lookup of provider information from these CIDs over a simple HTTP REST API.

IPNI has been load-bearing for years, but with greater dependence on IPNI from a growing and increasingly diverse set of stakeholders, new usage patterns have emerged, and a few serious brown-outs shook confidence in the system.
For this reason, technical and process improvements are being proposed and funded to iterate and improve IPNI.
The following design goals organize both the in-progress work items and the backlog items.

### What an impactful IPNI looks like

- A. Reliable & Conceptually Simple
  - The abstraction of a 'key value store' just works, without additional thought having to be put in by the publisher/consumer. Key Value operations (reads and writes) work with a 5-nines (99.999%) success rate.
- B. Nearby
  - There is a federated instance in the region of any given client, such that queries are reliably answered within ~50ms
- C. Up-front expectations
  - Publishers / partners understand the community-level limits (TBD ingest latency, daily publishing rate), and how they can get further service through payments. The payment amounts are reasonable for the service provided.
    - We can explain our pricing model (e.g. a premium tier once you hit n MB / m items per day, or for stronger SLAs)
- D. Decentralized
  - The operations do not depend on a single entity; there is a functional governance/coordination process;
- E. Responsive
  - As new use cases are identified, the system is able to evolve quickly meet additional requirements

## Work In Progress

The following work-packages have already been funded.
Exact milestones and timeline expectations are hard to determine for these items, as the limited funding and staffing alotted to the improvements listed below can get significantly diluted triaging users and getting providers better debugging information.
See [Project Goals](#project-goals) above for more detail on which outcome(s) each work item supports.

### Work Items

- 1.) (P1) Double-cursor Ingest
  - Supports: reliable, expectations
    - Target: allow new replicas to go from startup to offloading traffic load from the system w/i 2 days
  - This component will support shortened recovery time
- 2.) (P2) Compaction-free KV Store
  - Supports: reduced operational overhead of long-lived KV backbone of IPNI
  - Target: significantly decrease the operational footprint and resource consumption of IPNI for better IO utilisation.
- 3.) (P1) Car-mirror upkeep
  - Supports: reliable, decentralized
    - Target: exposed full car mirror other instances can use to start up faster
      - This component will support shortened recovery time
- 4.) (P2) Per-provider metering / billing
  - Supports: up-front expectations, responsive, simple
  - Target: we know what fraction of overall resources are attributable to each provider
- 5.) (P3) Indexer Auto-Discovery
  - Supports: decentralized, Nearby
  - Target: Library allows querying without `cid.contact` hardcoded, able to be integrated into IPFS web&desktop clients w/ buy-in from [IP Shipyard](https://ipshipyard.com/)
- 6.) (P2) Additional Instance
  - Supports: decentralized, nearby
  - Target: Additional full instance running by another entity

## Backlog

Future work items proposed by the team but awaiting funding and/or staffing. Feel free to open issues about these proposals and their relative priority, especially if you(r organization) would contribute directly or monetarily.
Pull requests to add to this list without discussion on community calls and/or detailed user stories in issues will not be considered!

- 7.) (P3) Checkpoint
  - Supports: reliable
  - Target: be able to get a snapshot transferred rather than full-ingest from a provider
- 8.) (P3) Vector-Clock Consensus
  - Supports: decentralized
  - Target: be able to get a consistent response from multiple indexer instances
- 9.) (P3) Alternate publishing mechanisms
  - Supports: simple
  - Target: be able to support direct pushes
- 10.) (P3) Governance evolution
  - Supports: reliable, decentralized
  - Target: healthy federation with governance beyond our team
