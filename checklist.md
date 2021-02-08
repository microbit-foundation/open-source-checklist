# Open Source Checklist

This aim of this checklist is to provide the minimum set of things that must be done before releasing our code or other content as open source. Not all items on the checklist will apply to every release, as noted and some projects may trigger other considerations as this list is not exhaustive.

This checklist does not replace the decision about what should be released, under what license, when it should be released or how it should be announced. These decisions will have been made before using this checklist. 


## ToC

- [Public Project Name](#1-public-project-name)
- [Licensing Information](#2-licensing-information)
- [Project Information](#3-project-information)
- [Content](#4-content)
- [Continuous Integration](#5-continuous-integration)
- [Code of Conduct](#6-code-of-conduct)
- [Security](#7-security)


## 1. Public Project Name

When naming a project, we need to consider if we also want to brand or market the project name, in which case, we may want to even register a trademark. For other projects, something descriptive may suffice. Use of third-party names or trademarks is usually not a good idea.

See http://fossmarks.org/ for more information on trademarks and choosing a project name.


## 2. Licensing Information

Licensing info includes identifying the outbound license (the license under which users take our software); and the inbound license (the license under which people contribute to our software.

The inbound license may be the same license as the outbound license, may also use the Developer's Certificate of Origin or the inbound agreement may be a different license like a contributor license agreement or assignment agreement.

In any case, it's important to make it easy for users and contributors of our projects to easily understand what license applies when.

- [ ] 2.1 **License file:** Place the complete text of the outbound license in its own file called, LICENSE or LICENSE.md, at the top-level directory.
- [ ] 2.2 **License and copyright notice:** Place the SPDX-License-Identifier tag for the outbound license in every file at or near the top of the file in a comment. The SPDX-License-Identifier syntax may consist of a single SPDX license identifier or an SPDX License Expression to represent a single license or a compound set of licenses (respectively) that apply to that file. If a file contains third party open source under a different license, see section on third party open source below. Place the our copyright notice in every file we author as shown below.
  > (c) [year file created] - [last year file modified], Micro:bit Educational Foundation and contributors
  >
  > SPDX-License-Identifier: Apache-2.0
  - For more information on the use of SPDX identifiers, see: https://spdx.org/ids or https://spdx.org/ids-how
- [ ] 2.3 **Identify the inbound and outbound license in the README:** Include a short, concise statement as to the outbound license in the README, preferably in a section called “license” and link to the LICENSE file and CONTRIBUTING file as appropriate.
- [ ] 2.4 **Identify the inbound and outbound license on the project’s website (if applicable):**  Include a short, concise statement as to the outbound and inbound license in a conspicuous place on the project’s website, if there is one. This can be simply the same statement used in the README, with the appropriate links.
- [ ] 2.5 **Contributing file:** Place a file at the top-level directory called CONTRIBUTING or CONTRIBUTING.md, which include information about how to contribute to your project, coding standards, as well as the inbound license information. Also include instructions for contributors to add their name (if they so wish) to the CONTRIBUTORS file.
- [ ] 2.6 **Contributors file (optional):** Place a file at the top-level directory called CONTRIBUTORS, which includes a self-maintained list of names and email addresses of contributors.
    - GitHub also tracks contributors, so this could be used as well.
- [ ] 2.7 **Identify inclusion of third-party open source code:** If our open source project incorporates third-party open source code in the repository, users will want to know about this especially if the third-party code uses a different open source license than the project.  There is no one way to identify third-party code and its license. The best way may depend on how the repository is structured or how much third-party open source code is incorporated. We might put a statement in our README, put all third-party code in a specific directory, or both.  Be sure to include the full license text for the third-party code as well and name these files with a project or license naming scheme to avoid confusion with the main project license. The end-goal here is to make it easy to know what is there without requiring our users to run a scan and audit of our code to find out.
- [ ] 2.8 **License for additional documentation:** If the project has extensive additional documentation beyond the README, use a license notice in the file or document and place a full copy of the license text in the associated directory following the same advice as above. Where images of the micro:bit or logos are used, consider including a reference to the Community Guidelines page and a friendly reminder about the rules for working with our brand. 


## 3. Project Information

- [ ] 3.1 The GitHub description (underneath the repo title) is clear and concise and includes, if applicable, a link to the relevant website.
- [ ] 3.2 The project has a descriptive README.md file rendered on the GitHub repo entry page. The README includes:
    - [ ] Project title.
    - [ ] Project description.
    - [ ] Project introduction.
    - [ ] Inbound and Outbound licenses (more info in the "2. Licensing Information" section).
    - [ ] Links to relevant documentation or information.
    - [ ] Link to the Code Of Conduct.
- [ ] 3.3 Where applicable, ensure there is appropriate additional documentation (e.g., technical documentation, webpage source, etc.).
- [ ] 3.4 The project is versioned (the preferred versioning system is Semantic Versioning 2.0.0).
- [ ] 3.5 GitHub Releases are used to mark releases and releases are git tagged with a description.
- [ ] 3.6 Changes for each release are captured, either in a CHANGELOG file at the top-level directory, or within the GitHub release descriptions.
- [ ] 3.7 There is a `.gitignore` file excluding everything we don’t want versioned.
- [ ] 3.8 There are contributing guidelines (preferably in a CONTRIBUTING file) that communicate ways to contribute, any guidance regarding contributing (e.g., relevant coding standards) or related information. 
- [ ] 3.9 (Optional) Add topics to the repository.
- [ ] 3.10 (Optional) Add issue templates for common contributions as appropriate or relevant.
- [ ] 3.11 (Optional) Add PR templates for common contributions as appropriate or relevant.


## 4. Content

Check commits, documentation, code and go through the git history to check for the following:

- [ ] 4.1 There is no swearing or anything offensive (use personal judgement and remember that young people and our partners can read this)
- [ ] 4.2 There is no confidential information belonging to us or any third party. There are no passwords, secrets or similar information. Pay special attention to the git history in case something was accidentally added and removed.
- [ ] 4.3 Any mention of third-parties or third-party trademarks or tradenames, including partners or founder partner names should be mentioned in factual context (e.g., “This supports Company XYZ’s new toy”, “This includes library developed by XYZ”). Where discussions of partners in other than positive or neutral light are deemed necessary, sign-off should be sought from the management team as the publishing team deems appropriate to ensure appropriate relationship management steps can be taken.


## 5. Continuous Integration

- [ ] 5.1 CI scripts do not contain any passwords or secrets.
- [ ] 5.2 CI SaaS project does not contain any env var that could leak. If there are env vars, the CI project is configured to not trust forks and PRs.
- [ ] 5.3 CI SaaS global settings do not contain any env var or secret shared to this project that could leak.


## 6. Code of Conduct

- [ ] 6.1 Include a section in the README for the Code of Conduct and link to the Foundation Code Of Conduct.
- [ ] 6.2 If there is a project website, include information about the Code of Conduct with the appropriate links.


## 7. Security

[something to consider adding? Might have a look at relevant standards here https://www.coreinfrastructure.org/programs/badge-program/]

-----

This document is released under the [Creative Commons Attribution 4.0 International license](LICENSE).

SPDX-License-Identifier: CC-BY-4.0
