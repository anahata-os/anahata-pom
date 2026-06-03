# Project Instructions: anahata-pom

This file contains project-specific system instructions for the **anahata-pom** project.

## 6. Centralized CI/CD & DevOps Philosophy 👑📡

To preserve maximum **Simplicity, Leanliness, and Maintainability**, this project implements a world-class **GitHub Reusable Workflows** architecture:

*   **The Master Workflow (`shared-maven-build.yml`):** Resides strictly in this grandfather repository. It houses all compilation, GPG signing, Sonatype deploying, and the secure `settings.xml` override step to trust insecure HTTP Artifactory repositories globally.
*   **Zero Duplication:** No child repository is allowed to copy-paste setup scripts, GPG configurations, or custom settings.xml writers. They must inherit from this grandfather's shared template in a simple 5-line import block.
*   **Single Point of Truth:** Any systemic modifications, token rotations, or JDK updates are made strictly inside this repository, automatically modernizing the entire 7-project library stack instantly!

*Força Barça!*
