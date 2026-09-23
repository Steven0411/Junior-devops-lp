# Migration

* A migration is moving data/infrastructure from one place to another such as from on prem to the cloud

## Migration plan

* A migration plan defines the specific order, timing and approach for migrating workloads
* A readiness assessment measures your teams ability to execute the migration plan
* A readiness plan will:
  * evalutate team's skills with the new provider
    * if moving to azure check what skills your team has in azure and what training the need
  * engage external expertise when needed:
    * if your teams lacks cloud migration experience using external experts can validate your migration strategy, recommend appropriate tools, and help establish realistic timelines

## Data Migration Path

* How you move from its current location to the new location
* When moving data to Azure you should use:
  * expressroute when available
    * this gives you a private, dedicated connection to Azure thats faster and more secure
  * a vpn is expressroute isn't available
    * creates an encrypted tunnel pver the internet to azure
  * aure data box for large amounts of data
    * allows for offline migration because microsoft ships you a physical device you put your data on and you ship it back
  * public internet for less sensitive data
    * works when your data doesn't need encrption or much security

## Migration sequence

* reduce risk and build teams confidence by establishing a logical order for workload migration

1. Find dependencies
   * discover all dependencies and analyze dependency types and criticality
   * group workloads by dependency relationships
   * validate each group includes all necessary components for apps to operate
2. Address split environment operations
   * identify components that can't be move (for either technical or regulatory reasons)
   * minimize split-environemnt operation time
   * connect environments effectively using api gateways, message queues and data sychronization to create reliable connections
3. Prioritize workloads to migrate
   * start with simpler workloads to reduce risk
   * move non-production environments before production
   * schedule critical systems after ou demonstrate initial success
   * include complex workloads early to expose challenges 
4. Create a detailed migration schedule
   * set start and end dates for each migration
   * avoid scheduling migrations during critcal business periods
   * use project management tools to track progress
5. Choose the migration method for each workload
   * choose downtime migration for workloads that tolerate planned outages
   * choose near-zero downtime migration for critical workloads


## Define rollback plan

* enables teams to quickly reverse changes when a deployment fails or introduces risk

1. define failed deployment
2. automate rollback steps in CI/Cd pipelines
3. create workload-specific rollback instructions
4. test rollback procedures

## Engage stakeholders on migration plan

* Stakeholder approval validates that your migration plan meets business requirements and risk tolerance

1. document migration plan with business justification
2. present tested rollback procedures
3. validate against businedd constraints
4. obtain formal approval and rollback authority
5. define success criteria and review checkpoints