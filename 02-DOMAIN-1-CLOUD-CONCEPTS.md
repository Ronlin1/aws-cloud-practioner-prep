# Domain 1 — Cloud Concepts (24%)

This domain is conceptual. You should be able to recognize the correct cloud benefit, Well-Architected pillar, migration concept, CAF outcome, or economic principle from a scenario.

# 1. AWS Cloud value proposition

## Agility
Provision technology resources quickly instead of waiting for hardware procurement.

**Exam trigger:** “launch experiments quickly”, “provision in minutes”, “respond faster to business needs”.

## Elasticity
Capacity dynamically grows and shrinks with demand.

**Exam trigger:** “automatically adds capacity during spikes and removes it after demand falls”.

## Scalability
Ability to handle increased workload by adding/increasing resources.

- Vertical scaling = scale **up/down** one machine
- Horizontal scaling = scale **out/in** number of machines

Elasticity includes dynamic adjustment; scalability simply means the workload can grow.

## High availability
Design to minimize downtime through redundancy and multiple failure domains.

**Exam trigger:** “remain available if one server/AZ fails”.

## Fault tolerance
Continue operating despite component failure, with very little/no interruption.

## Disaster recovery
Restore/continue operations after a significant failure/disaster.

**Do not confuse:**
- Backup helps recovery.
- High availability aims to keep service running.
- DR addresses major disruption and restoration/continuity.

## Global reach
AWS Regions let companies deploy closer to users around the world without building their own data centers.

## Economies of scale
AWS aggregates usage across many customers and can achieve infrastructure efficiencies individual customers usually cannot.

## Stop guessing capacity
Cloud enables capacity adjustment rather than buying hardware years in advance.

---

# 2. Fixed costs vs variable costs

## Fixed/upfront costs
Typical on-premises examples:
- data-center space
- servers
- network equipment
- storage hardware
- UPS/generators
- cooling
- long procurement cycles

## Variable/consumption costs
Cloud resources can be consumed according to demand and pricing model.

**Exam phrase:** trade upfront/fixed expense for variable expense.

---

# 3. AWS Well-Architected Framework

Memorize all six pillars and the scenario each represents.

## Operational Excellence
Run, monitor, understand, and improve workloads and operational processes.

Triggers:
- operational procedures
- observability
- automation
- learning from operational events
- continuous improvement

## Security
Protect information, systems, and assets.

Triggers:
- IAM
- least privilege
- encryption
- detection
- data protection
- incident response

## Reliability
Workload performs correctly and recovers from failures.

Triggers:
- redundancy
- recovery
- distributed systems
- Multi-AZ
- automatic recovery

## Performance Efficiency
Use computing resources efficiently as requirements and technologies evolve.

Triggers:
- choose appropriate resource type
- serverless/managed technology where appropriate
- monitor performance
- adapt to demand and new technologies

## Cost Optimization
Deliver required business value while avoiding unnecessary cost.

Triggers:
- rightsizing
- remove idle resources
- choose proper pricing model
- measure/attribute spend

## Sustainability
Minimize environmental impact through efficient resource usage.

Triggers:
- maximize utilization
- minimize unnecessary resources
- use efficient managed/cloud technologies

### Fast differentiation
- “operate better” -> Operational Excellence
- “protect” -> Security
- “recover/continue” -> Reliability
- “perform efficiently” -> Performance Efficiency
- “spend efficiently” -> Cost Optimization
- “environment/resource footprint” -> Sustainability

---

# 4. AWS Cloud Adoption Framework (AWS CAF)

CAF helps organizations structure cloud transformation/readiness.

Memorize the six perspectives:

## Business
Ensure cloud investments produce business outcomes.

Keywords: strategy, business value, outcomes, product/portfolio, revenue.

## People
Skills, culture, leadership, workforce, organizational change.

Keywords: training, skills, culture, organization design.

## Governance
Coordinate initiatives while maximizing benefits and controlling risk.

Keywords: risk, program/project management, financial management, governance.

## Platform
Build scalable cloud/hybrid platforms and workloads.

Keywords: architecture, engineering, infrastructure, delivery platform.

## Security
Confidentiality, integrity, availability, IAM, threat/vulnerability/data protection.

## Operations
Operate cloud services at levels that meet business needs.

Keywords: observability, incident/problem management, patching, availability/continuity.

## CAF outcome examples explicitly worth recognizing
The CLF-C02 task statement gives examples of cloud-adoption outcomes such as:
- **reduced business risk**
- **improved environmental, social and governance (ESG) performance**
- **increased revenue**
- **increased operational efficiency**

These are examples of the business value/outcomes of cloud transformation, not additional CAF perspectives.

### CAF vs Well-Architected
- **CAF** = organizational cloud transformation/readiness.
- **Well-Architected** = evaluate/design/operate workloads against cloud best practices.

Do not merge these two frameworks.

---

# 5. Migration concepts

Know WHY companies migrate:
- agility
- elasticity
- global reach
- reduce data-center footprint
- modernization
- operational efficiency
- reduce business risk
- improve scalability/availability
- potentially improve ESG/sustainability outcomes
- support new revenue/business opportunities

## Common migration strategies

### Rehost
“Lift and shift.” Move with minimal application changes.

### Replatform
Move while making limited optimizations without fully redesigning.

### Refactor / Re-architect
Redesign to use cloud-native architectures/services.

### Repurchase
Move to a different product/SaaS solution.

### Retire
Decommission workload no longer needed.

### Retain
Keep where it is for now.

### Relocate
Move existing infrastructure/workloads with minimal redesign where supported.

## Key migration-service recognition
- Application Discovery Service -> discover inventory/dependencies
- Application Migration Service -> server/application migration
- DMS -> migrate database data
- SCT -> convert database schemas
- Migration Hub -> central migration tracking
- Migration Evaluator -> migration business case/cost assessment
- Snow Family -> physical/offline transfer for large data sets when network transfer is impractical

---

# 6. Cloud economics

## Rightsizing
Match resource size/type to actual workload requirement.

Bad:
- paying for a 64-vCPU instance used at 5%.

Good:
- move to appropriate capacity based on utilization.

AWS Compute Optimizer can provide recommendations for supported resources.

## Automation
Automation can:
- reduce manual work
- increase consistency
- speed provisioning
- reduce operational errors
- help scale operations

## BYOL vs license included
- BYOL = Bring Your Own License, if vendor/licensing rules allow.
- License included = AWS/service price includes relevant software licensing under that model.

## On-premises costs AWS questions may imply
Remember hidden costs beyond server purchase:
- facilities/real estate
- hardware replacement
- electricity
- cooling
- security
- networking
- maintenance contracts
- backup infrastructure
- system administration
- over-provisioning

---

# Domain 1 instant-check questions

You should answer these immediately:

1. Automatic grow/shrink? -> **Elasticity**
2. More servers? -> **Horizontal scaling**
3. Bigger server? -> **Vertical scaling**
4. Multiple AZs to survive failure? -> **High availability / Reliability**
5. Launch resources rapidly? -> **Agility**
6. Large provider gets efficiencies from aggregate demand? -> **Economies of scale**
7. Organizational cloud transformation framework? -> **AWS CAF**
8. Six workload-design pillars? -> **Well-Architected Framework**
9. Correctly size resources to utilization? -> **Rightsizing**
10. Lift and shift? -> **Rehost**
11. Redesign app to cloud-native? -> **Refactor/re-architect**
12. Massive offline migration with limited bandwidth? -> **Snow Family**
13. CAF business outcomes? -> **reduced risk / ESG improvement / revenue / operational efficiency**

# Official references

- Domain 1: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html
- Well-Architected: https://docs.aws.amazon.com/wellarchitected/latest/framework/the-pillars-of-the-framework.html
- AWS CAF: https://aws.amazon.com/cloud-adoption-framework/
