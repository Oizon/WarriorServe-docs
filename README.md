## WarriorServe® Package Documentation
WarriorServe® documentation, installation guides, and configuration references for deploying the WarriorServe® platform in Salesforce organizations.

### ⚙️ Overview

WarriorServe is a managed package that facilitates partner coordination, data consistency, and case handling for veteran services. It includes custom objects, trigger handlers, validation logic, and configuration tooling designed for modular deployment across VA service networks.

---
### 🛠️ Installation & Configuration Requirements

Before installing WarriorServe®, complete the following steps to ensure the package deploys and functions correctly.

### Prerequisites (Before Installing the Package)

1. **Enable My Domain**

  - In Salesforce Setup:
    - Go to: `Setup → Company Settings → My Domain`
    (**Ensure you choose a domain you are comfortable making public.**)

2. **Enable Digital Experiences (Experience Cloud)**

  - In Salesforce Setup:
    - Go to: `Setup → Digital Experiences → Settings`
    - Click: **Enable Digital Experiences**

3. **Configure Default External Access (OWD)**

  - In Salesforce Setup
    - Go to: `Setup  → Sharing Settings → Edit
    - **Contact Internal**: Any except `Controlled by Parent` 
    - **Contact External**: `Private`
    - **Case External**: `Private`  

4. **Enable Folders and Enhanced Sharing**
  - In Salesforce Setup:
    - Go to: `Setup → Lightning Email Templates`
    - Toggle On: **Folders and Enhanced Sharing**

4. **Install Nonprofit Success Pack (NPSP)** (Optional)

  Allows multi-phone/email per contact and more Do Not Contact Messaging

### 🚀 Installation

1. **Log Into Org**

  - While logged into org
    - Install `WarriorServe`
    - adjust URL to the following: `https://login.salesforce.com/packaging/installPackage.apexp?p0=XXXXXXXXXXXX`

### 🏛️ Architecture

  - WarriorServe extends core Salesforce objects including:

    - Contact
    - Account
    - Case

Additional custom objects manage referrals, service history, and program metrics.
### 📦 Core Objects

#### `Case Referral` (Custom Object)

A custom object used to manage the referral of cases to partner contacts.

- **CaseRef__c** (Master-Detail -> Case): Links Case Referral to Case for steamlined data association.
- **IsDoNotEmailContact__c** (Checkbox): Indicates we will not send the Case Referral Email when checked.
- **RatingPick__c** (Picklist): This picklist on the rating field ranges from 1 to 5 stars and visually represents the rating using star images.
- **RatingReason__c** (Text): The indicated reason for the selected rating.
- **Name** (Auto Number): The set number of referral in format CR-{YYYY}{MM}{DD}{0}
- **ReferredToAccountRef__c** (Master-Detail -> Account): The account we have made a referral to.
- **ReferredToContactRef__c** (Lookup -> Contact): The individual at the account we are referring to.
- **StarRatingAuto__c** (Formula(Text)): The visual representation of the Rating.

#### `Support Action` (Custom Object)

Stores information about monetary value of a referral //TODO Evaluate merging into case referral.

- **ActionPick__c** (Picklist): The actions taken.
- **ActionDate__c** (Date): Indicates the date the action took place.
- **Amount__c** (Currency): Indicates the value of the Support Action.
- **CaseRef__c** (Lookup -> Case): The Case that received this support action.
- **ContactRef__c** (Master-Detail -> Contact): The contact who received the support action.
- **Description__c** (Text Area): Notes or description of the support action taken.
- **PayorRef__c** (Lookup -> Account): The Account that paid for this action. //TODO Possible Remove, unused in our org.
- **Name** (Auto Number): The set number of referral in format SA-{YYYY}{MM}{DD}{0}
- **SupportActionSupplierRef__c** (Lookup -> Account): The Account that paid for this action.


#### `Case` (Standard Object)

Standard Object for Case Tracking.

- **WorkAndShiftDesiredPick__c** (Multi-Select Picklist): Work and Shift Desired
- **TotalValueOfSupportActionsTrig__c** (Number(18, 0)): Holds the total value of support actions for this case.(why is this a number instead of currency?)
- **TargetDateToBeEmployed__c** (Date): Indicates the individuals desired date to get employment.
- **SSVFStatusPick__c** (Picklist): The current SSVF status of the contact.
- **SSVFHousingCategoryPick__c** (Picklist): The category of SSVF Homelessness.
- **ShiftDesiredPick__c** (Multi-Select Picklist): Indicates the shift the individual desires.
- **ShareWithPick__c** (Multi-Select Picklist): This is used to share cases with Groups. The group name must match what is listed here. (Possible remove due to being complicated)
- **SalaryWagePeriodPick__c** (Picklist): Time Period as applies to Salary/Wage
- **RecordTypeNameAuto__c** (Formula (Text)): Displays the record type name of the case.
- **ProfessionalDesignatorPick__c** (Picklist): The Designation of the individual's profession.
- **ProfessionalCategoryPick__c** (Picklist): The Profession of the individual.
- **IsResumeAttached__c** (Checkbox): Indicates that the individual's resume is attached to this case.
- **IsResumeAssistance__c** (Checkbox): Indicates that the individual requires resume assistance.
- **IsProfessionalMentorship__c** (Checkbox): Identifies that the individual is seeking professional mentorship.
- **IsJobSearch__c** (Checkbox): Warrior need help finding employment.
- **IsHasFelony__c** (Checkbox): Indicates the individual has a Felony conviction.
- **IsCurrentResume__c** (Checkbox): The individual has a current resume.
- **HousingPartnerRef__c** (Lookup -> Account):	Referred to this housing partner. (Duplicative to Case Referral Object)
- **FelonyDescription__c** (Text): The description of a felonious act by the individual.
- **EnrollmentDate__c** (Date): The date enrolled, can be used for different types of enrollment.
- **DesiredSalaryWage__c** (Currency): The desired salary/wage of the individual.
- **DesiredAnnualizedSalary__c** (Currency): 	The desired salary of the individual annualized.
- **DaysOpenAuto__c** (Formula(Number)): The amount of time a case has been or was open.
- **CurrentSalaryWage__c** (Currency): The current Salary/Wage of the Contact.
- **ContactPhoneAuto__c** (Formula(Text)): 	Displays the client's phone number if it's available; otherwise, displays "No Phone Provided"
- **ContactNameAuto__c** (Formula(Text)): Displays the client's full name. If both first and last names are available, it concatenates them; otherwise, it shows whichever part is not blank.
- **ContactEmailAuto__c** (Formula(Text)):	Displays the client's email if it's available; otherwise, displays "No Email Provided"
- **ConditionRatingTrig__c** (Text): Set by automation to display a color for each condition.
- **ConditionAuto__c	** (Formula(Text)): Displays color and name to visually see the condition.
- **CaseCloseReasonPick__c** (Picklist): The reason the case was closed.
- **ServiceCategoryPick__c** (Picklist): The subcategory of the case record type. Used with Condition Rating to show a color rated value.
- **FieldApiName** (FieldType): use
- **FieldApiName** (FieldType): use
- **FieldApiName** (FieldType): use
- **FieldApiName** (FieldType): use

#### `Account` (Standard Object)

Standard Object for Accounts.

- **FieldApiName** (FieldType): use

#### `Contact` (Standard Object)

Standard Object for Contacts.

### `Condition Rating` (Custom Object)

Allows for managing setting colors for cases and severity

### `Education` (Custom object)

Allow for storing information regarding the contacts education status such as schooling attended or certifications completed.

### `Employment` (Custom Object)

Stores information regarding a contacts employment history or current employment.

### `Error` (Custom Object)

Stores infomration regarding errors that may happen during WarriorServe® usage for debugging purposes

### `Event Log` (Custom Object)

Stores information of meaningful changes to the contact record

### `Finance` (Custom Object)

//TODO add definition and finish Finance Object

### `Injury` (Custom Object)

Stores information about injuries sustained by a contact.

### `QOL Assessment` (Custom Object)

Stores a base survey of how a contact feels regarding themselves and their community

### `Service Record` (Custom Object)

Stores information regarding a contacts individual service history

### `Metric` (Custom Object)
Stores an automatically generated snapshot of how your organization is doing using predefined context

A snapshot overview of how your organization has done serving their community.
//TODO finish Metric and ensure it is visible and being schedule popualted.

##### Validation Rules:

* **VR01\_CRE\_ValidEmailRequiredForContacts:** Ensures the referred contact has a valid email.
* **VR02\_CRE\_ContactConsentMissing:** Requires consent to share information on the contact record.
* **VR03\_CRE\_ContactMustBeFromTheAccount:** Prevents referring contacts who are not part of the case's account.
* **VR04\_CRE\_PreventDoNotEmailChanges:** Prevents changing the Do Not Email Fields after creation.
* **VR01\_CON\_FirstNameRequired:** Prevents saving a contact record if they do not have a first name.
* **VR02\_CON\_DisallowNeedsChangeAfterIntake:** Prevents changing the intial needs after the first day of the contact being created.
* **VR01\_SER\_ValidateEnlistDate:** Prevents creating a service record where someone is listed as under 15 years old upon service starting.
* **VR02\_SER\_ActiveWithServiceEndDate:** Prevents end date if service says there should be one yet.
* **VR03\_SER\_EndDateLaterThanStartDate:** Prevents a service record where they end before starting.
* **VR04\_SER\_NotActiveNoEndDate:** Presents saving a service record not active without an end date.

##### Trigger Handler:

`CaseReferralTriggerHandler` manages logic during record inserts/updates for this object, enforcing referential integrity and business rules.

---

### 🎯 Trigger Handlers

#### `CaseReferralTriggerHandler`

Handles `BEFORE INSERT/UPDATE` logic for `CaseReferral__c` to enforce validation rules, contact-account relationships, and email/consent requirements.

#### `ConditionRatingTriggerHandler`

*Background object used for defining the color-coded severity levels of cases.*

Handles `BEFORE INSERT` logic for `ConditionRating__c`, ensuring alignment with `Case.Type` values and preventing duplication.

**Key Behaviors:**

* **Duplicate detection (case-insensitive):**

  * Blocks insert if the `Name` already exists in the database (either via Apex or standard Duplicate Rules).
  * Blocks duplicate `Name` values within the same insert transaction.
* **Validation against `Case.Type` picklist:**

  * Ensures `ConditionRating__c.Name` matches a valid `Case.Type` value (case-insensitive).
  * Uses dynamic schema metadata to validate.
* **Fallback Enforcement:**

  * If the Duplicate Rule is disabled or bypassed, Apex logic still prevents duplicates and informs the user to reactivate the rule.

**Future Configuration:**

* These `ConditionRating__c` records will eventually be **configurable via the WarriorServe Settings page/app**, allowing administrators to manage them declaratively.

**Test Coverage Includes:**

* Case-insensitive name comparisons
* Picklist alignment
* Duplicate detection in-flight and against the DB
* Safe handling if standard rules are bypassed

---

### 🛠️ Settings Management

WarriorServe® includes **modular settings components** to configure system behavior:

#### **Basic Settings**

* Configured via a dedicated Lightning Web Component (`basicSettingsManager`).
* Includes core enablement flags, such as:

  * Enable WarriorServe®
  * Enable Case Auto Create
  * Enable Event Logging
  * Enable Task Auto Create
* When **Enable WarriorServe** is unchecked, all other basic settings are automatically disabled in the UI.
* Changes are saved independently and do not impact Advanced Settings.

#### **Advanced Settings**

* Configured via the `advancedSettingsManager` Lightning Web Component.
* Includes specialized controls such as:

  * Enable Veteran Confirmation
  * Batch processing limits
  * VA Facility retrieval options
  * Case Referral Auto Sharing
* **Acknowledgment Required:**

  * Users must confirm a warning prompt before accessing advanced controls.
* When **Enable WarriorServe** is unchecked, all advanced settings are disabled.
* Changes are saved independently of Basic Settings.

**Future Configuration Plans:**

* A unified **WarriorServe® Settings Home page** is being developed to centralize access to all settings components and related walkthrough documentation.
* Additional configuration for `ConditionRating__c` records and error logging visibility will be surfaced through this page.

---

More features and configuration options will be appended as additional parts of the WarriorServe system are documented and implemented.

---

### ✅ Supported Package Components

- Applications
  - WarriorServe
  - WarriorServe Settings and Tools
- Permission Sets
  - WarriorServe Administrator
  - WarriorServe User
- Custom Metadata
  - WarriorServeAPISettings (VAFacilitiesAPI, Veteran_Confirmation_API)
- Remote Site Settings
  - VeteransAffairsAPI
- Tabs
  - Settings Home
  - Condition Rating
  - Error
  - Metric
- Flexipages
  - Home_Page_Default
  - SettingsHome
  - WarriorServeContactPage
  - Case_Record_Page
  - Service_Record_Record_Page
  - Education_Record_Page
  - Employment_Record_Page
  - Injury_Record_Page
  - Support_Action_Record_Page
  - WarriorServe_UtilityBar
  - WarriorServe_Settings_And_Tools_UtilityBar
- Flows
  - Record_Trigger_Service_Record_Before_Save
  - Schedule_Trigger_Partner_Rating
  - Screen_Flow_HUD_Homeless
- LWCs
  - basicSettingManager
  - advancedSettingsManager
  - aboutSettingManager
  - contactDataIntegrity
  - contactQuickView
  - contactTimeline
  - nearbyVAFacilitiesMap
- Apex (Core)
  - CaseTriggerHandler, ContactTriggerHandler, CaseReferralTriggerHandler, ConditionRatingTriggerHandler, SupportActionTriggerHandler
  - VAFacilitiesService, VeteranConfirmationStatus, EventLogUtility, HandleException, MetricsGenerator, SettingsManagerController, CollectionUtils, PostInstall
- Apex (Test/Mocks)
  - Comprehensive test classes and HttpCalloutMock implementations

---

### 🔐 Permission Sets

Assign these to users after install:

- WarriorServe Administrator
  - Full access to Settings Home and related tabs (Settings Home, Error, Metric, Condition Rating)
  - Manage Basic/Advanced Settings components
  - Required CRUD/FLS on custom objects used by configuration
- WarriorServe User
  - Operational access for case workers
  - Access to Contact/Case and related custom objects needed by automations (ServiceRecord__c, CaseReferral__c, SupportAction__c, etc.)
  - Visibility for LWCs embedded on Lightning pages (Quick View, Timeline, Data Integrity)

Note: Validate OWD and Profile tab visibility so utility bars and record pages appear as intended.

---

### 🌐 External Integrations

- Remote Site Settings
  - VeteransAffairsAPI — must be enabled to allow outbound VA callouts
- Custom Metadata: WarriorServeAPISettings
  - VAFacilitiesAPI — endpoint/key config for VA Facilities search
  - Veteran_Confirmation_API — endpoint/key config for veteran status confirmation

Update these records post-install before enabling related features in Advanced Settings.

---

### 🧩 Lightning Pages & Utility Bars

- Utility Bars
  - WarriorServe_UtilityBar — end-user quick tools
  - WarriorServe_Settings_And_Tools_UtilityBar — admin tools
- Record Pages
  - Case_Record_Page, WarriorServeContactPage, Service_Record_Record_Page
  - Education/Employment/Injury record pages
- SettingsHome
  - Central landing area for Settings LWCs and admin guidance

After install, assign these pages/utility bars to the appropriate Apps and Profiles.

---

### ⚡️ Flows

- Record_Trigger_Service_Record_Before_Save
  - Validates/normalizes ServiceRecord__c data prior to DML
- Schedule_Trigger_Partner_Rating
  - Scheduled maintenance for partner ratings (ensure schedule activation post-deploy)
- Screen_Flow_HUD_Homeless
  - Guided HUD Homelessness intake; grant Flow access to case worker profiles

---

### 🧠 Lightning Web Components (LWC)

- basicSettingManager
  - Toggles: Enable WarriorServe, Case Auto Create, Event Logging, Task Auto Create
  - Disables dependent toggles when WarriorServe is off
- advancedSettingsManager
  - Veteran Confirmation, VA Facility retrieval options, batch/scheduler limits, auto-sharing
  - Requires user acknowledgement prior to edits
- aboutSettingManager
  - Contextual info about features and configuration
- contactDataIntegrity
  - Scores Contact completeness and lists missing critical fields
- contactQuickView
  - Compact roll-up (Contact highlights + related lists such as Service Records and Education)
- contactTimeline
  - EventLogUtility-backed timeline of significant Contact events
- nearbyVAFacilitiesMap
  - Map of VA facilities near Contact mailing address (requires VA integration enabled)

Add these components to Lightning pages using App Builder as shown in the Flexipage section.

---

### 🎯 Trigger Handlers (Summary)

- CaseTriggerHandler
  - Maintains computed fields/rollups, schedules post-insert processing where applicable
  - Skips logic based on org-level settings (WarriorServeSettings__c)
- ContactTriggerHandler
  - Contact lifecycle automation (e.g., HUD task creation, related case orchestration)
  - Honors settings flags to minimize side effects
- CaseReferralTriggerHandler
  - Referential integrity and consent/email checks for CaseReferral__c
- ConditionRatingTriggerHandler
  - Enforces uniqueness (case-insensitive) and alignment to Case.Type values
  - Works even if duplicate rules are disabled
- SupportActionTriggerHandler
  - Keeps Case rollups in sync with SupportAction__c transactions

All handlers are bulkified and tested. See individual Test classes for scenarios and assertions.

---

### 🧰 Services & Utilities

- VAFacilitiesService (Queueable, callouts)
  - Queries nearby VA facilities for a Contact location
  - Mockable for tests (VAFacilitiesServiceMock)
- VeteranConfirmationStatus (Queueable, callouts)
  - Verifies veteran status via external API
  - Mockable for tests (VeteranConfirmationStatusMock)
- EventLogUtility
  - Creates/reads EventLog__c entries for Contact timelines and auditing
- HandleException
  - Centralized error capture with support for synchronous and async contexts
- MetricsGenerator (Schedulable)
  - Periodic snapshot into Metric__c for org health KPIs
- SettingsManagerController (AuraEnabled)
  - Backing controller for Settings LWCs
- CollectionUtils
  - Common collection helpers used across triggers/services
- PostInstall (InstallHandler)
  - Post-install initialization and data seeding hook

---

### 🧪 Testing

- Unit tests per handler/service with mock callouts where required
- Example scenarios:
  - Duplicate detection and picklist validation (ConditionRating)
  - Contact lifecycle (insert/update; HUD task; record-derived toggles)
  - Case rollup recalculations and skip logic
  - External integrations (VA Facilities, Veteran Confirmation) via HttpCalloutMock

Run all tests:
- From VS Code: Apex Tests view
- From CLI: sf apex run test --code-coverage --wait 10

---

### 📦 Deployment & Setup (Scratch Orgs)

1) Prerequisites
- My Domain enabled
- Digital Experiences enabled
- OWD (External) — Contact (Private), Case (Private), adjust “Contact Internal” (not “Controlled by Parent”)

2) Create Scratch Org
- sf org create scratch -f config/project-scratch-def.json -a WarriorServe -d 7

3) Deploy Source and Assign Permissions
- sf project deploy start -d force-app
- sf org assign permset --name WarriorServeAdministrator
- sf org assign permset --name WarriorServeUser

4) Post-Deploy Configuration
- Remote Site: enable VeteransAffairsAPI
- Custom Metadata: populate WarriorServeAPISettings for VA endpoints/keys
- Pages: set app default pages and utility bars
- Flows: activate/schedule Schedule_Trigger_Partner_Rating if required

5) Open Org
- sf org open

---

### 🔎 Admin Scripts

Use the included Apex scripts for quick setup/testing:

- scripts/apex/setDefaultConditions.apex
  - Seeds ConditionRating__c defaults
- scripts/apex/runVAFacilitiesServices.apex
  - Exercises VAFacilitiesService for a sample Contact
- scripts/apex/hello.apex, scripts/apex/test.apex
  - Sanity checks for org/package readiness
- scripts/soql/account.soql
  - Convenience query for Account data checks

Execute:
- sf apex run --file scripts/apex/setDefaultConditions.apex

---

### 🧭 Known Gaps / TODOs

- SupportAction__c: evaluate merging into Case Referral or clarify data model separations
- Finance__c: finalize definition, fields, and documentation
- Metric generation: verify visibility and production scheduling
- Case vs CaseReferral__c field duplication: rationalize fields such as HousingPartnerRef__c

---

#### Suggestions for NPSP

* Add to Contact Dynamic Form page WarriorServeContactPage 
  * npsp__Deceased__c
  * preferred phone
  * preferred email
  * workphone
  * do not contact
  * personal email
  * work email
  * alt email
  * household address
  * Private
  * Related List Relationships

* Above shoiuld also go on relavent page layouts

* Permissions on WarriorServe User
  * Account Household Record Type
  * Account Organization Record Type
---
