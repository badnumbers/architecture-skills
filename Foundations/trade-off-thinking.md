# Trade-off thinking

## What is trade-off analysis?

Trade-off analysis is the examination of how architectural decisions impact quality attributes. A given decision will likely improve certain attributes while degrading others. Trade-off analysis starts with the assumption that there is no perfect architecture and our decisions will necessarily be compromises.

## Advantages of trade-off analysis

- risks are identified before implementation
- quality attributes are clarified
- a rationale for decisions
- identifies interactions between quality attributes

## What formal methods are there for performing trade-off analysis?

The most established formal method is [ATAM](https://en.wikipedia.org/wiki/Architecture_tradeoff_analysis_method) (Architecture Trade-off Analysis Method) developed by Carnegie Mellon’s Software Engineering Institute. This process involves stakeholders identifying business drivers (e.g. the goals of the system, expected constraints, NFRs) in order to derive a list of quality attributes which in turn create *scenarios*. These scenarios are used to examine approaches and to get at the trade-offs, risks and sensitivity points [?].

Each analysis cycle is expected to result in further questions at deeper, more specific levels.

### Steps in ATAM

ATAM formally has the following 9 steps (quoted directly from Wikipedia):

1. Present ATAM – Present the concept of ATAM to the stakeholders, and answer any questions about the process.
1. Present business drivers – everyone in the process presents and evaluates the business drivers for the system in question.
1. Present the architecture – the architect presents the high-level architecture to the team, with an 'appropriate level of detail'
1. Identify architectural approaches – different architectural approaches to the system are presented by the team, and discussed.
1. Generate quality attribute utility tree – define the core business and technical requirements of the system, and map them to an appropriate architectural property. Present a scenario for this given requirement.
1. Analyze architectural approaches – Analyze each scenario, rating them by priority. The architecture is then evaluated against each scenario.
1. Brainstorm and prioritize scenarios – among the larger stakeholder group, present the current scenarios, and expand.
1. Analyze architectural approaches – Perform step 6 again with the added knowledge of the larger stakeholder community.
1. Present results – provide all documentation to the stakeholders.

TODO: find out about *quality attribute utility tree*.

These 9 steps are divided into 2 phases. Phase 1 consists of steps 1 to 6 and focuses on establishing information. Phase 2 consists of steps 7 to 9 and focuses on decision making and presentation.

## Somewhat less obvious factors in decision making

Although rarely considered quality attributes as such, the following are also important factors in architectural decision making that may impact trade-off analysis:

- Cost
- Time
- Skill levels (does anyone know this platform?)
- Resource availability (obviously linked to point above)

Another less-discussed aspect of trade-off analysis is that since we want to engage stakeholders, we must create an environment for discussion that is inclusive, supportive and balanced.

## Examples of trade-offs

| Decision      | Good for | Bad for |
| ----------- | ----------- |
| Microservices | Scalability, deployability | Complexity, operational overhead [?] |
| Monolith | Simplicity, performance [?] | Modifiability, team autonomy |
| Caching | Performance | Performance [ not to mention ease of  support! ] |
| Strong security controls | Security, privacy | Usability, latency |
| Event‑driven architecture | Decoupling, scalability | Debuggability, eventual consistency |

## Summary

In trade-off analysis we acknowledge that the perfect architecture is probably not possible. So we strive to choose options that favour the quality attributes identified as being most important to the system, at the expense of those least important.

Architectural failures come not so much from bad designs, but from unexamined assumptions and unidentified requirements. ATAM, and other processes for trade-off analysis, seek to bring those into the light.

# Links

| Link      | Description |
| ----------- | ----------- |
| https://en.wikipedia.org/wiki/Architecture_tradeoff_analysis_method | ATAM in Wikipedia |
| https://moldstud.com/articles/p-architectural-trade-off-analysis-balancing-competing-factors-in-design-decisions | An excellent simple-page summary of architectural decision making. |