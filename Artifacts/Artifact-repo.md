# Artifact Repository

## What is an Artifact Repository?

* A software artifact repository (SAR) is a repository designed to govern the hosting, caching and versioninf of build outputs
* Can be implemeted into CI/CD pipelines to provide predictable delivery mechanisms
* Makes sure only tested binaries are deployed

## What is the purpose of an Artifact Repository?

* Store and manage artifacts produced during the software development lifecycle
  * Artifacts include: compiled code, libraries, dependencies, config files, documentation and build outputs.

## Benefits of an Artifact Repository

* Efficiency - Streamlined build and deployment processes reduce development time and effort
* Consistency - Version-controlled artifacts ensures all team members have access to the correct version of the artifacts to reduce the risk of errors or inconsistencies
* Seurity - Centralized storage and access controls enhance the security of sensitive artifacts
* Traceability - Detailed logs and version histories provide insights into the development process, aiding in debugging an compliance

## Types of Artifact Repository

* Local:
  * Hosted on the same machine/network as the dev environment
  * useful for storing and managing the lifecycle of in house developed artifacts
  * Limited outside access increases security - e.g. law enforcement

* Virtual:
  * aggregation of local and remote repos
  * Provides a view of all artifacts regardless of storage location
  * allows access to artifacts from multiple sources

* Remote:
  * Similar functionality to virtual
  * Used for proxying and caching dependencies from upstream public registries on the internet

## Best Practices

* Structuring artifacts in repositories:
  * Maintain organization and ease of access
  * Use clear and consistent naming conventions and organize artifacts into logical directories
    * JFrog recommends a 4-part naming structure:
      1. A Project, product or team name as primary identifier
      2. Technology, tool or package type used
      3. Maturity level such as developement, staging and release stages
      4. The Locator, the physical topology of your artifacts - where they're stored e.g. local
      * e.g. `<team>-<tech>-<maturity>-<locator>`

* Implementing build control and release management:
  * Helps ensure only approved and tested artifacts are used in production
  * minimize human error and maintain consistency

* Ensuring Artifact Security and access control
  * Scanning for potential vulnerabilities
  * Implement strong access control policies
  * Useencryption for sensitive data
  * regularly audit repo access and usage to mitigate security risks

## Integrate into CI/CD pipelines

* Artifact repositories store and manage the artifacts produced by build processes making them available for subsequent stages of development and distribution pipelines
* Can enhance the efficiency and reliability of CI/CD pipelines
* Provide a single source of truth for all team members

## Repository structure

* Refers to how repositories are organized, stored and accessed
* Without a proper structure repo's can become a dumping ground for artifacts

* Different repository structures include:
  * Mono-repository
  * Language-specific repositories
  * Team/service-specific repositories
  * Environment-specific repositories
  * Hybrid repository approach

* Benefits of the right repo:
  * Productivity
    * having a clear structure makes it easier for team members to find what they need
  * Security
    * a clear structure makes it easier to configure access controls of teams
  * Observability
    * clear structure makes it easier to log and debug specific changes
  * Impact on pipelines
    * can prevent:
      * failures due to ambiguous package resolution
      * pulling artifacts from the wrong state
      * inefficient caching


## Benefits of Cloud-native Artifact Repsitory

* Elasctic scalability
  * no need to provision hardware or manually plan capacity as team grows
* High availability
  * multi-region fault tolerant architecture ensures critical software artifacts are always accessible
* Global edge delivery
  * use edge caching to distribute artifacts closer to where they're needed ensuring faster access and minimal latency
* Zero maintenance
  * cloud provider handles server management, patches and upgrades
* Integrated Security and Compliance
  * often come with built-in vulnerability scanning, SBOM support and access controls