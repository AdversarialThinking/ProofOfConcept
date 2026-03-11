# ProofOfConcept
This repository serves as a centralized portfolio for my cybersecurity research, system hardening, and defensive architecture labs. Each project follows a full life cycle audit audit approach: identifying and exploiting a vulnerability (Red Team), implementing the proper controls to mitigate the vulnerability (Blue Team, and documenting the mitigation strategy (GRC/Audit). 

## Global Lab Environment
* **Primary OS:** Black Arch Linux
* **Target Machines:** Raspberry Pi 3 Model B+
* **Network Architecture:** TP-Link Archer AX21 AX1800 Dual Band WiFi 6 Router (isolated, offline LAN)

## Lab Directory
Each project will be labeled using a lab ID (i.e. L-01, L-02, L-03) with a ReadMe to document the CVE being tested. Each lab directory will contain a sub-directory documenting the audit process to demonstrate the proof-of-concept for GRC. 

Example:

* **L-01:** Outlines the vulnerability being tested, the associated CVE, and other relevant information.
  * **L-01-Audit**
    * **L-01-RMF**
      * **L-01-Prepare:** This section outlines the scope of the audit. This section will also contain the following:
        * **Business Impact Analysis:** The BIA identifies which mission-essential functions are most critical and the potential consequences of their disruption.
        * **Gap Analysis:** Determine which controls are already implemented and which controls need to be established to ensure compliance (architectural gaps).
      * **L-01-Categorize:** This section determines the impact of a loss of confidentiality, integrity, or availability (CIA triad) on the organization's mission and assets using the BIA.
      * **L-01-Select-and-Implement:** This section outlines the security controls that are selected and implemented within the system and its operational environment based on the impact levels. This section will include the following:
        * **Gap Analysis Review:** Review the previous gap analysis to identify missing controls in the system's architectural design to help develop the DRP.
        * **Disaster Recovery Planning:** This section outlines the organization's plans on how to protect and recover the system.
      * **L-01-Assess:** This section outlines the "testing" phase to determine if the controls are implemented correctly and operating as intended. This section will include the following:
        * **Examination:** Reviewing documentation, system configurations, and logs to obtain evidence of control effectiveness.
        * **Interviewing** Discussing security practices with staff to clarify how controls are managed.
        * **Testing:** Actively exercising objects (like networks or software) to compare expected behavior with actual behavior.
          * **Vulnerability Scanning:** Using automated tools to identify known flaws in an active system.
          * **Penetration Testing:** Using tools in an attempt to exploit the identified vulnerabilities to demonstrate the real-world risks.
            * **Gap Analysis Second Review:** Compare vulnerability findings against the security plan outlined in the DRP to see where the implemented controls failed to meet the requirement. This review provides a more technical deep-dive.
            * **Security Assessment Report:** After scanning and testing, the results are summarized in the SAR. This data will be used to develop the risk heatmap.
            * **Risk Heatmap:** Results from the vulnerability scanning phase and penetration testing phase (outlined in the SAR) are used to create a risk heatmap to visually display and quantify security and privacy information by mapping the likelihood of a breach or exploitation.
            * **Plan of Action and Milestones:** The Plan of Action and Milestones (POA&M) document outlines vulnerabilities that cannot be fixed immediately. This provides a plan and timeline for remediation.
      * **L-01-Authorize-and-Monitor:** This section outlines whether or not to accept the risk based on the assessment results. The system is then continuously monitored for changes in its security posture using a continuous gap analysis.
