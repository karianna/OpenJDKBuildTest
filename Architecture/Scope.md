#Scope

It is envisaged that the ecosystem would enable a user of the system to make requests like:

"Build OpenJDK from a repository point with checksum X, with supplied patch P applied, on environments E1, ..., En - and tell me what the result of the build was."

This implies some technical infrastructure
* Servers for managing
  - Collections of patches
  - Build jobs which users want executed
  - A review system of same
  - Some sort of registry or discovery service for build servers to announce their existence, willingness to perform work, and capabilities.

* The system should support BOTH build servers which are capable of making binaries available on a successful build, AND servers which will only report results

* The system should support build servers which act as gateways to groups of servers which do not wish to directly connect to the discovery / registry service. 

* A protocol for describing jobs, handing them off to build servers and reporting results is implied.

* All patches and jobs will have to be manually reviewed to begin with. 
  - Patches (eg to Makefiles) could contain malicious code - we don't want to create a botnet.

Overall, two initial phases for the project are imagined:

* Collect the IP contributions from participating members. 
  - Sort through them
  - See how they fit together
  - Identify gaps.

* Build out the needed components (patch distribution protocol, etc). 
  - Wherever possible, this should be done using existing technology - i.e. is it possible to do this by enhancing Jenkins rather than building from scratch.

The project would contain scripts, configuration and other helper utilities in order to allow Contributors to set-up their own build-farms for OpenJDK builds. Within scope would be such items as Vagrant scripts, Jenkins/Hudson scripts, Mercurial scripts etc. Out of scope would be actual OpenJDK source code (scripts would retrieve this) or source/binary installations of tools such as Jenkins/Hudson.

Overall, two initial phases for the project are imagined:

* Collect the IP contributions from participating members. Sort through them, see how they fit together, and identify gaps.

* Build out the needed components (patch distribution protocol, etc). Wherever possible, this should be done using existing technology - i.e. is it possible to do this by enhancing Jenkins rather than building from scratch.
