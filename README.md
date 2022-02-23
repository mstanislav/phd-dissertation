# Mark Stanislav's Ph.D. Dissertation Resources
## Overview
This repository offers artifacts and data relevant to the [Ph.D. in Cyber Operations](https://dsu.edu/programs/phdco/index.html) dissertation by [Mark Stanislav](https://uncompiled.com/) entitled, _Multi-dimensional Security Integrity Analysis of Broad Market Internet-connected Cameras_ that was defended during March, 2022 at [Dakota State University](https://dsu.edu/).

## Repository Contents
* **Assessment Tracking-Test Coverage.md:** An association the study's assessment needs with testing criteria to yield results, with a rollup of the number of controls that each entry would satisfy from the original input IoT frameworks that acted as inspiration for the data to gather during the study.
* **Study Data.{csv,json,xlsx}:** Organized data that was captured during the study's sample device analysis, which serves at the basis for IoT security framework mapping inputs. This data set is presented in three formats to allow future researchers to more easily interact with it for their own analysis/interests.
* **Proposed IoT Framework.md:** Details of an IoT security framework that was generated as part of the dissertation to provide a different lens to view the results of the study results through. While the framework is intended to represent a simple, valuable, and reasonable IoT security framework to use for analysis, it should _not_ be seen as an attempt to create yet-another-standard in any formal way.
* **Camera Credentials.md:** Credentials that were found within vendor documentation or during the analysis of firmware during the study's research. While some credentials have a password provided, many of the entries only provide the password hash since it was unable to be found online or readily cracked in a timely/low cost manner.
* **Proposed Framework - Study Result Mapping.csv:**  Device outcomes for the proposed IoT security framework control testing including statistical roll-up details.
* **Proposal-Presentation.pdf:** The slide deck used for this dissertation's proposal defense slide deck that occurred during March, 2021, and explains the context, literature review, goals, and study plan that was conducted over the following year.
* **DCMS-Test Criteria Mapping.md:** A mapping of testing criteria against DCMS controls that can be checked against the _Study Data_ results that will yield a _Pass_ or _Fail_ outcome. Some controls are out-of-scope and marked as such with _OOS_.
* **DCMS-Study Result Mapping.csv:** Device outcomes for DCMS control testing including statistical roll-up details.
* **ETSI-Test Criteria Mapping.md:** A mapping of testing criteria against ETSI controls that can be checked against the _Study Data_ results that will yield a _Pass_ or _Fail_ outcome. Some controls are out-of-scope and marked as such with _OOS_.
* **ETSI-Study Result Mapping.csv:** Device outcomes for ETSI control testing including statistical roll-up details.
* **Cameras:** A folder that contains folders for each assessed camera containing internal, external, & packaging photos, along with any digital user manuals.

## License
Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg