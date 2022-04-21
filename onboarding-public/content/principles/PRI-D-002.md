---
id: "PRI-D-002"
category: Data
title: API First
statement: |
  Design an API so that it has <b>consistency</b>, as well as <b>adaptability</b>, regardless of the type of project. The API first principle is as follows:<br/>

  - The API is the first user interface of an application.<br/>
  - The API comes first and then the implementation.<br/>
  - The API is described.<br/>
  - The API is contracted between the provider and the consumer.<br/>
rationale: |
  - Permit parallel work by development teams: As soon as the contract is established, teams can work on implementation.<br/>
  - Reduce time to market: API specifications permit auto-generation of clients and servers, stubbing, auto-documentation etc.<br/>
  - Reduced risk of failure: The process of designing an API up-front results in a shared understanding of the problem domain and better alignment between stakeholders since all parties work on defining the contract.<br/>
implications: |
  - Teams should design & publish an API conforming to organizational standards ahead of implementation.<br/>
  - System components need to be appropriately sliced by encapsulating the business logic and rules in domain objects using e.g. domain-driven design techniques.
categories: ["principles"]
layout: principle-details
pageType: "Principle"
date: 2022-04-20T16:23:47+02:00
draft: true
---

