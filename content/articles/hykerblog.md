---
title: "Confidential Computing can ease the trust burden in Software Assurance."
date: 2022-11-11T14:37:57+01:00
featured_image: "/assets/img/factory.png"
tags: 
- "Confidential Computing"
- "Software Assurance"
- "CEST"
- "Intellectual Property (IP) Protection"
- "Security Analysis Tools"
---
  
The increased complexity of software systems has led to the situation where their security and reliability have become more necessary and more challenging. As a response, researchers and developers are constantly advancing software assurance techniques and tools that increase the assurance productivity. For example, one advancement in software assurance is the use of fuzz testing, which involves automatically generating random inputs to a program in order to find unexpected behavior. Fuzz testing has been shown to be effective at identifying security vulnerabilities that might have been missed by traditional manual testing methods. 

Despite constant advances in software security assurance, the demand for increased security is higher than ever. In today's digital world, the number of business-critical programs has skyrocketed. This coupled with the fact that software updates and patches are being released more frequently leads to a high burden for software vendors and assurance teams. 

State-of-the-art software development incorporates security analysis tools into the Continuous Integration/Continuous Deployment (CI/CD) process which should in principle ease the burden for assurance. However, the trustworthiness of the results of these tools are unverifiable, meaning that the trust is on the developers. But the increasing globalization of software supply chains means that we can no longer trust software providers automatically. As such, there is a higher demand for independent assurance of the complete software supply chain.  

Another factor driving demand for assurance is critical infrastructure. Much of our roads, trains, water, and 5G, are relying heavily on software. And nation states and regulators in general are increasingly tightening the demands for software trustworthiness. For example In India, the Indian Telecom Security Assurance Requirements requires that 5G Vendors  “... shall submit the source code to the Telecom Security Testing Laboratory”. This creates a need for trust in the other direction, since software vendors don’t want to increase the threat surface by exposing their software in all jurisdictions that require software access for assurance compliance due to the valuable Intellectual Property realized in software. 

Confidential Computing is an emerging technology that can solve this dilema. Confidential Computing allows for the computation of sensitive data in a secure environment, where the data cannot be accessed by unauthorized parties, even those with privileged access to the system “root administrators”. This technology can be used to produce trusted reports (attestable) on the source code that the assurance labs can use instead of viewing the actual source code. 

But how exactly does Confidential Computing produce trusted reports? Confidential Computing allows for confidential software analysis using a Trusted Execution Environment (TEE), a security technology that protects the execution of code and the confidentiality and integrity of data. The TEE ensures that the analysis is performed in a secure environment and that the results are trustworthy. This means that analysis tools used for software assurance can run inside a TEE thus protecting the Vendors sensitive Intellectual Property (IP). 

Therefore, Confidential Computing has been used to develop a prototype of Confidential Evaluation of Software Trustworthiness (CEST), which is the first step towards a safe and inevitable, more automated software supply chain assurance. CEST allows measuring the assurance level of software without exposing the company's sensitive IP. Having an assurance level simplifies the procurement process and regulatory compliance for software users. 

The CEST prototype is implemented as a SaaS platform, with software vendors having control over their sensitive IP in the form of source code, executables and CEST generated reports. This is made possible by the CEST platform’s architecture. 

For the CEST prototype, our team chose to use the TEE technique called Intel® SGX. This technology relies on hardware mode limiting a privileged user to access anything running inside an “enclave”, which is the name of a program running in the SGX TEE. The platform CEST is responsible for running analysis tools inside SGX. All parties can separately and in their own time review the tools and validate that they do not leak any data outside of their own runtime. When both Vendor and Evaluator agree that the tools are correct and relevant, they can use it in CEST. To be sure that the tools are correct they can build the tools themselves with the TEE to find out what the enclave will look like. This way they get a MRENCLAVE-value, which is in short a hash of the program running in the enclave. With this hash they can verify that an enclave running on another system is in fact running the same code.  

As mentioned above the CEST prototype is implemented as a SaaS solution to make it easy for interested parties to try it, but since no TEE is 100% unhackable Vendors can still be cautious about sending their IP to a SaaS solution, fortunately CEST could be run on vendor premises and the reports could be sent to evaluator. This will work since the reports are integrity protected by the hardware and can be attested by a remote party (Evaluator).  

The CEST solution is only limited by the robustness of the TEE and the accuracy, precision of the tools. Moreover, as TEE technology continues to advance and become more secure, the trustworthiness of CEST will only increase. Additionally, the recent surge in the popularity of AI may pave the way for more sophisticated and precise software analysis tools that can further enhance the accuracy and precision of CEST and close the loop, reducing the need for human-based inspections of evaluated software. 
