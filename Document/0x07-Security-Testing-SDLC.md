# Appendix

## Security Testing in the Software Development Lifecycle

The history of software development is not that old after all, and it is easy to see that, rapidly, teams have stopped developing programs without any framework: we have all experienced the fact that, as the number of lines of code grow, a minimal set of rules are needed in order to keep work under control, meet deadlines, quality and budgets. 

In the past, the most widely adopted methodologies were from the "Waterfall" family: development was done from a starting point to a final one, going through several steps, each of them happening one after the other in a predefined sequence. In case something was wrong during a given phase and something had to be changed in a former phase, it was possible to go back only one step backward. This was a serious drawback of Waterfall methodologies. Even if they had strong positive points (bring structure, clarify where to put effort, clear and easy to understand, ...), they also had negative ones (creation of silos, slow, specialized teams, ...). 

As time was passing and software development was maturing, also competition was getting stronger and stronger, and a need to react faster to market changes while creating software products with smaller budgets rose. The idea of having fewer structure with smaller teams collaborating together, breaking silos through the organization from marketing to production, became popular. The "Agile" concept was created (well known examples of Agile implementations are Scrum, XP and RAD), which was enabling more autonomous teams to work together in a faster manner.

Originally, security was not part of software development. It was seen as an afterthought, and was performed by Operation teams at the network level: those teams had to find ways to compensate for poor security in software programs! However, while this was possible when software programs were located inside a perimeter, the concept became obsolete as new ways to consume software emerged with Web and Mobile technologies. Nowadays, security has to be baked **inside** software as it is often very hard in this new paradigm to compensate for existing vulnerabilities.

The way to incorporate security during software development is to put in place a SDLC (Software Development Life Cycle). A SDLC does not depend on any methodology, and it is possible incorporate one in Waterfall or Agile: no excuse not to use one!
This chapter will focus on Agile and SDLC, in particular on the DevOps world. The reader will find below details on state-of-the-art ways to develop and deliver secure software in a fast-paced and collaborative manner that promotes autonomy and automation.

### Agile and DevOps

#### DevOps

DevOps refers to practices that focus on a close collaboration between all stakeholders involved in delivering software. DevOps is the logical evolution of Agile in that it enables software to be released to users as rapidly as possible. Besides the collaboration aspect, to a large extent, this is facilitated through heavy automation of the build, test and release process of software and infrastructure changes. This automation is embodied in the deployment pipeline.

##### Todo: Add deployment pipeline overview and description specific for mobile apps.

The term DevOps might be mistaken for only expressing collaboration between development and operations teams, however, as Gene Kim, a DevOps thought leader, puts it: “At first blush, it seems as though the problems are just between dev and ops," he says, "but test is in there, and you have information security objectives, and the need to protect systems and data. These are top-level concerns of management, and they have become part of the DevOps picture."

In other words, when you hear "DevOps" today, you should probably be thinking DevOpsQATestInfoSec.” (Source: https://techbeacon.com/evolution-devops-new-thinking-gene-kim)

Security is just as important for the business success as the overall quality, performance and usability of an application. As development cycles are shortened and deployment frequencies increased it is elementary to ensure that quality and security is built in from the very beginning.

From the human aspect, this is achieved by creating cross functional teams that work together on achieving business outcomes. This section is going to focus on the interaction with and integration of security into the development life-cycle, from the inception of requirements, all the way until the value of the change is made available to users.

### Approach

Start by doing risk assessment
-> Define data classification (What is considered sensitive data in your org)
-> Set the according ASVS level
-> Integrate requirements into ALM
-> Threat model for design
-> Provide secure coding guidelines to the devs
-> Provide test cases for qa folks
-> Automate as many security tests as possible in the deployment pipeline
-> Perform exploratory security testing
-> Close feedback loop to dev team

### General Considerations

* Release time for apple store
* Why are black listed, and how to avoid it.
* Common gotchas: Ensure that the app is always fully removed and re-installed. Otherwise there might be issues that are hard to re-produce.
*

### SDLC Overview

#### General description of SDLC

Whatever the development methodology that is being used, a SDLC always follows the same process:
* at the beginning of a project or a development cycle, at the same time when functional requirements are gathered, **Security Requirements** are listed and clarified. As use cases are built, **Abuse Cases** are added. Also, **Security Risks** are analysed, as other risks of the project (financial, marketing, industrial, ...). Teams (including development teams) may be trained on security if needed (Secure Coding, ...);
* then, as architecture and design are ongoing, a foundational artefact must be performed: **Threat Modeling**. Based on it, **Security Architecture** is defined (both on the software and hardware sides). **Secure Coding rules** are established and the list of **Security tools** that will be used is created. Also, the strategy for **Security testing** is clarified;
* the next step is to develop software, including **Code Reviews** (usually with peers), **Static Analysis** with automated tools and **Unit Tests** dedicated to security;
* then comes the long-awaited moment to perform tests on released codes: **Penetration Testing** ("Pentests"), using both manual and automated techniques; 
* and finally, after software has been **Accredited** by all stakeholders, it can be transitioned to Operation teams and safely put in Production. 

The picture below shows all the phases with the different artefacts:
-- TODO : Add a picture of a SDLC diagram that clarifies the description above --

Based on the risks of the project, some artefacts may be simplified (or even skipped) while others may be added (formal intermediary approvals, documentation of certain points, ...). **Always keep in mind a SDLC is meant to bring risk reduction to software development and is a framework that helps put in place controls that will reduce those risks to an acceptable level. ** While this is a generic description of SDLC, always tailor this framework to the needs of your projects.

#### Diving into phases and artefacts

-- TODO :  Quick description of all phases (what? when? who? ...) --

### Security Testing in the SDLC
-- TODO :

- Explain how it relates to and differs from quality assurance
- Explain the different types of tests (unit, Verification, Validation, ....)

--
### Technical Management
#### Test Strategy
-- TODO : Describe what a Security Test Strategy is, how it relates to other artefacts (Threat Model, Requirements, ...), how it is declined into Test Plans and Test Cases --
#### Test Case
-- TODO : Describe a typical test case for Security --
#### Reporting and Issue tracking
-- TODO : Explain reporting and Issue tracking (principles and popular tools) --
### Testing methods
#### White box
#### Grey box
#### Black box
### Team management
-- TODO :

- explain the importance of Separation of Duties (developers VS testers, ...)
- internal VS sub-contracted pentests

### References

- [1] Meyer's Recipe for Tomato Soup - http://www.finecooking.com/recipes/meyers-classic-tomato-soup.aspx
- [2] Another Informational Article - http://www.securityfans.com/informational_article.html
