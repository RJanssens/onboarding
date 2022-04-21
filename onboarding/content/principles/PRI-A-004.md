---
date: 2022-04-20T16:08:16+02:00
draft: true
layout: principle-details
principleId: "PRI-A-004"
pageType: "Principle"
id: "PRI-A-004"
category: Application
title: Single concern
statement: |
  <a href="https://en.wikipedia.org/wiki/SOLID">SOLID</a> design principles include the principle of single responsibility, meaning that every class should have only one responsibility.<br/>
  The single concern principle is its equivalent in a cloud-native architecture, stating that a container should address a single problem.
rationale: |
  - Reuse: Container images which address a single concern are easier to reuse in other applications without modification and need for re-testing.<br/>
  - Independent scaling: Separating concerns across containers allows more fine-grained scaling of application components.
implications: |
   - Monolithic applications consisting of a front-end and back-end should be deployed independently as separate containers, rather than bundled.<br/>
   - If a microservice has multiple concerns which need to be deployed as a single entity, use constructs such as sidecars or init containers to maintain the single concern principle at the container-level.
categories: ["principles"]
---

