# Home Labs

This section contains labs done in my "Home Lab" environment as part of my broader "ProofOfConcept" portfolio. This is a dedicated section for hardening and security research following a full lifecycle auditing process.

## Global Lab Environment
* **Primary OS:** Black Arch Linux
* **Target Machines:** Raspberry Pi 3 Model B+
* **Network Architecture:** TP-Link Archer AX21 AX1800 Dual Band WiFi 6 Router (isolated, offline LAN)

## Lab Directory
Each project will be labeled using a lab ID (i.e. L-000, L-001, L-002). Each lab will contain documentation that follows the full lifecycle audit process to demonstrate the proof-of-concept for GRC. 

Example:

* **L-000:** Project folder that outlines the vulnerability being tested, the associated CVE, and other relevant information.
    * **L-000-RMF:** The Risk Management Framework (RMF) subdirectory that houses the artifacts required for RMF compliance.
      * **0-Prepare:** The "Prepare" phase subdirectory. This phase establishes the foundational organizational context by defining the system boundary, identifying key stakeholders, and conducting an initial asset inventory to ensure a comprehensive scope for all subsequent risk management activities. This section will include the following:
        * **0A-Roles-and-Responsibilities:** A formal designation of key stakeholders and security personnel to ensure clear accountability and authorized oversight throughout the RMF lifecycle.
        * **0B-Asset-Inventory:** The asset inventory serves as a comprehensive catalog of all hardware, software, and data assets within the system boundary to ensure 100% visibility and accountability for control implementation.
        * **0C-Network-Diagram:** The network diagram serves as a high-level visual mapping of the system boundary, trust zones, and data flows required to define the scope of all subsequent security controls.
        * **0D-Initial-Security-Posture-Assessment:** A high-level review of existing environment conditions to identify obvious vulnerabilities and inform the initial risk profile.
      * **1-Categorize:** The "Categorize" phase subdirectory. This phase documents the analysis used to determine the system's impact level on the organization's mission by evaluating the sensitivity of information types and conducting a Business Impact Assessment (BIA) to establish the required security baseline. This section will include the following:
        * **1A-System-Security-Categorization:** A formal analysis utilizing FIPS 199 to determine the impact levels for Confidentiality, Integrity, and Availability based on the types of information processed, stored, or transmitted by the system.
        * **1B-Information-Type-Inventory:** A detailed identification of the information types within the system boundary, mapped to the appropriate security categories to justify the overall system impact level.
        * **1C-Business-Impact-Analysis:** The BIA identifies which mission-essential functions are most critical and the potential consequences of their disruption.
      * **2-Select:** The "Select" phase subdirectory. This phase outlines the selection of a tailored security control baseline and the development of the System Security Plan (SSP) to meet the specific risk requirements identified in phase 1 (categorize). This section will include the following:
        * **2A-Control-Baseline:** A curated set of security controls selected from the NIST 800-53 catalog based on the system's impact level and risk profile.
        * **2B-Control-Tailoring-Actions:** The rationalization for modifying or eliminating specific controls to fit the unique technical environment and operational needs of the lab.
        * **2C-System-Security-Plan:** The foundational governance document that provides a comprehensive overview of the security requiremets and the planned implementation strategy.
        * **2D-Disaster-Recovery-Planning:** A strategic document defining the procedures, technical requirements, and recovery time objectives (RTOs) necessary to restore system operations following catastrophic failure.
      * **3-Implement:** The "implement" phase subdirectory. This phase documents the technical execution of the selected security controls, including system hardening, configuration management, and the initial gap analysis to verify the system's baseline security posture. This section will include the following:
        * **3A-Gap-Analysis:** Determine which controls are already implemented and which controls need to be established to ensure compliance (architectural gaps).
        * **3B-Implementation-Statements:** Detailed technical narratives describing the specific methods and configurations used to meet each selected security control.
        * **3C-Technical-Configurations:** The raw technical artifacts, including scripts, configuration files, and exported rulesets, that constitute the system's security posture.
        * **3D-System-Inheritance-Report:** An Identification of security controls provided by external service providers or common infrastructures rather than the system itself.
      * **4-Assess:** The "Assess" phase subdirectory. This section outlines the "testing" phase to determine if the controls are implemented correctly and operating as intended. This section will include the following:
        * **4A-Examination:** Reviewing documentation, system configurations, and logs to obtain evidence of control effectiveness.
        * **4B-Interviewing** Discussing security practices with staff to clarify how controls are managed.
        * **4C-Testing:** Actively exercising objects (like networks or software) to compare expected behavior with actual behavior.
          * **4CA-Vulnerability-Scanning:** Using automated tools to identify known flaws in an active system.
          * **4CB-Penetration-Testing:** Using tools in an attempt to exploit the identified vulnerabilities to demonstrate the real-world risks.
            * **4CBA-RoE:** The "Rules of Engagement" document that outlines the scope and legal authorization for the penetration test.
            * **4CBB-Gap-Analysis-Second-Review:** Compare vulnerability findings against the security plan outlined in the SSP to see where the implemented controls failed to meet the requirement. This review provides a more technical deep-dive.
            * **4CBC-Security-Assessment-Report:** After scanning and testing, the results are summarized in the SAR. This data will be used to develop the risk heatmap.
            * **4CBD-Risk-Heatmap:** Results from the vulnerability scanning phase and penetration testing phase (outlined in the SAR) are used to create a risk heatmap to visually display and quantify security and privacy information by mapping the likelihood of a breach or exploitation.
            * **4CBE-Plan-of-Action-and-Milestones:** The Plan of Action and Milestones (POA&M) document outlines vulnerabilities that cannot be fixed immediately. This provides a plan and timeline for remediation.
      * **5-Authorize:** The "Authorize" phase subdirectory. This phase documents the formal acceptance of residual risk and the official authorization to operate (ATO), ensuring all identified vulnerabilities are tracked via a POA&M and approved by leadership. This section will include the following:
        * **5A-Plan-of-Action-and-Milestones (POA&M):** A management document identifying tasks to be accomplished and resources required to remediate known vulnerabilities discovered during the assessment phase.
        * **5B-Authorization-Decision-Document (Authorization to Operate- ATO):** A formal memorandum signed by the Authorizing Official that officially accepts the residual risk and grants the system permission to operate for a specific period.
      * **6-Monitor:** The "Monitor" phase subdirectory. This phase establishes the framework for ongoing security oversight, ensuring the system's defensive posture is maintained through continuous control assessments, configuration changes management, and incident response readiness. This section will include the following:
        * **6A-Continuous-Monitoring-Strategy:** A documented plan for the ongoing assessment of security control effectiveness, including the frequency of reviews and the selection of automated monitoring tools.
        * **6B-System-Change-Log (Configuration Management):** A record of all modifications made to the system hardware, software, or firmware to ensure that changes do not negatively impact the security posture.
        * **6C-Incident-Response-Testing-Log:** Documentation of tabletop exercises or simulated security incidents used to verify the organization's ability to detect, respond, and recover from a breach.
