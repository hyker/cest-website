---
title: "Introducing a New Trust Model for Software Assurance: The CEST Platform"
date: 2022-11-11T10:59:01+01:00
featured_image: "/assets/img/trust_model.png"
tags: 
- "Trust Model"
- "CEST"
---
## Introduction:
Trust is a crucial factor in software assurance, particularly when multiple parties are involved. In this article, we propose a new trust model for software assurance that aims to minimize the required trust between different actors by introducing an intermediary that everyone trusts: the CEST platform. We'll discuss the rationale behind this trust model, how trusted computing plays a role, and the advantages of a location-agnostic approach.

### The Trust Model: CEST Platform
The CEST platform is a confidential computing solution based on state-of-the-art hardware and open-source software. By allowing all actors to scrutinize the CEST platform and understand its behavior, trust is established. This trust model ensures that:

Vendors can be certain that their software or sensitive information does not leak out of the CEST.
Evaluators can use all tools supported by the CEST to analyze the software and know that the output of the tools is authentic.
Customers can trust that the results of the analysis cannot be modified arbitrarily outside the CEST.
The goal is to minimize the required trust between the original actors.

### Trusted Computing
The trust model relies on all actors trusting the hardware and the software executing on that hardware. One way to achieve trust in the software is to allow all actors to inspect and audit the open-source code running on the hardware. It is essential to trust the hardware itself and its manufacturer, but not necessarily the CEST operator.

### Location Agnostic
The location of the platform and the exact entity taking the role of the CEST operator have no direct impact on the trust relationships and the guarantees the CEST provides, as long as the hardware and code are trusted. Possible locations include vendor premises, evaluator premises, or a public cloud aaS.

The platform's location can help build trust in the platform itself. For instance, if the CEST is hosted in the cloud, the vendor can more easily trust that the trusted enclaves hosted by the CEST have not been tampered with. Even if the vendor refuses to send the software outside their premises, the CEST can be run locally and used by the vendor to guarantee to the evaluator that agreed tests have been performed and the resulting report has not been modified.

## Conclusion:
The CEST trust model introduces a new approach to software assurance by minimizing the required trust between different actors and focusing on a trusted, transparent intermediary. By leveraging trusted computing and a location-agnostic approach, this trust model can help improve the overall software assurance process, ensuring the security and reliability of software solutions across industries.
