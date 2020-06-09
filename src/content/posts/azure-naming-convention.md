+++
author = "Rick Neeft"
title = "Azure Naming Convention"
date = "2020-05-24"
description = "Within Azure, every resource must have a unique name. It can be helpful to create a naming convention for your Azure resources."
tags = [
    "azure",
    "naming",
    "guidelines"
]
+++

# Naming conventions
Within Azure, every resource must have a unique name. It can be helpful to create a naming convention for your Azure resources. This will prevent naming issues and will help you finding your resources quicker. The following convention below have proved to be very helpful for my projects.

## Default naming convention

**DO** apply the following convention while naming resources:

 AAA-BBB-CCC-DDD-EEE (ex: CHR-MTA-ASP-DEV-WE)

| Part | Abbreviation For | Example
| ---- | -----------| ---
| AAA  | Company | CHR (Chroomsoft)
| BBB  | Product | MTA (My Template Abbreviation)
| CCC  | [Resource](#resources) | ASP (App Service Plan)
| DDD  | [Stage](#stages) | DEV, PRD
| EEE  | [Location](#locations) | WE (West Europe)

> *Some Azure resources prevents the use of the above convention. However, try to stay close to this convention. For example: Azure Storage Account, apply the following convention: aaabbbcccdddeee*

**AVOID** small letters in the abbreviation.

**CONSIDER** three letter abbreviations for each part of the template.

**DO** use the abbreviations as specified in the tables below.

**DO NOT** apply this convention to 'DNS Zones' since they are named after the domain name and are by definition unique. 

### Resources
Some of the resources are noted down below:

| Resource           | Abbreviation 
| ------------------ | ---
|App Service Plan|ASP
|Application Insights|AI
|Azure Function App|AFA
|CDN Endpoint|CEN
|CDN Profile|CDN
|DNS Zone | ---
|Key Vault|KV
|Resource Group|RG
|Shared Dashboard|SDB
|Storage Account|sa
|User managed identity|UMI
|Web site|WEB

### Stages
| Abbreviation | Stage | Description
| --- | --- | ---
| RND | Research And Development | Used for manually created resources in Azure. Most of them are try outs, click and play or quick demo's. Resources have a short life span. 
| POC | Proof Of Concept | Stage for a bit more serious resources, still a lot of try outs but most of the resources are created with (manually executed) ARM templates.
| DEV | Development | First stage featuring fully automated deployed resources with ARM templates (or Azure CLI commands) inside an Azure DevOps pipeline. Used for early development, not all changes to resources are fully yet, but must be automated ASAP.
| TST/ACC | Test/Acceptance | Stage dedicated for testing purposes, manual changes are strongly discouraged.
| PRD | Production | Speaks for itself. Manual changes are not allowed (unless for Priority bugsfixes or changes not supported by the Azure framework, like applying a SSL certificate for CDN Endpoints)

### Locations

| Location      | Abbreviation |
| --- | ---
|Australia Central|AC
|Australia Central 2|ACT
|Australia East|AE
|Australia South East|ASE
|Brazil South|BS
|Canada Central|CC
|Canada East|CE
|Central India|CI
|Central Us|CU
|East Asia|EA
|East Us|EU
|East Us 2|EUT
|France South|FS
|Japan East|JE
|Japan West|JW
|Korea Central|KC
|Korea South|KS
|North Central Us|NCU
|North Europe|NE
|South Africa North|SAN
|South Africa West|SAW
|South Central Us|SCU
|South East Asia|SEA
|South India|SI
|Uk South|UKS
|Uk West|UKW
|West Central Us|WCU
|West Europe|WE
|West India|WI
|West Us|WU
|West Us 2|WUT

## Conclusion
Which conventions are you currently using or are you going to start a naming convention now? Let me know what you think in the comments below. 