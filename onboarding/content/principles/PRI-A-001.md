---
title: "PRI-A-001"
layout: principle-details
pageType: "Principle"
date: 2022-04-20T16:08:16+02:00
draft: true
id: "PRI-A-001"
category: Application
title: Technology independence
statement: |
  Applications are independent of specific technology choices and therefore can operate on a variety of technology platforms.
rationale: |
  Independence of applications from the underlying technology allows applications to be developed, upgraded, and operated in the most cost-effective and timely way. Otherwise technology, which is subject to continual obsolescence and vendor dependence, becomes the driver rather than the user requirements themselves.<br/>
  Realizing that every decision made with respect to IT makes us dependent on that technology, the intent of this principle is to ensure that Application Software is not dependent on specific hardware and operating systems software.
implications: |
  - Favour languages which provide a high degree of platform independence (e.g. use java instead of C#)<br/>
  - Deploy applications in containers and externalize configuration  to ensure portability across environments and platforms.<br/>
  - Optionality: Avoid vendor-specific extensions unless unavoidable. (e.g. on AWS use Aurora rather than DynamoDB)
categories: ["principles"]
---

