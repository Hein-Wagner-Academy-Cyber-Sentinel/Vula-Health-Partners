# Phase 1 reflection — Avril Wessels

_What did I do? What did I find hard? What would I do differently? What do I understand now that I did not before?_

**Pair:** Pair 3 (Avril Wessels and Nathan Botes)  
**Client Persona:** Vula Health Partners  
**Phase 1 Role:** Build Lead  

---

## Introduction and Team Collaboration

During Phase 1 of the Build It Anywhere Action Learning Project, my partner Nathan Botes and I worked together on our assigned client persona, Vula Health Partners—a healthcare administrator responsible for processing sensitive medical and billing records. For this foundational phase, I served as the Build Lead while Nathan acted as the Assurance Lead. 

Throughout our Action Learning Fridays, most of our communication happened verbally. Because Phase 1 leaned heavily on initial documentation while simultaneously standing up our technical environment, Nathan took the lead on drafting the written assurance and business documents, while I focused on initializing our repository, configuring my local workstation toolchain, and reviewing the written deliverables to ensure they aligned with our persona and our overall vision for the platform.

---

## What did I do?

As the Build Lead for Phase 1, my primary technical responsibility was establishing our pair's central version-control environment and verifying my local development toolchain:

* **Repository Initialization and Access Control:** I created our pair's public GitHub repository from the official Hein Wagner Academy template inside the Academy organization. Once the repository structure was generated, I invited Nathan as a collaborator so that we could both contribute to the codebase and maintain a shared portfolio.
* **Initial Documentation and Pipeline Verification:** I updated the main `README.md` file to record both of our names, our assigned persona (Vula Health Partners), and our designated roles for Phase 1. I staged, committed, and pushed these initial changes from my local machine to GitHub without issue. Following the push, I navigated to the GitHub Actions tab and verified that our starter continuous integration (CI) pipeline executed and passed ("ran green"), confirming that our automated validation workflow was active from week one.
* **Local Toolchain Installation and Verification:** On my local machine, I set up and configured the required Phase 1 tools inside Ubuntu on Windows Subsystem for Linux (WSL2), including the `alp-env` Python virtual environment, Git, Docker, OpenTofu, Moto with the AWS CLI, `asciinema`, and the security scanners (`gitleaks`, `Checkov`, and `Trivy`).
* **Text-Native Evidence Capture:** To produce my first piece of accessible, text-native evidence, I recorded a terminal session using `asciinema`. During the recording, I systematically ran each tool's executable followed by the `--version` flag to prove that every component of the Phase 1 toolchain was properly installed and responding in my terminal.
* **Research, Quality Assurance, and Peer Review:** For the business and governance deliverables—specifically the one-page Business Profile, the Protection of Personal Information Act (POPIA) exposure assessment, Threat Model v0, and the Project Charter—I conducted my own independent background research into Vula Health Partners' healthcare sector and regulatory pressures. Because Nathan had already drafted thorough, well-structured versions of these documents as Assurance Lead, I did not need to rewrite them. Instead, I acted as the reviewer: I proofread the Project Charter (checking scope, success criteria, assumptions, and out-of-scope items) and cross-checked the Business Profile, POPIA exposure analysis, and Threat Model v0 to verify that they accurately reflected our healthcare persona and project goals.

---

## What did I find hard?

Transitioning from theoretical study to a strictly terminal-driven, code-first workflow presented several genuine challenges during Phase 1:

* **Terminal Navigation and Git Synchronization:** The most difficult technical hurdle for me was linking and merging the remote GitHub repository with the directory on my local machine. Because I am still building confidence working entirely inside the Linux command-line terminal rather than graphical interfaces, managing divergent branches and resolving Git merge conflicts felt overwhelming at first.
* **Authentication and Network Setup:** Configuring SSH keys, personal access tokens, and completing the Academy UniFi network certificate trust step were tricky to get right on the first attempt. However, by reaching out to my teammates and working through the configuration steps together, I was able to resolve the authentication errors and establish a working connection to GitHub.
* **Understanding Project Expectations and Persona Framing:** Beyond the technical commands, I initially struggled to grasp the bigger picture of the Action Learning Project and what the Vula Health Partners persona required from us as a pair. Translating a simulated business scenario into formal cloud security deliverables is a completely new way of working for me. While my understanding has improved as Phase 1 progressed, I recognize that I am still building confidence in connecting business context to technical architecture.

---

## What would I do differently?

Looking back at how Phase 1 unfolded, there are two practical habits I plan to change moving into Phase 2:

* **Simplify My Local Directory Structure:** When setting up my WSL Ubuntu environment and cloning project files, I placed my working folders deep inside a long directory path. Navigating that overly long file path in the terminal every Friday was frustrating and slowed me down. Going forward, I will keep my project repository and virtual environment directly inside my standard user's home directory (`~`) so that paths remain short, clean, and easy to manage.
* **Proactively Verify File Status and Pipeline Runs:** Rather than assuming my local files are clean or assuming a commit automatically passed in GitHub Actions, I will make it a strict habit to check my repository status (`git status`) before and after working, ensure no file ownership or conflict markers remain, and actively confirm that the GitHub Actions pipeline runs green after every push.
* **Maintain Our Documentation Workflow:** Regarding how Nathan and I approached the business documents and Friday schedules, I would not change our format. Keeping our documentation concise and well-summarized worked smoothly for our pair and allowed us to stay on track during our Friday sessions.

---

## What do I understand now that I did not before?

Even though Phase 1 was challenging, it shifted several concepts from textbook theory into practical reality:

* **From Theory to Practice in Linux Administration:** Before starting this project, I already understood the theory behind Linux user account types (`root` versus standard users) and file permissions from earlier modules. What changed in Phase 1 was applying that knowledge practically—experiencing firsthand how running commands or creating files under the wrong user context impacts daily Git and SSH operations, and how to remediate ownership in a live terminal.
* **Version Control as Team Memory:** I now understand why Git, GitHub repositories, and automated pipelines are essential when working in a pair. Having a shared commit history means we can inspect exactly what our partner changed and when, without having to constantly ask each other what was done the previous day or the previous Friday—which is vital because it is easy to forget small details between sessions.
* **Accessibility and Independence Through Text-Native Evidence:** The project's strict "Everything as code" and "Evidence as text" rules make complete sense to me now. Screen readers cannot interpret screenshots of graphical consoles, which locks blind and low-vision engineers out of traditional visual workflows. By using Markdown files, configuration code, and `asciinema` terminal transcripts, blind learners can read, verify, and produce audit-ready evidence completely independently on the exact same footing as sighted peers.
* **Zero-Cost Local Emulation:** While I am still learning how OpenTofu and Moto work under the hood, I now understand the core purpose of local cloud emulation: it allows us to design, test, and practice cloud infrastructure safely on our own laptops without needing a live cloud account or worrying about receiving an unexpected bill from Microsoft or AWS.
* **Connecting POPIA Compliance to Technical Security for Vula Health Partners:** Finally, my biggest takeaway regarding our persona is how directly legal compliance drives technical design. Because Vula Health Partners handles Special Personal Information—such as patient medical records and billing histories—both hardware and software security are critical. Understanding the specific threats facing our healthcare persona in Threat Model v0 is not just paperwork; it tells us exactly what risks our cloud architecture must defend against so that patient data remains confidential, intact, and compliant with POPIA.

