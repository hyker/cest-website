---
title: "The Assurance Tools Used by CEST"
date: 2022-11-11T10:59:01+01:00
featured_image: "/assets/img/assurance_tools.png"
tags: 
- "Security Analysis Tools"
- "CEST"
---
## Introduction:
In a [previous article](/articles/assurance-tools-choice/), we discussed the criteria for selecting the right assurance tools for your project. In this follow-up article, we'll show the specific tools that were chosen in the CEST Assurance Study to address software assurance in the telco and automotive industries. (Some of the tools where changed after the "hands-on examination"). By learning about these tools, you can gain insights into the features and capabilities you should look for when choosing assurance tools for your own projects. It should be noted that the list of tools are just the one we ported for our prototype and most if not all tools can be ported into the CEST architecture.

1. **Static Source Code Analyzers for C/C++**: The CEST Assurance Study selected four static source code analyzers for C/C++:
    * **CodeChecker**: Built on the LLVM/Clang Static Analyzer toolchain, CodeChecker includes several rulesets, such as a security ruleset, and can perform checks against the SEI CERT coding standard.
    * **Cppcheck**: Cppcheck provides a shallow analysis based on pattern matching at the token level, focusing on a low false positive rate. It detects various types of bugs, including security issues, and checks for MISRA, memory leaks, and more.
    * **FlawFinder**: FlawFinder examines C/C++ source code and reports possible security weaknesses (CWE) sorted by risk. It detects the use of risky C-functions that can lead to buffer overflows or race conditions.
2. **Checksec**: The study selected Checksec as the binary code scanner. Checksec is a bash script that checks the properties of executables, such as PIE, RELRO, PaX, Canaries, ASLR, and Fortify Source. Note that there are limited open source binary code scanners available, so only one was selected for the study.
3. **Dependency-check**: The CEST Assurance Study chose ScanCode for Software Component Analysis SCA. ScanCode scans source code or binaries to detect packages and dependencies, licenses, copyrights, and more. However after hands-on examination we changed to dependency-check which has other capabilities but we only use the binary code scanner functionality. The reason was that the output of dependency-check was more simmilar to a Software Bill of Material then ScanCode.

## Conclusion:
The CEST Assurance Study selected a range of open source tools to address various software assurance needs in the telco and automotive industries. By understanding the features and capabilities of these tools, you can make more informed decisions when selecting assurance tools for your own projects. Remember to consider the criteria we discussed in our [previous article](/articles/assurance-tools-choice/) to ensure that the tools you choose will effectively address the specific needs of your software and help maintain the highest level of quality and security.
