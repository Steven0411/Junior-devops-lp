# Jenkins

* Jenkins is an open source platform that is used to implement Devops pipelines

## Benefits of cicd

* Reduced risk - frequently integrating changes reduces risk of sudden failure close to release
* Increase confidence - as new changes are introduced you can be sure they pass the test
* Better code quality - fast feedback loop of code deployment increase the quality of code that gets deployed
* Ready to ship - builds are automated and code is continuously deployed there is little delay in making code available
* Systematic versioning - builds are tracked with a build number making development traceable
* Code quality trend analysis - by tracking how long the pipeline takes to run and how many build failures happen over time you can track if your code is decreasing in quality
* Reduced cost - all these other benefits lead to a lower cost

## Jenkins features and architecture

* can be used across platforms
* Jenkins supports plugins which allows for further features in jenkins
* To use jenkins with a particular devops platform just install the necessary plugins and it should work seemlessly

* master-servant architecture
* master:
  * pulls code from source code repo
  * dispatch builds to the servants
  * monitor the health of the servant nodes
  * can execute build jobs directly
* servant:
  * java executable
  * runs on a remote machine
  * execute job and report back to master