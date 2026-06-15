# Non-functional requirements

## What are non-functional requirements

Non‑functional requirements (NFRs) are requirements that do not describe what the system does in terms of its purpose, but instead in terms of how well it behaves or feels. For example, *the system must translate text entered by the user into Chinese* is a functional requirement because it relates to the system's purpose, but *the system must protect its text inputs from SQL injection* is a non-functional requirement because it describes how the system must be able to look after itself.

## Examples of non-functional requirements

### Performance
* response time
* throughput
* latency

### Scalability
* ability to handle growth

### Availability
* uptime
* redundancy [?]

### Reliability
* consistency of operation

### Security
* confidentiality
* integrity
* authentication

### Maintainability
* ease of fixing
* updating
* refactoring

### Observability
* logs
* metrics
* traces

### Usability
* how easy it is to figure out
* how long it takes to perform tasks
* accessibility

### Portability
* ability to run in different environments

### Compliance
* legal
* regulatory
* industry rules

These are the “architectural forces” that shape every design decision.

## Specifying NFRs

NFRs should be specified in a measurable way. For example:

* *95% of requests must complete within 200 ms.*
* *System must support 10,000 concurrent users.*
* *99.95% availability per month.*
* *Recover from failure within 30 seconds.*
* *All data at rest must be encrypted with AES‑256.*

SMART is a good tool for specifying NFRs:

* Specific
* Measurable
* Testable
* Relevant
* Time‑bound (if needed)

### A good example

> All external API calls must require OAuth2 access tokens with a maximum lifetime of 60 minutes.

### A bad example

> The system should be secure.

## NFRs and trade‑offs

NFRs generally imply some kind of trade-off because they often conflict with one another. Here are some examples:

* Security vs usability
* Availability vs cost
* Performance vs maintainability [?]
* Consistency vs scalability
* CAP theorem

## How NFRs shape architecture

Take for example this requirement:

> System must handle 5,000 requests per second.

This may push you towards:
* asynchronous messaging
* horizontal scaling (and consequently, load balancing)
* stateless services
* caching layers
* load balancing
* partitioned databases

# Links

| Link      | Description |
| ----------- | ----------- |
| https://en.wikipedia.org/wiki/Non-functional_requirement | Non-functional requirement on Wikipedia |
| https://quality.arc42.org/articles/sei-quality-model | Summary of differences between the SEI (Software Engineering Institute) quality model and that of Arc42 |
| https://microsoft.github.io/code-with-engineering-playbook/design/design-patterns/non-functional-requirements-capture-guide/ | Examples of a wide range of NFRs authored by Microsoft |
| https://www.amazon.co.uk/dp/1098175514 | Fundamentals of Software Architecture: A Modern Engineering Approach (Richards & Ford) |
| https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html | AWS Well-Architected Framework - Copilot recommends the 'Pillars' sections |
| https://www.amazon.co.uk/Building-Evolutionary-Architectures-Automated-Governance/dp/1492097543 | Building Evolutionary Architectures: Automated Software Governance (Ford, Parsons, Kua, Sadalage) - Focuses on fitness functions — automated ways to enforce NFRs |
| https://github.com/joelparkerhenderson/system-quality-attributes | Appears to be a personal repository by someone who is studying system quality attributes - very rich information and links |
| https://iso25000.com/index.php/en/iso-25000-standards/iso-25010 | ISO/IEC 25010 Quality Model - The international standard for software quality attributes |


