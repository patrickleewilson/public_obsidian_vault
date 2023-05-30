# What is a container?
- A way to package an application with all the necessary dependencies and configuration.
- Containers are easily shared and moved around.
- Makes development and deployment more efficient.


# Where do containers live?
- Containers reside in Container Repositories.
- Many companies have their own private container repositories.
- Docker has its own public container repository.


# How do containers improve the development process?

# Before containers were available
- ![[Pasted image 20221030191442.png]]
-  Deployment pains/setup pains/OS requirement pains/potential error
- The more complex the application, the more tedious it can be to setup a new environment for it.


# After containers became available
![[Pasted image 20221030191841.png]]
- A much more streamlined process, all configurations and packages/dependencies are there
- Much less room for error, no OS shenanigans, all same version depending on the container image version.
- Easy install.
- Run two different versions of the same application at the same time with no conflicts.


# How do containers improve the deployment process?

# Before containers were available
![[Pasted image 20221030192359.png]]
- Artifacts created by devs are handed off to an external team to deploy to environments.
- There is a hefty amount of room for error in this process due to potential version conflicts of dependencies (think assembly binds required, nuget package updates not being consumed by external apps, etc) and the deployment team potentially misunderstanding what to deploy.

# After containers became available
![[Pasted image 20221030192635.png]]
- One goal in tandem to package application into a container
- No configuration needed on specific servers for specific environments, except Docker RunTime


