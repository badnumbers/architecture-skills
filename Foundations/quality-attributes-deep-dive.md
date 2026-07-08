# Quality attributes deep dive

## Many subgroupings

Various sources provide different ways of categories quality attributes. I will summarise some of those here.

## ISO/IEC 25010

- Software product quality

### Functional suitability

*Functional completeness*, *functional correctness*, *functional appropriateness* [not clear what this latter means]

### Performance efficiency

*Time behaviour* (e.g. response times), *resource utilisation* (anything e.g. CPU, energy, materials), *capacity* (i.e. maximum throughput)

### Compatibility

*Coexistence* (not impacting other applications in the same environment), *interoperability* (ability and exchange information and use exchanged information)

### Interaction capability

*Appropriateness recognisability* (whether users can recogise whether it meets their needs), *learnability*, *operability* (easy to operate and control), *user error protection* (prevents users making errors), *user engagement* (is 'inviting and 'motivating'), *inclusivity* (can be used by people of various backgrounds e.g. ethnic / ability), *user assistance* [not clear what this means], *self-descriptiveness* (I think easy to figure out before going to manual)

### Reliability

*Faultlessness* ('performs specified functions without fault') [error or outage?], *availability*, *fault tolerance* (can work even when there are hardware or software faults), *recoverability* (ability to reestablish 'desired state')

### Security

*Confidentiality* (access to data only to those authorised), *integrity* (guards against unauthorised changes / deletions), *non-repudiation* (proof offered of events + inability to alter the proof), *accountability* (ability to trace actions uniquely to author), *authenticity* (identity of subject or resource can be proven) [perhaps like AAL?], *resistance* (sustains operations while under attack) [DDOS prevention?]

### Maintainability

*Modularity* (changing one thing doesn't change others), *reusability* (something can be reused in more than one place or as a part of more than one thing), *analysability* (can see how well it works or find cause of faults), *modifiability* (can be modified without impacting quality), *testability* (can define test criteria and run tests)

### Flexibility

*Adaptibility* (can be adapted to or moved to other environments) [inc. usage I think], *scalability* (handle growing **or shrinking** workloads), *installability* (install and uninstall), *replaceability* (replace something else for **the same purpose** in the **same environment**) [sounds like replacing **something else** e.g. PAS upgrades I guess]

### Safety

*Operational constraint* ('constrains its operation to within safe parameters' when encountering hazard), *risk identification* (can identify events or operations that risk life/property/environment), *fail safe* ('automatically place itself in a safe operating mode', or 'revert itself to safe condition'), *hazard warning* (provides warnings of risks or controls to react in time), *safe integration* (maintains sfety during / after integration with other things)

## AWS well-architected six pillars

The six pillars each have *design principles*, which are listed below:

### Operational excellence

[Link](https://docs.aws.amazon.com/pdfs/wellarchitected/latest/operational-excellence-pillar/wellarchitected-operational-excellence-pillar.pdf)

*Organise teams around business outcomes*, *implement observability for actionable insights*, *safely automate where possible*, *make frequent, small, reversible changes*, *refine operations procedures frequently*, *anticipate failure*, *learn from all operational events and metrics*, *use managed services*.

### Security

[Link](https://docs.aws.amazon.com/pdfs/wellarchitected/latest/security-pillar/wellarchitected-security-pillar.pdf)

*Implement a strong identity foundation*, *maintain traceability*, *apply security at all layers*, *automate security best practices*, *protect data in transit and at rest*, *keep people away from data*, *prepare for security events*.

### Reliability

[Link](https://docs.aws.amazon.com/pdfs/wellarchitected/latest/reliability-pillar/wellarchitected-reliability-pillar.pdf)

*Automatically recover from failure*, *test recovery procedures*, *scale horizontally to increase aggregate workload availability*, *stop guessing capacity*, *manage change through automation*.

### Performance efficiency

[Link](https://docs.aws.amazon.com/pdfs/wellarchitected/latest/performance-efficiency-pillar/wellarchitected-performance-efficiency-pillar.pdf)

*Democratize advanced technologies*, *go global in minutes*, *use serverless architectures*, *experiment more often*, *consider mechanical sympathy*.

### Cost optimization

[Link](https://docs.aws.amazon.com/pdfs/wellarchitected/latest/cost-optimization-pillar/wellarchitected-cost-optimization-pillar.pdf)

*Implement cloud financial management*, *adopt a consumption model*, *measure overall efficiency*, *stop spending money on undifferentiated heavy lifting*, *analyze and attribute expenditure*.

### Sustainability

[Link](https://docs.aws.amazon.com/pdfs/wellarchitected/latest/sustainability-pillar/wellarchitected-sustainability-pillar.pdf)

*Understand your impact*, *establish sustainability goals*, *maximise utilisation*, *anticipate and adopt new, more efficient hardware and software offerings*, *use managed services*, *reduce the downstream impact of your cloud workloads*.

## Arc42

On their website Arc42 use the following 9 categories:

- #efficient
- #flexible
- #maintainable
- #operable
- #reliable
- #safe
- #secure
- #suitable
- #usable

You can see more by filtering [this page](https://quality.arc42.org/qualities/) by the 'dimensions' at the top.

## A criticism

From [Wikipedia](https://en.wikipedia.org/wiki/Non-functional_requirement):

The term "non-functional requirement" is criticized for being seen as a misnomer diminishing of the importance of the set of requirements it covers. In its place, the term "cross-functional requirement" (CFR) has been proposed and adopted at ThoughtWorks.

## Resources

| Link      | Description |
| ----------- | ----------- |
| https://iso25000.com/index.php/en/iso-25000-standards/iso-25010 | ISO25010 |
| https://aws.amazon.com/architecture/well-architected | AWS six pillars |
| https://en.wikipedia.org/wiki/Non-functional_requirement | Non-functional requirements (Wikipedia) |

Summarise the various groupings you see here:
- https://iso25000.com/index.php/en/iso-25000-standards/iso-25010
- https://aws.amazon.com/architecture/well-architected/ - six pillars
- https://quality.arc42.org/articles/sei-quality-model - 10 properties