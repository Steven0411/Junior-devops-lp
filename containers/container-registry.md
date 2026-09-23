# Container registry

* A repo or collection of repo's used to store and access container images
* Support container base app development
* Save time in creation and delivery of cloud-native applications

## Container images and registries

* A container image include files and components to make an application
* Containers are lightweight packages of software that run on linux os
* Container registries act as a place for developers to store container images and share them
* Containers isolate application processes, runtime files, and os dependencies from the rest of the system

## Public vs Private Registries

* Public:
  * commonly used by individuals or small teams
  * can have security issues in larger organizations like patching, privacy and access control
* Private:
  * often cone with advanced security features and techinacal support
  * things to consider with private registries:
    * support for multiple authentication systems
    * role-basedd acess control management for local images
    * vulnerability scanning capabilities for enhanced security and configuration
    * ability to record use in auditable logs so that activity can be traced to a single user
    * optimized for automation