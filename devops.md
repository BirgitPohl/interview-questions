# Devops

# AWS

## SHORT:
Explain in SQS a deadletter queue to me
What is ECS and how is it used with ECR?
Why does a S3 bucket needs to have a globally unique name?
What is a VPC? What are IAM and (N)ACLs in this regard?


## LONG AWS:
Given the situation that we need to rapidly need to build an application to handle the following:
A partly Germany / partly US based customer of ours runs several eCommerce sites in AWS which should all be connected to a single API and persisting sensitive data. The API needs to be written. The current rates are in total 20000 visitors per day per site and 5000 req/s – however since the customer aims to enlarge their company it is quite likely that this needs to scale in the next month and years.

The data should be able to be easily taken and to be analyzed and displayed to the customer. What tooling would you use for that?

Also the customer complains about performance of the website. Especially the initial loading time is in some areas in the US quite terrible.
What would you advise him to do?

How should the initial overall architecture look like from your pov?

# Azure

What is a logic app?
What is a timer trigger in Azure functions?
What is a data factory and what are pipelines here?

# GCP

When would you use Cloud functions and when App Engine?
When would you use Firebase over GCP?


General to Cloud Platfoms
Explain to me event streaming in cloud platforms
What makes serverless functions so powerful?

Last question: How much should you charge to wash all the windows in Munich?
Or Techie: How much RAM is in the Frankfurt AWS data centre a and b