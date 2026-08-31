[简体中文](./soc_tiered_guarantee.md)

# OpenHarmony Community SoC Tiered Guarantee Admission Criteria

To ensure the stability of the community master version, control master maintenance costs, and encourage ecosystem diversification and technology exploration, the community classifies SoC support into a four-tier system: T1, T2, T3, and T4. SoCs within the four-tier system are reviewed and dynamically updated by the community PMC.

### Service Standards

| Support Tier | Code Hosting | Gate Check | Daily Build | Automated Testing | Community Recommendation |
| :---: | :---: | :---: | :---: | :---: | :---: |
| T1 | Master | √ | √ | √ | √ |
| T2 | Master | √ | - | - | √ |
| T3 | Branch | √ | - | - | √ |
| T4 | - | - | - | - | √ |

### Support Level

- **T1**: Community master code; gate check triggered on every PR submission; daily full build with continuous integration, smoke testing & full development board testing (performance, stability, etc.); rapid BUG and vulnerability fixes; first release of new features; default official images.
- **T2**: Community master code; T1 gate check triggered on every PR submission; full build at each release; development board smoke testing and full XTS testing; only core features guaranteed; BUGs and vulnerabilities may remain; no official images published.
- **T3**: Community branch code; T3 gate check triggered on every PR submission; selective version adaptation; development board smoke testing and full XTS testing (provided by vendor); full XTS testing; only core features guaranteed.
- **T4**: Code not hosted in the OH community; maintained and published by vendors independently; products have passed OpenHarmony compatibility testing; OH community recommends to developers on a merit basis.

## 1. General Evaluation Dimensions

All SoCs applying for T1/T2 entry are assessed across three major dimensions — technical maturity, ecosystem maturity, and vendor support capability — with scoring applied.

### 1.1 Technical Maturity

- Mass production status, stability, and hardware/software completeness of the chip itself;
- Adaptation degree of drivers, BSP, and peripheral capabilities to the OpenHarmony architecture;
- Power consumption, real-time performance, security, and reliability meeting the requirements of the target device scenarios.

### 1.2 Ecosystem Maturity

- Terminal mass production scale and number of industry deployment cases;
- Completeness of supporting development boards, reference designs, documentation, and toolchains;
- Adoption breadth among downstream hardware vendors, solution providers, and OEMs.

### 1.3 Vendor Support Willingness and Investment

- Dedicated adaptation team staffing and long-term maintenance commitment;
- Timeliness of responding to community issues, fixing BUGs, and following version iterations;
- Activeness in participating in community SIG groups, code contributions, and technical co-development.

## 2. T1 SoC Admission Criteria (Master Preferred)

### 2.1 Quantity Rules

The community master retains only 1 T1 SoC for each of the mini, small, and standard systems respectively; replacement requires PMC-initiated review and public announcement before execution.

### 2.2 Hard Admission Thresholds

**Mass Production and Deployment**

- Chip in large-scale mass production for ≥2 years with no major batch hardware defects;
- Annual shipment volume of terminals using the SoC ranks among the industry leaders, covering mainstream deployment scenarios.

**Technical Adaptation Capability**

- Complete adaptation to OpenHarmony with full BSP, drivers, peripherals, audio/video, graphics, networking, and security deeply adapted, with no functional gaps;
- Stable support for the full set of system APIs, distributed capabilities, AB streaming upgrades, ArkUI, media, and security capabilities.
- Closed-source binary and open-source code quality meeting community standards.

**Supporting Infrastructure**

- Official public development board / reference board continuously available and with stable supply, serving as the community's primary benchmark hardware;
- Complete output of adaptation documentation, development guides, debugging manuals, sample code, and out-of-the-box toolchains.

**Vendor Investment Requirements**

- Establish a dedicated resident community maintenance team for long-term tracking of daily master iterations;
- Commit to following all master version iterations, completing full-feature regression verification for each iteration;
- 7×12 hour response to master-related BUGs and compatibility issues, with fix plans for critical issues within 48 hours;
- Verification environment support.

### 2.3 Verification Requirements

- Participate in daily master builds and continuous integration (CI); every code merge must complete full-feature regression testing;
- Before official version release, complete verification across six dimensions: functionality, performance, stability, compatibility, security, and upgrade;
- Serve as the community benchmark verification hardware; all new master features and architectural changes must undergo basic validation on this SoC.

### 2.4 O&M and Elimination Rules

PMC conducts a semi-annual review. If version iteration lag, prolonged unaddressed BUGs, or team disbandment occurs, a progressive replacement review is initiated; the old and new SoCs undergo parallel verification before a smooth transition is completed.

## 3. T2 SoC Criteria (Master Compatible)

### 3.1 Quantity Rules

Standard system ≤4; mini and small systems ≤1 each. Applications are accepted while slots remain; once full, a "first out, then in" principle applies; new additions / replacements require PMC review and public announcement.

### 3.2 Hard Admission Thresholds

**Mass Production and Deployment**

- Chip officially in mass production for ≥1 year with stable batch supply;
- Possesses scaled commercial use cases with benchmark projects in at least 1 major OpenHarmony deployment industry.

**Technical Adaptation Capability**

- Kernel version matching the target device form factor, with master core components and key peripherals fully adapted;
- Stable operation of core system capabilities: distributed connectivity, basic application framework, security capabilities, AB upgrades, mainstream media and networking functions;
- Master non-core extension components may have adaptation differences, which must be clearly documented in community documentation.
- Closed-source binary and open-source code quality meeting community standards.

**Supporting Infrastructure**

- Provide public development boards / evaluation boards with publicly available specifications and normal procurement availability;
- Output standard BSP, driver packages, basic adaptation documentation, and debugging guides to ensure normal developer usage.

**Vendor Investment Requirements**

- Configure a dedicated maintenance team to align with community version iterations;
- Commit to adaptation maintenance following master official versions, focusing on core feature assurance;
- Issue and compatibility BUG response time: 72 hours for routine issues; critical BUGs fixed within 5 business days;
- Verification environment support: including donating or providing equivalent resources such as infrastructure gate checks and development boards to the community.

### 3.3 Verification Requirements (Master Release Phase)

- No participation in daily full CI regression; complete verification only at version release milestones;
- Key validation: full XTS testing and four modules of the current master version — core features, basic functionality, stability, and upgrade capability;
- Non-core features and edge interfaces are not required to undergo mandatory full-coverage verification; differences are consolidated into the community compatibility notes.

### 3.4 O&M and Elimination Rules

- Quarterly routine evaluation; failure to complete core feature verification for 2 consecutive official versions or prolonged unresolved issues results in direct removal from the T2 list;
- Vacated slots open for a new round of application review.

## 4. T3 SoC Criteria (Community Branch Adaptation, Non-Master)

### 4.1 Positioning and Core Rules

- Not merged into community master code; vendors independently create patch code repositories based on community released versions for adaptation and maintenance;
- Core constraint: Branch SoC capabilities, positioning, and target scenarios must not highly overlap with existing T1/T2 or existing T3 SoCs, to avoid homogeneous adaptation and resource waste; PMC conducts differentiation evaluation.

### 4.2 Basic Admission Requirements

**Compliance and Community Rules**

- Strictly comply with OpenHarmony open-source licenses and community contribution norms; branch code must be open-source and auditable;
- Unified branch naming conventions, indicating vendor, SoC model, and adapted version for easy community identification.

**Differentiation Requirements (Core Red Lines)**

- Clear differentiation in at least one of the following: computing power, manufacturing process, peripheral interfaces, target device form factor, deployment industry, or power consumption level;
- Prohibition of simple replication of mainstream T1/T2 general-purpose SoCs or repeated adaptation of the same form factor and scenario; if PMC review does not approve, the branch will not be created.

**Vendor Responsibility Requirements**

- Patch code repositories are fully maintained by vendors: code iteration, BUG fixes, version synchronization, and issue Q&A are all the vendor's responsibility;
- Required to periodically synchronize with the latest community version (every 2–4 master version cycles) to reduce version fragmentation;
- Publish adaptation notes, usage limitations, and known issues in the corresponding community section for clear developer transparency.

### 4.3 Adaptation and Usage Constraints

- CI setup and full testing assurance; testing and verification work is completed by vendors independently or by donating/providing equivalent resources to the community; the community requires CI results to be publicly viewable.
- Branches serve only as ecosystem supplements and are not included in the official master version release list; master-level compatibility is not guaranteed;
- If the product matures and the ecosystem grows subsequently, meeting T2 admission criteria, reapplication for review and transfer to the T2 master support tier is permitted.

### 4.4 Repository Cleanup Rules

- Repositories with no code updates or maintenance activity for 6 consecutive months will be marked as archived by the community;
- Long-abandoned and unmaintained T3 repositories will be uniformly cleaned up after PMC public announcement.

## 5. T4 SoC Criteria

### 5.1 Positioning and Core Rules

- T4 SoC code is not hosted in the OpenHarmony community; it is maintained and published independently by vendors;
- Based on SoC products passing community XTS compatibility testing and meeting developer evaluation standards, the OpenHarmony community recommends them to developers on a merit basis, but the "OpenHarmony Official Recommendation" brand must not be used; only "OpenHarmony Compatibility Tested" may be indicated.

### 5.2 Basic Admission Requirements

- XTS compatibility testing: Products must pass the OpenHarmony XTS full compatibility test; expired certifications require re-testing.

### 5.3 Management Rules

- The community does not provide any infrastructure including code hosting, CI, builds, or testing environments;
- The community only handles XTS certification review and maintains the developer recommendation list;
- The recommendation list is updated quarterly, removing products that no longer meet the criteria.

## 6. Supplementary General Management Rules (For Implementation)

- **Review Authority**: All T1/T2 applications, replacements, and eliminations, as well as T3 differentiation validation, are led by the community PMC and jointly reviewed with the corresponding SIG group leads.
- **Public Announcement Mechanism**: Each round of applications, list changes, and slot adjustments must be publicly announced on the community official website / mailing list for no less than 7 business days.
- **Dynamic List**: The community maintains a public "SoC Tiered Support List" with real-time updates on T1/T2/T3 models, vendors, adapted versions, and status.
- **Upgrade Path**: T3 branch SoCs meeting T2 criteria may apply for promotion; T2 SoCs with outstanding performance and the highest composite score may participate in T1 replacement review.