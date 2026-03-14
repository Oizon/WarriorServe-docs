# WarriorServe-docs
WarriorServe® documentation, installation guides, and configuration references for deploying the WarriorServe platform in Salesforce organizations.

## WarriorServe Package Documentation

### ⚙️ Overview

WarriorServe is a managed package that facilitates partner coordination, data consistency, and case handling for veteran services. It includes custom objects, trigger handlers, validation logic, and configuration tooling designed for modular deployment across VA service networks.

---
### 🛠️ Installation & Configuration Requirements

Before installing WarriorServe, complete the following steps to ensure the package deploys and functions correctly.

### Prerequisites (Before Installing the Package)

1. **Enable My Domain**

  - In Salesforce Setup:
    - Go to: `Setup → Company Settings → My Domain`
    (**Ensure they choose one they are happy being public**)

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

4. **Install Nonprofit Success Pack (NPSP)** (Optional)

  Allows multi-phone/email per contact and more Do Not Contact Messaging

### 🚀 Installation

1. **Log Into Org**

  - While logged into org
    - Install `WarriorServe API`
    - adjust URL to the following: `{Domain} + /packaging/installPackage.apexp?p0= + {packageId}`
    - Once completed Install `WarriorServe Core` in the same manner

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

Allows for managing setting colors for cases and severuity

### `Education` (Custom object)

Allow for storing information regarding the contacts education status such as schooling attented or certifications completed.

### `Employment` (Custom Object)

Stores information regarding a contacts employment history or current employment.

### `Error` (Custom Object)

Stores infomration regarding errors that may happen during WarriorServe usage for debugging purposes

### `Event Log` (Custom Object)

Stores information of meaningful changes to the contact record

### `Finance` (Custom Object)

//TODO add definition and finish Finance Object

### `Injury` (Custom Object)

Stores information about injuries sustained by a contact.

### `QOL Assessment` (Custom Object)

Stores a base survey of how a contact feels regarding themselves and their community

### `Service Record` (Custom Object)

Stores informaiton regarding a contacts individual service history

### `Metric` (Custom Object)
Stores an automatically generated snapshot of how your organziation is doing using predefined context

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

WarriorServe includes **modular settings components** to configure system behavior:

#### **Basic Settings**

* Configured via a dedicated Lightning Web Component (`basicSettingsManager`).
* Includes core enablement flags, such as:

  * Enable WarriorServe
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

* A unified **WarriorServe Settings Home page** is being developed to centralize access to all settings components and related walkthrough documentation.
* Additional configuration for `ConditionRating__c` records and error logging visibility will be surfaced through this page.

---

More features and configuration options will be appended as additional parts of the WarriorServe system are documented and implemented.

---
#### **Update from Old WarriorServe Field Mapping**

* Suggest downloading objects directly and reuploading with a service like Salesforce Inspector after changing headers to new fields
* For the same object only update, for different/new objects insert new and remove/hide old. 

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