# Home Labs

This section contains labs done in my "Home Lab" environment as part of my broader "ProofOfConcept" portfolio. This is a dedicated section for hardening and security research following a full lifecycle auditing process.

## Global Lab Environment
* **Primary OS:** Black Arch Linux
* **Target Machines:** Raspberry Pi 3 Model B+
* **Network Architecture:** TP-Link Archer AX21 AX1800 Dual Band WiFi 6 Router (isolated, offline LAN)

## Lab Directory Hierarchy:

Each project will be labeled using a lab ID (i.e. L-000, L-001, L-002). Each lab will contain documentation that follows the full lifecycle audit process to demonstrate the proof-of-concept for GRC. 


* **L-000:** Project folder that outlines the vulnerability being tested, the associated CVE, and other relevant information.

   * **L-000-RMF:** The Risk Management Framework (RMF) subdirectory that houses the artifacts of each phase required for RMF compliance.

## Prepare (Phase 0)

* **0-Prepare:** The "Prepare" phase subdirectory. This phase establishes the foundational organizational context by defining the system boundary, identifying key stakeholders, and conducting an initial asset inventory to ensure a comprehensive scope for all subsequent risk management activities. Asset inventory, Network Diagrams, and Initial Security Posture documentation provide the framework for the SSP **(PL-1; the "why" and "who"),** which is a living, breathing document. This section maps to *NIST SP 800-37/800-39; Organizational governance and risk management strategy.* This section will include the following:

  * **0A-Roles-and-Responsibilities: (PM-16/PS-7)** - A formal designation of key stakeholders and security personnel to ensure clear accountability and authorized oversight throughout the RMF lifecycle. **Living, breathing document - update for staff/structural changes.**
  * **0B-Asset-Inventory: (CM-8)** - The asset inventory serves as a comprehensive catalog of all hardware, software, and data assets within the system boundary to ensure 100% visibility and accountability for control implementation. **Living, breathing document - update for hardware/software changes.**
  * **0C-Network-Diagram: (SC-7/SA-8/AC-4)** - The network diagram serves as a high-level visual mapping of the system boundary, trust zones, and data flows required to define the scope of all subsequent security controls. **Living, breathing document - update for network topology changes.**
  * **0D-Initial-Security-Posture-Assessment:(RA-3/CA-2/PM-9/PL-1)** - A high-level review of existing environment conditions to identify obvious vulnerabilities and inform the initial risk profile. This document includes the *Risk Management Strategy (PM-9).* **Static document - snapshot for initial risk profile.**

## Categorize (Phase 1)

* **1-Categorize:** The "Categorize" phase subdirectory. This phase documents the analysis used to determine the system's impact level on the organization's mission by evaluating the sensitivity of information types and conducting a Business Impact Assessment (BIA) to establish the required security baseline. This section maps to *FIPS 199/NIST SP 800-60; Determining high/mod/low impact based on data types.* This section will include the following:

  * **1A-System-Security-Categorization: (PL-4)** - A formal analysis utilizing FIPS 199 to determine the impact levels for Confidentiality, Integrity, and Availability based on the types of information processed, stored, or transmitted by the system. **Static document - static unless mission or data type changes.**
  * **1B-Information-Type-Inventory: (PL-2/MP-2)** - A detailed identification of the information types within the system boundary, mapped to the appropriate security categories to justify the overall system impact level. **Living, breathing document - update if new data types are processed.**
  * **1C-Business-Impact-Analysis: (CP-2/PL-4)** - The BIA identifies which mission-essential functions are most critical and the potential consequences of their disruption. **Static document - static unless mission or functions change.**

## Select (Phase 2)

* **2-Select:** The "Select" phase subdirectory. This phase outlines the selection of a tailored security control baseline and the development of the System Security Plan (SSP) to meet the specific risk requirements identified in phase 1 (categorize). This section maps to *NIST SP 800-53B; Selecting the control baselines and tailoring them.* This section will include the following:

  * **2A-Control-Baseline: (RA-4)** - A curated set of security controls selected from the NIST 800-53 catalog based on the system's impact level and risk profile. **Static document - static unless categorization changes.**
  * **2B-Control-Tailoring-Actions: (RA-4)** - The rationalization for modifying or eliminating specific controls to fit the unique technical environment and operational needs of the lab. **Static document - static unless architecture changes.**
  * **2C-System-Security-Plan: (PL-2)** - The foundational governance document that provides a comprehensive overview of the security requirements and the planned implementation strategy. This part of the SSP maps to the "why" of the security controls. **Living, breathing document - primary operational security document.**
  * **2D-Disaster-Recovery-Planning: (CP-2)** - A strategic document defining the procedures, technical requirements, and recovery time objectives (RTOs) necessary to restore system operations following catastrophic failure. **Living, breathing document - annual update mandatory via CP-4.**

## Implement (Phase 3)

* **3-Implement:** The "implement" phase subdirectory. This phase documents the technical execution of the selected security controls, including system hardening, configuration management, and the initial gap analysis to verify the system's baseline security posture. This section maps to *NIST SP 800-53/800-160; Engineering the controls into the system.* This section will include the following:

  * **3A-Gap-Analysis: (CA-7)** - Determine which controls are already implemented and which controls need to be established to ensure compliance (architectural gaps). **Living, breathing document - snapshot of control implementation status, updated after vulnerability scanning and penetration testing.**
  * **3B-Implementation-Statements: (PL-2)** - Detailed technical narratives describing the specific methods and configurations used to meet each selected security control. **Living, breathing document - update when technology or controls change.**
  * **3C-Technical-Configurations: (CM-2/CM-3/CM-5)** - The raw technical artifacts, including scripts, configuration files, and exported rulesets, that constitute the system's security posture. **Living, breathing document - current security posture.**
  * **3D-System-Inheritance-Report: (SA-9)** - An Identification of security controls provided by external service providers or common infrastructures rather than the system itself. **Living, breathing document - update when external services added/removed.**

## Assess (Phase 4)

* **4-Assess:** The "Assess" phase subdirectory. This section outlines the "testing" phase to determine if the controls are implemented correctly and operating as intended. This section maps to *NIST SP 800-53A; Auditing guide.* This section will include the following:

  * **4A-Examination: (CA-2)** - Reviewing documentation, system configurations, and logs to obtain evidence of control effectiveness. **Static document - raw artifacts of a single assessment.**
  * **4B-Interviewing: (CA-2)** - Discussing security practices with staff to clarify how controls are managed. **Static document - raw artifacts of a single assessment.**
  * **4C-Testing: (CA-2)** - Actively exercising objects (like networks or software) to compare expected behavior with actual behavior. **Static document - raw artifacts of a single assessment.**
    * **4CA-Vulnerability-Scanning: (RA-5)** - Using automated tools to identify known flaws in an active system. **Static document - raw artifacts of a single assessment.**
    * **4CB-Penetration-Testing: (CA-8)** - Using tools in an attempt to exploit the identified vulnerabilities to demonstrate the real-world risks. **Static document - raw artifacts of a single assessment.**
      * **4CBA-RoE: (CA-8)** - The "Rules of Engagement" document that outlines the scope and legal authorization for the penetration test. **Living, breathing document - used for every assessment; updated if scope changes.**
      * **4CBB-Gap-Analysis-Review: (CA-7)** - Compare vulnerability findings against the security plan outlined in the SSP to see where the implemented controls failed to meet the requirement. This review provides a more technical deep-dive. **Living, breathing document - Reviewed and updated after vulnerability scanning and penetration testing.**
      * **4CBC-Security-Assessment-Report: (CA-4)** - After scanning and testing, the results are summarized in the SAR. This data will be used to develop the risk heatmap. **Living, breathing document - updated quarterly or after significant changes.**
      * **4CBD-Risk-Heatmap: (RA-3)** - Results from the vulnerability scanning phase and penetration testing phase (outlined in the SAR) are used to create a risk heatmap to visually display and quantify security and privacy information by mapping the likelihood of a breach or exploitation. **Living, breathing document - updated quarterly or after significant changes.**
      * **4CBE-Plan-of-Action-and-Milestones-Draft: (PM-4)** - The Plan of Action and Milestones (POA&M) document outlines vulnerabilities that cannot be fixed immediately. This provides a plan and timeline for remediation. **Living, breathing document - used throughout assess and authorize phase.**

## Authorize (Phase 5)

* **5-Authorize:** The "Authorize" phase subdirectory. This phase documents the formal acceptance of residual risk and the official authorization to operate (ATO) by the Authorizing Official (AO), ensuring all identified vulnerabilities are tracked via a POA&M and approved by leadership. This section maps to *NIST SP 800-37; Risk-acceptance and ATO.* This section will include the following:

  * **5A-Plan-of-Action-and-Milestones-Review: (PM-4)** - The POA&M is reviewed by the Authorizing Official for final integration into the Authorization Decision Document. **Living, breathing document - used throughout assess and authorize phase.**
  * **5B-Authorization-Decision-Document (Authorization to Operate- ATO): (CA-6)** - A formal memorandum signed by the Authorizing Official that officially accepts the residual risk and grants the system permission to operate for a specific period. The POA&M is integrated into the formal *Authorization Decision Document* for finalization. It serves as the binding commitment to remediate outstanding vulnerabilities within defined milestones. In this phase, the POA&M provides the transparency necessary for the Authorizing Official to make an informed, risk-based decision to authorize the system's operation. **Static document - formal, static authorization to operate.**

## Monitor (Phase 6)

* **6-Monitor:** The "Monitor" phase subdirectory. This phase establishes the framework for ongoing security oversight, ensuring the system's defensive posture is maintained through continuous control assessments, configuration changes management, and incident response readiness. This section maps to *NIST SP 800-137; Continuous monitoring and automated reporting.* This section will include the following:

  * **6A-Continuous-Monitoring-Strategy: (CA-7)** - A documented plan for the ongoing assessment of security control effectiveness, including the frequency of reviews and the selection of automated monitoring tools. **Living, breathing document - defines how the system remains in compliance.**
  * **6B-System-Change-Log (Configuration Management): (CM-3)** - A record of all modifications made to the system hardware, software, or firmware to ensure that changes do not negatively impact the security posture. **Living, breathing document - continuous log of all configuration changes.**
  * **6C-Incident-Response-Testing-Log: (IR-3)** - Documentation of tabletop exercises or simulated security incidents used to verify the organization's ability to detect, respond, and recover from a breach. **Living, breathing document - log of all ongoing IR drills and exercises.**
