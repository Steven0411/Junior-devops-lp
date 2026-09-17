# Azure Artifacts 

## Best Practices

### Core guidance

* Use one feed in each client config and enable upstream sources when you need public registries or additional internal sources
  * A feed is an organizational construct that can host multiple package types.
* Treat feed views as release channels - publish new versions to one channel and then promote them to others when they're ready for broader use
* Configure feed permissions
* Enable retention policies to prevent older versions clogging up feeds

### For Package Publishers

* User a single feed per repository
  * This helps reduce conflict and simplify package management
* Automatically publish newly created packages
  * Helps ensure the latest versions are available to your team or target consumers
* Enable retention policies
  * Automatically removes older versions while keeping a specified number of new versions to prevent consuming too much storage 
* Use feed views to release packages
  * Lets you share a subset of package versions with consumers
* Ensure proper access permissions
  * If releasing to the public make sure views such as release and prerelease have appropriate visibility

### For Package Consumers

* Use one feed in your client config
  * keeps files simpler and reduces the chance of unexpected package resolution results
* Use upstream sources for external packages
  * Gives your team a consitent way to restore both internal and external dependencies throught the same feed
* Order upstream sources intentionally 
  * The feed checks upstream sources sequentially so the order of them matters
* Use feed view to controll what consumers see:
  * Use views to share only package versions that are intended for a given audience
* Use the feed locator for cross-organization sources in the same tenant:
  * If sources are in the same Microsoft Entra tenant but aren't part of your organization, use the feed locator. 
    * The syntax is `azure-feed://<organization>/<projectName>/<feed>@<view>.`