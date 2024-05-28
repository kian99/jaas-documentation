# Description

The following document describes missing JAAS documentation as well as any docs that need to be modernized.

## Missing Docs
- ~~Deploy JAAS tutorial~~ (completed in deploy_jimm_microk8s.rst)
- JAAS architecture
- ~~Explain the difference between Juju, JAAS and jimmctl CLI tools.~~ (completed in cli_tools.rst)
- Auth doc explaining JIMM's authentication and authorization.
- How to enable/deploy/use the dashboard.
- JAAS Limitations - potentially (As an example, cross-controller relations don't work with JAAS currently)
- Relating JIMM and COS stack - general observability.
- What versions of Juju controllers and CLI does JIMM support.
- Managing access rights via jimmctl 
- How to migrate existing Juju controllers and models to JAAS.
- How to bootstrap JAAS with an admin user and create user permissions.
- How to migrate models between Juju controllers in JAAS.
- Documentation on the jaas cli extension snap.

## Docs requiring changes
- how-to/add_controller (possibly merge add_controller_no_dns into the original)
- how-to/deploy_jimm_k8s
- how-to/deploy_jimm (the machine charm is not currently on par with the k8s charm, this document could be removed until the machine charm is updated and ready for production use)
- how-to/route53 ensure this document is still up to date.
- tutorial/jaas_basics