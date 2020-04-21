# AWS Notes

A place to put notes while studying for my AWS certifications.

## Global Infrastructure

Know the difference between AWS regions, availability zones, and edge locations.

A _region_ is a physical location in the world which consists of two or more availability zones.

An _availability zone_ is one or more discrete data centers, each with redundant power, networking, and connectivity, housed in separate facilities.

_Edge locations_ are endpoints for AWS which are used for caching content. Typically this consists of CloudFront, Amazon's content delivery network (CDN).

## IAM

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

### Key terminology

#### Users

End users such as people, employees of an organization, etc.

#### Groups

A collection of users. Each user in the group will inherit the permissions of the group.

#### Policies

Policies are made up of policy documents. They are in a JSON format and give permissions as to what a user / group / role can do.

## S3

What exactly is S3?

* S3 is a safe place to store your files.
* The data is spread across multiple devices and facilities.
* It is object-based storage.
* Files can be from 0 bytes to 5 TB.
* There is unlimited storage.
* Files are stored in buckets.
* If you upload a file to S3 successfully, you will receive an HTTP 200 code.
* S3 is a universal namespace - names must be globally unique.
* Amazon guarantees 99.99% availability.
* Amazon guarantees 99.999999999% durability (11 9's).

### Objects
 
An object in S3 has a key, value (the data), a version id, and metadata.

There are also subresources like access control lists and torrents.

### Consistency

Read after write consistency for PUT's of new objects. If you write a new files and read it immediately afterwords, you will be able to view that data.

Eventual consistency for overwrite PUT's and DELETE's. If you update an _existing_ file or _delete_ a file and read it immediately, you may get the older version or you may not. Changes to objects can take time to propagate.

### Features
