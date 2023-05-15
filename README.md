# AAA-Scrum (Analysis, Automation, and Acceptance)

* [Introduction](#introduction)
* [Diagram](#diagram)  
* [Phases](#phases)  
  * [Analysis](#analysis)
  * [Automation](#automation)
  * [Acceptance](#acceptance)


## Introduction
Here we introduce AAA-Scrum – Triple A, an acronym for Analysis, Automation, and Acceptance – seeks to plugin relevant security components broken into three distinct security phases which overlap the existing scrum framework. Furthermore, the model attempts to learn from the success of DevOps and DevSecOps in modern software development and incorporate it into our model in the hope that it helps reduce overhead or change team dynamics.

We find that security practices can be mapped to the stages of analysis, automation, and acceptance. Within each of these phases exists contextually important security components that we expect can be implemented by either current scrum teams or in consultation of IT / security / operations teams. That said, it is important to note that the use of security expertise is not required for every security phase in AAA-Scrum and can be considered more as part-time supervisor role that defines and accepts but does not implement.

## Diagram 
![image](https://raw.githubusercontent.com/bcdunbar/aaa-scrum/main/aaa-scrum.png)


## Phases

Next, we take a closer look at each security phase and its relevant components.

### Analysis 
The initial security phase overlaps with the product backlog, spring planning, and sprint backlog aspects of the scrum framework. Furthermore, we identified three security components within the analysis phase. The first two, compliance and policy & frameworks, are defined at the creation of the product backlog through the involvement of the security expert within the business who oversees such responsibilities. The desired outcome of these components during analysis is to ensure that product items are mapped to relevant policies or frameworks. However, this part of analysis is preliminary since the product items have not yet been included into the sprint. The third component, Baseline Acceptance, is considered during the sprint backlog and ideally would involve the security expertise working closely with lead developer to ensure an understanding of acceptable risk given the current software composition and product item in relation to the previously defined policies and frameworks the business aims to comply with. To ensure transparency, all policies, frameworks, and security acceptance criteria are to be documented (such as a Jira user story) to ensure developers have visibility.

### Automation
An essential part to maintaining the existing agility of scrum, is automation. Importantly, it enables developers to perform security practices without security experts needing to be actively present. The automation phase roughly maps to the implementation aspect of scrum – including daily scrum standups and iteration. Here, we introduce security components which perform SAST (Static Application Security Testing) and DAST (Dynamic Application Security Testing), as well as dependency vulnerability scanning, on each code change request, which is achieved with continuous integration (CI) tools such as Github Actions or CircleCI and code scanning software providers. Developers can get immediate feedback from these tests via test report outputs from the CI process and then make changes accordingly. Furthermore, many security code scanning providers link issues found in testing to their platforms education resources to help educate developers on the associated vulnerabilities. Finally, test results are integrated into the version-controlled repository and thus accessible to code reviewers and security experts. Additionally, due to the continuous integration these outputs are in sync with a developer’s daily work and consequently can be discussed by team members during daily scrum – bringing security practices into daily scrums.

### Acceptance
The final phase captures the verification and definition of done aspects of the scrum framework. Here, we introduce 1 compulsory security component and 1 conditional security component. Namely, the compulsory component is the inclusion of the security expert who in the analysis phase defined and documented the relevant policies and frameworks; and established the acceptable risk the business would be willing to accept. To achieve this, the security expert reviews the requested code changes and the outputs from the automation phase. The conditional security component – penetration testing, is dependent on resources available within the team or if the team needs to seek external resources. Furthermore, it is considered conditional as not all code changes will require penetration testing. However, where penetration testing may be applicable it ought to be defined during the analysis phase in the baseline acceptance security component.
