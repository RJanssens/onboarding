---
title: "Update management"
date: 2022-04-19T11:09:59+02:00
draft: true
---

## Introduction

It's important to ensure that your application runs on a current environment. When you deliver an application, you potentially provide an **operating system, runtime, frameworks and libraries**. 

Over time, software vulnerabilities & bugs are discovered and fixed these products. Malicious actors can take advantage of published patches by writing code to target the corrected vulnerabilities. For this reason, it is important to patch early and patch often.
 


## Why not explicitly specify which versions to use?

Rather than providing an exhaustive list of authorized versions for all products in use, we apply the principle of **decentralized governance**. Project teams are responsible for ensuring that the products used by their applications are up to date. 

Managing a central index of versions for all products in use across the organisation would not be feasible given the wide scope of products in use. Such a list would also be cumbersome to maintain over time as new releases appear. 

{{< notice tip >}}
General principle: Use software versions under active vendor support.
{{< /notice >}}

## Validing software for vulnerabilities

If you are using automation, use **[OWASP Dependency Check](https://owasp.org/www-project-dependency-check/)** and **[SonarQube](https://ecoapp.internal.economie.fgov.be/sonar)** to validate whether your deliverables are prone to vulnerabilities. If CVEs are detected, the description of the CVE also lists versions which correct to security flaw (if available). 

Update management is an ongoing activity which does not end with delivery in production.

{{< notice warning >}}
While the application is live, the project team is responsible for ensuring that application runtime, frameworks & libraries are updated in time. 
{{< /notice >}}


## Recommendations by platform

### Containerized applications

- When using container images, use a local image (not Docker Hub). Local images are guaranteed to come from official sources.
- Use the latest tag for each image product-version combination.

### Spring Boot / Liberty Profile

Use:
- AdoptOpenJDK runtime (Temurin/Semeru), *not* Oracle Runtime
- HotSpot and OpenJ9 are acceptable.
- If possible, use an LTS release which is under vendor-support (8/11/17)
- If needed, use the latest non-LTS release (non-LTS releases expire after 6 months)


Cf. https://adoptopenjdk.net/support.html for overview  

### WebSphere Application Server

Use:
- The Java runtime that comes with the application server. 

### Angular

Use:
- The Angular version under active support: https://angular.io/guide/releases 

### Node

Use:
- The current or LTS release in active or maintenance state: https://nodejs.org/en/about/releases 



