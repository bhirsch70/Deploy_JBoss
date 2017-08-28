# Deploy_JBoss
Deploy JBoss EAP
This Ansible Playbook includes a single play and role.  It installs JBoss EAP 7 in standalone mode

## Dependencies
RHEL 6 or 7

## Roles

* jboss-standalone

### Role Variables
* defaults - defines the http and https ports to open on with firewalld

### Role files
* jboss-as-standalone.sh - Standard JBoss bourne shell script to initialize a standalone configuration

### Role Handlers
* restart jboss
* restart iptables (used for RHEL 6 only)

### Role tasks
Performs the lion share of the role work including installing prerequisites, downloading JBoss, perform the installation, run the jboss initialization script, etc.

### Role templates
* iptables-save - iptables definition
* standalone.xml - JBoss standalone configuration
