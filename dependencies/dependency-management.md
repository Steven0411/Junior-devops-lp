# Dependency Management

* Direct dependencies
  * Software that an application references directly
* Transitive (indirect) dependencies
  * Software that an application's direct dependencies funtionally require

* Dependencies can make it difficult to respond to vulnerabilities or other issues especially if caused by a component that your code doesn't directly reference
* There are many tools you can use to get insights into dependencies:
  * Open source insights - provides information about known vulnerabilities from known direct and indirect dependencies
  * Open source vulnerabilities database - a searchable db that aggregates vulnerabilities from other db's into one location
  * Scorecards - automated tool to identify risky software supply chain practices in your GitHub projects
  * Allstar - a GitHub app that monitors repo's for adherence to configured policies

## Including dependencies

* Install directly from public sources
  * convenient - don't need to maintain external dependencies
  * more prone to supply chain attacks since you don't control external dependencies
* Store copies of dependencies in your source repo
  * known as vendoring
  * more control over dependencies
  * increase size of project
  * must use same dependencies in each application or store copies of dependencies
  * upgrading can be more difficult
* Store dependencies in a private registry
  * allows for convenience public repo's with better control over dependencies
  * allows you to:
    * centralize artifacts and dependencies for all applications
    * config docker and language package clients to interact with it like a public repo
    * restrict access with IAM (identity and access management)
    * use remote repos to cache dependencies and scan for vulnerabilities
    * use virtual repos to group private repos behind a single endpoint

* Removing unused dependencies
  * more dependencies increases the risk of being compromised b a vulnerability in those dependencies so its best to use a few as needed
  * once the app is working locally copy the installed dependencies into the requirements file and deploy the app with those dependencies

## Version pinning

* restricting an application dependency to a specific version or version range.
* ensures application builds are reproducible but misses out on updates including security fixes, bug fixes and improvements
* can mitigate issues using automated dependency management tool that can monitor for new releases and update requirements files

## Verification

* Hash verification
  * compare the hash of an artifact witht he hash value calculated by the provider to confirm the integrity of the file
* Signature verification
  * the artifact repo, maintainers of the software or both can sign artifacts
  * there are services that allow maintainers to sign an artifact and for consumers to verify those signature

## Lock files

* Lock files are files with a list of dependencies with the versions specified
* created by installation tools and allow others to reproduce builds

