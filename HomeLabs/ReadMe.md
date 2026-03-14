# Home Labs

This section contains labs done in my "Home Lab" environment as part of my broader "ProofOfConcept" portfolio. This is a dedicated section for hardening and security research following a full lifecycle auditing process.

## Global Lab Environment
* **Primary OS:** Black Arch Linux
* **Target Machines:** Raspberry Pi 3 Model B+
* **Network Architecture:** TP-Link Archer AX21 AX1800 Dual Band WiFi 6 Router (isolated, offline LAN)

## Lab Directory
Each project will be labeled using a lab ID (i.e. L-01, L-02, L-03). Each lab will contain documentation that follows the full lifecycle audit process to demonstrate the proof-of-concept for GRC. 

Example:

* **L-01:** Project folder that outlines the vulnerability being tested, the associated CVE, and other relevant information.
    * **L-01-RMF:** The Risk Management Framework (RMF) subdirectory that houses the artifacts required for RMF compliance.
      * **1-Prepare:** The "Prepare" phase subdirectory. This section outlines the scope of the audit. This section will also contain the following:
        * **1A-Business-Impact-Analysis:** The BIA identifies which mission-essential functions are most critical and the potential consequences of their disruption.
        * **1B-Gap-Analysis:** Determine which controls are already implemented and which controls need to be established to ensure compliance (architectural gaps).
      * **2-Categorize:** The "Categorize" phase subdirectory. This section determines the impact of a loss of confidentiality, integrity, or availability (CIA triad) on the organization's mission and assets using the BIA.
      * **3-Select-and-Implement:** The "Select and Implement" phase subdirectory. This section outlines the security controls that are selected and implemented within the system and its operational environment based on the impact levels. This section will include the following:
        * **3A-Gap-Analysis-Review:** Review the previous gap analysis to identify missing controls in the system's architectural design to help develop the DRP.
        * **3B-Disaster-Recovery-Planning:** This section outlines the organization's plans on how to protect and recover the system.
      * **4-Assess:** The "Assess" phase subdirectory. This section outlines the "testing" phase to determine if the controls are implemented correctly and operating as intended. This section will include the following:
        * **4A-Examination:** Reviewing documentation, system configurations, and logs to obtain evidence of control effectiveness.
        * **4B-Interviewing** Discussing security practices with staff to clarify how controls are managed.
        * **4C-Testing:** Actively exercising objects (like networks or software) to compare expected behavior with actual behavior.
          * **4CA-Vulnerability-Scanning:** Using automated tools to identify known flaws in an active system.
          * **4CB-Penetration-Testing:** Using tools in an attempt to exploit the identified vulnerabilities to demonstrate the real-world risks.
            * **4CBA-Gap-Analysis-Second-Review:** Compare vulnerability findings against the security plan outlined in the DRP to see where the implemented controls failed to meet the requirement. This review provides a more technical deep-dive.
            * **4CBB-Security-Assessment-Report:** After scanning and testing, the results are summarized in the SAR. This data will be used to develop the risk heatmap.
            * **4CBC-Risk-Heatmap:** Results from the vulnerability scanning phase and penetration testing phase (outlined in the SAR) are used to create a risk heatmap to visually display and quantify security and privacy information by mapping the likelihood of a breach or exploitation.
            * **4CBD-Plan-of-Action-and-Milestones:** The Plan of Action and Milestones (POA&M) document outlines vulnerabilities that cannot be fixed immediately. This provides a plan and timeline for remediation.
      * **5-Authorize-and-Monitor:** The "Authorize and Monitor" phase subdirectory. This section outlines whether or not to accept the risk based on the assessment results. The system is then continuously monitored for changes in its security posture using a continuous gap analysis.
