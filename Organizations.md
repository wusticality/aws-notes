# Organizations

AWS organizations are an account management service that enables you to consolidate multiple AWS accounts into an organization that you create and centrally manage.

There is one root account that can both invite or create accounts that become child accounts. There are also _organizational units_ (OUs), which are groups of accounts with access restricted by policies.

## Consolidated billing

Some advantages of this are:

* One bill per AWS account.
* Very easy to track charges and allocate costs.
* Volume pricing discount.

## Best practices

* Always enable MFA on the root account.
* Always use a strong password on the root account.
* Paying account should be used for billing only. Do not deploy resources into the paying account.
* Enable / disable AWS services using _service control policies_ (SCPs) either on OUs or on individual accounts.

