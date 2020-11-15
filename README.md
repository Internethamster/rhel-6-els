Role Name
=========

This role allows the user to convert the root volume of an on-demand RHEL 6 instance to a Marketplace instance of the On-demand RHEL 6 with Extended Lifecycle Support. 

As of now, the role supportes converting instances built from AMIs that are backed by official RHEL 6 AMIs provided by Red Hat, so the instance from which the conversion must have the following: 
 - a valid RunInstance:0010 code identifying that it is derivative of the official AMI. 
 - access to the external network for access to the RHEL 6 ELS updates.
 
There are many ways to approach making a move from one instance to another. The instances built on the 
 

Requirements
------------

Access to the external Amazon EC2 network to connect

Role Variables
--------------

#### `aws_inject.aws_access_key`
    The Account Access key default is `null`. If ithis is not set then
    the value of the *AWS_ACCESS_KEY_ID*, *AWS_ACCESS_KEY* or
    *EC2_ACCESS_KEY* environment variable is used. See
    [configuring the aws cli](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html "Configuring the AWS CLI") documentation for additional details on configuring
    credentials (Aliases: ec2_access_key, access_key)[Default: (null)]

#### `aws_inject.aws_secret_key` 
    The AWS secret key default is `null`. If not set then the value of
    the *AWS_SECRET_ACCESS_KEY*, *AWS_SECRET_KEY*, or EC2_SECRET_KEY
    environment variable is used. See [configuring the aws
    cli](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html
    "Configuring the AWS CLI") documentation for additional details on
    configuring credentials (Aliases: ec2_secret_key,
    secret_key)[Default: (null)] type: str


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
