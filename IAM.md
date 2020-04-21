# IAM

IAM allows you to manage users and their level of access to the AWS console. At a high level, it enables the following:

* Centralized control of your AWS account.
* Shared access to your AWS account.
* Granular permissions.
* Identity federation (this means logging in with your Active Directory, Facebook, LinkedIn, etc. credentials).
* Multifactor authentication.
* Provides temporary access for users / devices and services where necessary.
* Allows you to setup your own password rotation policy.
* Integrates with many different AWS services.
* Supports PCI DSS compliance.

## Key terminology

### Users

End users such as people, employees of an organization, etc.

### Groups

A collection of users. Each user in the group will inherit the permissions of the group.

### Policies

Policies are made up of policy documents. They are in a JSON format and give permissions as to what a user / group / role can do.
