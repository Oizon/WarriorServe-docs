# 📦 Core Objects

## Table Of Contents
- [Account](#account-standard-object)
- [Case](#case-standard-object)
- [Case Referral](#case-referral-custom-object)
- [Condition Rating](#condition-rating-custom-object)
- [Contact](#contact-standard-object)
- [Error Event](#error-event-custom-object---platform-event)
- [Error](#error-custom-object)
- [Event Log Field](#event-log-field-custom-metadata)
- [Event Log](#event-log-custom-object)
- [Metric](#metric-custom-object)
- [Service Record](#service-record-custom-object)
- [Support Action](#support-action-custom-object)
- [User](#user-standard-object)

## `Account` (Standard Object)

Standard Object for Accounts.

- **Company Facebook** (`WarriorSrv__CompanyFacebook__c`) - *URL*: The link to the account's Facebook account.
- **Company Instagram** (`WarriorSrv__CompanyInstagram__c`) - *URL*: The link to the account's Instagram account. 
- **Company LinkedIn** (`WarriorSrv__CompanyLinkedIn__c`) - *URL*: The link to the account's LinkedIn account.
- **Company X** (`WarriorSrv__CompanyX__c`) - *URL*: The link to the account's X account.
- **Eligibility Criteria** (`WarriorSrv__EligibilityCriteria__c`) - *Text*: Captures the specific requirements individuals must meet to qualify for services.
- **Basic Needs** (`WarriorSrv__IsBasicNeedsPartner__c`) - *Checkbox*: Indicates the account is a Basic Needs partner.
- **Benefits/VSO** (`WarriorSrv__IsBenefitsVSOPartner__c`) - *Checkbox*: Indicates the account is a Benefits/VSO Partner
- **Caregiver Support** (`WarriorSrv__IsCaregiverSupportPartner__c`) - *Checkbox*: Indicates the account is a Caregiver Support Partner
- **Education** (`WarriorSrv__IsEducationPartner__c`) - *Checkbox*: Indicates the account is a Education Partner.
- **Family Support** (`WarriorSrv__IsFamilySupportPartner__c`) - *Checkbox*: Indicates the account assist with Family Support. 
- **Funding** (`WarriorSrv__IsFundingPartner__c`) - *Checkbox*: Indicates the account is a Funding Partner.
- **Housing** (`WarriorSrv__IsHousingPartner__c`) - *Checkbox*: Indicates the account is a Housing Partner.
- **Job Placement** (`WarriorSrv__IsJobPlacementPartner__c`) - *Checkbox*: Indicates the account is a Job Placement Partner.
- **Legal** (`WarriorSrv__IsLegalPartner__c`) - *Checkbox*: Indicates the account is a Legal Partner.
- **Long Term Financial** (`WarriorSrv__IsLongTermFinancialPartner__c`) - *Checkbox*: Indicates the account is a Long Term Financial Partner.
- **Medical Devices** (`WarriorSrv__IsMedicalDevicesPartner__c`) - *Checkbox*: Indicates the account is a Medical Devices Partner.
- **Mental Health** (`WarriorSrv__IsMentalHealthPartner__c`) - *Checkbox*: Indicates the account is a Mental Health Partner.
- **Peer Support** (`WarriorSrv__IsPeerSupportPartner__c`) - *Checkbox*: Indicates the account is a Peer Support Partner.
- **Physical Health** (`WarriorSrv__IsPhysicalHealthPartner__c`) - *Checkbox*: Indicates the account is a Physical Health Partner.
- **Recreation** (`WarriorSrv__IsRecreationPartner__c`) - *Checkbox*: Indicates the account is a Recreation Partner.
- **Short Term Financial** (`WarriorSrv__IsShortTermFinancialPartner__c`) - *Checkbox*: Indicates the account is a Short Term Financial Partner.
- **Spirituality** (`WarriorSrv__IsSpiritualityPartner__c`) - *Checkbox*: Indicates the account is a Spirituality Partner.
- **Technology** (`WarriorSrv__IsTechnologyPartner__c`) - *Checkbox*: Indicates the account is a Technology Partner.
- **Transportation** (`WarriorSrv__IsTransportationPartner__c`) - *Checkbox*: Indicates the account is a Transportation Partner.
- **Volunteer Opportunities** (`WarriorSrv__IsVolunteerOpportunitiesPartner__c`) - *Checkbox*: Indicates the account is Volunteer Partner.
- **Partner Account Star Rating** (`WarriorSrv__PartnerStarRatingAuto__c`) - *Formula(TEXT)*: Visual representation of the Partner Score.
- **Partner Rating** (`WarriorSrv__PartnerRatingPickTrig__c`) - *Picklist*: Partner score filled in only by automation from Case Referrals.
- **Referral Count** (`WarriorSrv__ReferralCountTrig__c`) - *Number*: The count of Case Referrals only filled by automation.
- **Referral Type** (`WarriorSrv__ReferralTypePick__c`) - *Picklist*: Indicates the type of referral required or accepted by the organization.
- **Service Coverage** (`WarriorSrv__ServiceCoveragePick__c`) - *Picklist*: Indicates the geographic scope of services provided by the organization, specifying whether they serve local or national clients. This helps categorize organizations based on their service area for accurate referral and resource matching.
- **Service Description** (`WarriorSrv__ServiceDescription__c`) - *Text*: Describes the services provided by the organization.
- **VA Facility External Id** (`WarriorSrv__VAFacilityExternalId__c`) - *Text*: This field stores the external identifier linking this Salesforce account to the corresponding VA Facility system record. It facilitates integration and data synchronization between Salesforce and the VA Facility system.

- [Return to Top](#table-of-contents)

## `Case` (Standard Object)

Standard Object for Case Tracking.

- **Case Close Reason** (`WarriorSrv__CaseCloseReasonPick__c`) — *Picklist*: The reason the case was closed.
- **Condition** (`WarriorSrv__ConditionAuto__c`) - *Formula(Text)*: Displays color and name to visually see the condition.
- **Condition Rating** (`WarriorSrv__ConditionRatingTrig__c`) - *Formula(Text)*: Set by automation to display a color for each condition.
- **Contact Email** (`WarriorSrv__ContactEmailAuto__c`) - *Formula(Text)*:	Displays the client's email if it's available; otherwise, displays "No Email Provided". Used in Case Referral Automations.
- **Contact Name** (`WarriorSrv__ContactNameAuto__c`) - *Formula(Text)*: Displays the client's full name. If both first and last names are available, it concatenates them; otherwise, it shows whichever part is not blank. Used in Case Referral Automations.
- **Contact Phone** (`WarriorSrv__ContactPhoneAuto__c`) - *Formula(Text)*: 	Displays the client's phone number if it's available; otherwise, displays "No Phone Provided"
- **Current Salary/Wage** (`WarriorSrv__CurrentSalaryWage__c`) - *Currency*: The current Salary/Wage of the Contact.
- **Days Open** (`WarriorSrv__DaysOpenAuto__c`) - *Formula(Number)*: The amount of time a case has been or was open.
- **Desired Annualized Salary** (`WarriorSrv__DesiredAnnualizedSalary__c`) - *Currency*: 	The desired salary of the individual annualized.
- **Desired Salary Wage** (`WarriorSrv__DesiredSalaryWage__c`) - *Currency*: The desired salary/wage of the individual.
- **Has Current Resume** (`WarriorSrv__IsCurrentResume__c`) - *Checkbox*: The individual has a current resume.
- **Resume Attached** (`WarriorSrv__IsResumeAttached__c`) - *Checkbox*: Indicates that the individual's resume is attached to this case.
- **Professional Category** (`WarriorSrv__ProfessionalCategoryPick__c`) - *Picklist*: The Profession of the individual.
- **Professional Designator** (`WarriorSrv__ProfessionalDesignatorPick__c`) - *Picklist*: The Designation of the individual's profession.
- **Record Type Name** (`WarriorSrv__RecordTypeNameAuto__c`) — *Formula(Text)*: Displays the record type name of the case. Used in Case Referral Automations.
- **Salary/Wage Period** (`WarriorSrv__SalaryWagePeriodPick__c`) - *Picklist*: Time Period as applies to Salary/Wage
- **Service Category** (`WarriorSrv__ServiceCategoryPick__c`) - *Picklist*: The subcategory of the case record type. Used with Condition Rating to show a color
- **Shift Desired** (`WarriorSrv__ShiftDesiredPick__c`) - *Multi-Select Picklist*: Indicates the shift the individual desires.
- **Target Date To Be Employed** (`WarriorSrv__TargetDateToBeEmployed__c`) - *Date*: Indicates the individuals desired date to get employment.
- **Total Value Of Support Actions** (`WarriorSrv__TotalValueOfSupportActionsTrig__c`) - *Currency*: Holds the total value of support actions for this case.
- **Work And Shift Desired** (`WarriorSrv__WorkAndShiftDesiredPick__c`) - *Multi-Select Picklist*: Work and Shift Desired

- [Return to Top](#table-of-contents)

## `Case Referral` (Custom Object)

Stores data to manage case referrals to partners.

- **Case** (`WarriorSrv__CaseRef__c`) — *Master-Detail -> Case*: Links Case Referral to Case for streamlined data association.
- **Do Not Email Contact** (`WarriorSrv__IsDoNotEmailContact__c`) — *Checkbox*: Indicates we will not send the Case Referral Email when checked.
- **Rating** (`WarriorSrv__RatingPick__c`) — *Picklist*: This picklist on the rating field ranges from 1 to 5 stars and visually represents the rating using star images.
- **Rating Auto** (`WarriorSrv__RatingAuto__c`) — *Formula(Number)*: Numerical version of the rating for easier calculations.
- **Rating Reason** (`WarriorSrv__RatingReason__c`) — *Text*: The Indicates reason for the selected rating.
- **Referral Number** (`Name`) — *Auto Number*: The unique number for this record. 
- **Referred To Account** (`WarriorSrv__ReferredToAccountRef__c`) — *Master-Detail -> Account*: The account we have made a referral to.
- **Referred To Contact** (`WarriorSrv__ReferredToContactRef__c`) — *Lookup -> Contact*: The individual at the account we are referring to.
- **Star Rating** (`WarriorSrv__StarRatingAuto__c`) — *Formula(Text)*: The visual representation of the Rating.

- [Return to Top](#table-of-contents)

## `Condition Rating` (Custom Object)

Defines standardized severity levels with unique names and color codes for classifying and prioritizing cases in WarriorServe.

- **Rating** (`WarriorSrv__RatingPick__c`) — *Picklist*: This is used to assign a color to a rating. All non specified ratings will default to Green.
- **Type API Name** (`Name`) — *Text(80)*: The exact API name that should be checked as on the Case field `ServiceCategoryPick__c`.

- [Return to Top](#table-of-contents)

## `Contact` (Standard Object)
 
Standard Object for contact's.

- **Age** (`WarriorSrv__AgeAuto__c`) — *Formula(Number)*: The contact's current age.
- **Caregiver Type** (`WarriorSrv__CaregiverTypePick__c`) — *Picklist*: Classifies the contact’s caregiver role and population served. Used to standardize reporting, segmentation, and program eligibility.
- **Closed Cases** (`WarriorSrv__ClosedCasesTrig__c`) — *Number*: Indicates the number of closed cases for the contact.
- **Condition Rating** (`WarriorSrv__ConditionRatingAuto__c`) — *Formula(Text)*: Indicates the contact's condition based on their current open cases.
- **Consent to Share Information** (`WarriorSrv__ConsentStatusPick__c`) — *Picklist*: Indicates the individual’s consent status for sharing their information with approved partner organizations for coordination of services. This field should reflect the most current consent decision and is used to control data sharing and integrations.
- **Current Living Situation** (`WarriorSrv__CurrentLivingConditionPick__c`) — *Picklist*: The contact’s current housing or living situation at the time the information is collected. Use this field to record where the contact is presently staying, such as rented housing, temporary shelter, institutional housing, or other current living arrangements.
- **Deceased Date** (`WarriorSrv__DeceasedDate__c`) — *Date*: The date the contact was determined deceased.
- **Disability Percentage** (`WarriorSrv__DisabilityPercentagePick__c`) — *Picklist*: Contact VA Disability rating.
- **Eligible for Tricare** (`WarriorSrv__EligibleForTricarePick__c`) — *Picklist*: Indicates whether the contact is eligible for TRICARE benefits based on known or provided information at the time. Use this field to capture confirmed, unconfirmed, or unknown eligibility status to support service eligibility and referral decisions.
- **Eligible for VA Healthcare** (`WarriorSrv__EligibleForVAHealthcarePick__c`) — *Picklist*: Indicates whether the contact is eligible for VA Healthcare benefits based on known or provided information at the time. Use this field to capture confirmed, unconfirmed, or unknown eligibility status to support service eligibility and referral decisions.
- **Employment Status** (`WarriorSrv__EmploymentStatusPick__c`) — *Picklist*: Indicates a contact's current employment status.
- **Employment Type** (`WarriorSrv__EmploymentTypePick__c`) — *Picklist*: Indicates the contact's type of employment.
- **Enrolled in Civilian Healthcare** (`WarriorSrv__EnrolledInCivilianHealthcarePick__c`) — *Picklist*: Indicates a contact's current Civilian Healthcare status.
- **Enrolled in Healthcare** (`WarriorSrv__EnrolledInHealthcareAuto__c`) — *Formula(Checkbox)*: Evaluates whether the individual is currently enrolled in any healthcare program.
- **Enrolled in Tricare** (`WarriorSrv__EnrolledInTricarePick__c`) — *Picklist*: The contact's Tricare enrollment status.
- **Enrolled in VA Benefits Portal** (`WarriorSrv__EnrolledInVABenefitsPortalPick__c`) — *Picklist*: Indicates the contact's VA Benefits Portal status.
- **Enrolled in VA Healthcare** (`WarriorSrv__EnrolledInVAHealthcarePick__c`) — *Picklist*: The contact's VA Healthcare enrollment status.
- **Family Member Type** (`WarriorSrv__FamilyMemberTypePick__c`) - *Picklist*: Identifies the relationship of the individual to the service member or Veteran when the participant is classified as a Family Member. This field supports intake classification, reporting, and service delivery segmentation. This field should only be populated when Participant Type is “Family Member.”
- **Has Service-Connected Injury** (`WarriorSrv__HasServiceConnectedInjuryPick__c`) — *Picklist*: Indicates the contact's service-connected injury status.
- **Highest Level Of Education** (`WarriorSrv__HighestLevelOfEducationPick__c`) - *Picklist*: Indicates the contact's highest level of education.
- **Hispanic Or Latino Ethnicity** (`WarriorSrv__HispanicOrLatinoEthnicityPick__c`) - *Picklist*: Indicates the contact identifies as Hispanic or Latino.
- **Home Location Type** (`WarriorSrv__HomeLocationTypePick__c`) — *Picklist*: Classifies the individual’s home location as urban, suburban, or rural for reporting purposes.
- **Interest** (`WarriorSrv__InterestsPick__c`) — *Picklist (Multi-Select)*: The contact's interest.
- **Has Valid Drivers License** (`WarriorSrv__IsHasValidDriversLicense__c`) — *Checkbox*: Indicates the contact has a valid driver's license.
- **Recheck Title 38** (`WarriorSrv__IsRecheckTitle38__c`) - *Checkbox*: When selected, requests a new Title 38 verification attempt for the contact. This should only be used when a new verification is needed. The contact must contain, at minimum, the fields required by the Data Integrity component for verification, excluding Email and Phone. This field is intended to trigger a recheck and should be cleared by automation after processing.
- **Last Four SSN** (`WarriorSrv__LastFourSSN__c`) — *Number(4,0)*: The last four digits of the contact's social security number.
- **Lead Source Organization** (`WarriorSrv__LeadSourceOrganizationRef__c`) — *Lookup(Account)*: The specific organization associated with the selected Lead Source when known. Use this field to identify the partner, agency, or organization connected to how the contact was acquired or referred.
- **Mailing County** (`WarriorSrv__MailingCounty__c`) — *Text(30)*: The mailing county of the contact.
- **Marital Status** (`WarriorSrv__MaritalStatusPick__c`) — *Picklist*: Indicates the current known marital status of the contact.
- **Mode of Transportation** (`WarriorSrv__ModeOfTransportationPick__c`) — *Picklist*: Indicates the contact's primary mode of transportation.
- **Number of Children** (`WarriorSrv__NumberOfChildren__c`) — *Number(2,0)*: Indicates the contact's current number of children under 18.
- **Number of Household Members** (`WarriorSrv__NumberOfHouseholdMembers__c`) — *Number(3,0)*: Indicates the number of people in the contact's household.
- **Open Cases** (`WarriorSrv__OpenCasesTrig__c`) — *Number(18,0)*: Indicates the number of open cases on the contact.
- **Open Orange Cases** (`WarriorSrv__OpenOrangeCasesTrig__c`) — *Number(18,0)*: Indicates the number of Open Orange Cases for the contact.
- **Open Red Cases** (`WarriorSrv__OpenRedCasesTrig__c`) — *Number(18,0)*: The count of open red cases.
- **Open Yellow Cases** (`WarriorSrv__OpenYellowCasesTrig__c`) — *Number(18,0)*: The count of open yellow cases.
- **Preferred Method of Contact** (`WarriorSrv__PreferredMethodOfContactPick__c`) — *Picklist*: Indicates the contact's preferred way to be contacted.
- **Race** (`WarriorSrv__RacePick__c`) — *Picklist (Multi-Select)*: Indicates the racial identity of the contact.
- **Record Age** (`WarriorSrv__RecordAgeAuto__c`) — *Formula(Number)*: Indicates the age of the contact in days.
- **Record Type Name** (`WarriorSrv__RecordTypeNameAuto__c`) — *Formula(Text)*: Displays the record type by name, used in some formulas and integrations.
- **Service Record Count** (`WarriorSrv__ServiceRecordCountAuto__c`) — *Roll-Up Summary*: Number of Service Records Entered on the contact.
- **Special Handling** (`WarriorSrv__SpecialHandlingPick__c`) — *Picklist (Multi-Select)*: Indicates information that might be needed when speaking with this contact.
- **Title 38 Verification Status** (`WarriorSrv__Title38VerificationStatusPick__c`) — *Picklist*: Displays the result returned directly from VA systems during Title 38 verification. All values, including errors, originate from the VA and are not determined by WarriorServe. Some results may require action by the VA or the Veteran, not internal staff.
https://www.govinfo.gov/content/pkg/CPRT-112HPRT65875/pdf/CPRT-112HPRT65875.pdf
- **Total Value Of Support Actions** (`WarriorSrv__TotalValueOfSupportActionsAuto__c`) — *Roll-Up Summary*: Automatically stores the total of support actions where this contact was Indicates.
- **WWP® Alumni Enrollment Status** (`WarriorSrv__WWPAlumniEnrollmentStatusPick__c`) — *Picklist*: Indicates the contact's WWP enrollment status.
- **WWP® Decline Reason** (`WarriorSrv__WWPDeclineReasonPick__c`) — *Picklist*: Indicates the reasoning the contact declined WWP enrollment.
- **WWP® Family Support Enrollment Status** (`WarriorSrv__WWPFamilySupportEnrollmentStatusPick__c`) — *Picklist*: Indicates the WWP Family Support enrollment status of the contact.

- [Return to Top](#table-of-contents)

## `Error Event` (Custom Object - Platform Event)

Stores information regarding errors that may happen during WarriorServe® usage for debugging purposes and sends it to the Error object for storing.

- **Automation Name** (`WarriorSrv__AutomationName__c`) — *Text(255)*: The name of the automation, process, flow, trigger, batch, queueable, or other system logic associated with the logged error.
- **Error Number** (`Name`) — *Auto Number*: A system-generated unique identifier for each error record, used for tracking, referencing, and support. Format: {000000}
- **Exception Message** (`WarriorSrv__ExceptionMessage__c`) — *Long Text Area*: The raw exception message captured from the automation at the time of failure (e.g., `Exception.getMessage()`), used for debugging and error analysis.
- **Exception Type** (`WarriorSrv__ExceptionType__c`) — *Text(255)*: The system exception type associated with the error (e.g., NullPointerException, DmlException, CalloutException), used to categorize and analyze failures.
- **Gov Limit in Executing Code** (`WarriorSrv__GovLimitInExecutingCode__c`) — *Long Text Area*: A snapshot of Salesforce governor limit usage at the time the error occurred (e.g., SOQL queries, DML statements, CPU time, heap size), used for debugging limit-related failures.
- **Line Number** (`WarriorSrv__LineNumber__c`) — *Number(18,0)*: The line number in the executing Apex code where the exception was thrown, used to help identify the source of the error.
- **Method Name** (`WarriorSrv__MethodName__c`) — *Text(255)*: The method name in the executing Apex code where the exception was thrown.
- **Related To Id** (`WarriorSrv__RelatedToId__c`) — *Text(255)*: The Salesforce record Id associated with the error at the time it was logged. Populated automatically to identify the record being processed when the failure occurred.
- **Stack Trace** (`WarriorSrv__StackTrace__c`) — *Long Text Area*: The full Apex stack trace captured at the time of the exception (e.g., Exception.getStackTraceString()), used to identify the execution path and source of the error.

- [Return to Top](#table-of-contents)


## `Error` (Custom Object)

Stores information regarding errors that may happen during WarriorServe® usage for debugging purposes

- **Automation Name** (`WarriorSrv__AutomationName__c`) — *Text(255)*: The name of the automation, process, flow, trigger, batch, queueable, or other system logic associated with the logged error.
- **Error Number** (`Name`) — *Auto Number*: A system-generated unique identifier for each error record, used for tracking, referencing, and support. Format: {000000}
- **Exception Message** (`WarriorSrv__ExceptionMessage__c`) — *Long Text Area*: The raw exception message captured from the automation at the time of failure (e.g., `Exception.getMessage()`), used for debugging and error analysis.
- **Exception Type** (`WarriorSrv__ExceptionType__c`) — *Text(255)*: The system exception type associated with the error (e.g., NullPointerException, DmlException, CalloutException), used to categorize and analyze failures.
- **Gov Limit in Executing Code** (`WarriorSrv__GovLimitInExecutingCode__c`) — *Long Text Area*: A snapshot of Salesforce governor limit usage at the time the error occurred (e.g., SOQL queries, DML statements, CPU time, heap size), used for debugging limit-related failures.
- **Line Number** (`WarriorSrv__LineNumber__c`) — *Number(18,0)*: The line number in the executing Apex code where the exception was thrown, used to help identify the source of the error.
- **Method Name** (`WarriorSrv__MethodName__c`) — *Text(255)*: The method name in the executing Apex code where the exception was thrown.
- **Related To Id** (`WarriorSrv__RelatedToId__c`) — *Text(255)*: The Salesforce record Id associated with the error at the time it was logged. Populated automatically to identify the record being processed when the failure occurred.
- **Stack Trace** (`WarriorSrv__StackTrace__c`) — *Long Text Area*: The full Apex stack trace captured at the time of the exception (e.g., Exception.getStackTraceString()), used to identify the execution path and source of the error.

- [Return to Top](#table-of-contents)

## `Event Log Field` (Custom Metadata)

Stores information for fields used in Event Log to configure additional logged fields

- **Event Prefix** (`WarriorSrv__EventPrefix__c`) - *Text*: The string to prefix in the logs (e.g. 'Living Condition: ').
- **Field API Name** (`WarriorSrv__FieldAPI__c`) - *Text*: The exact API name of the Contact field to monitor for changes (e.g. WarriorSrv__Title38VerificationStatusPick__c).
- **Prefixes To Match** (`WarriorSrv__PrefixesToMatch__c`) - *Text*: Comma-separated values. If provided, the event will only log if new value starts with one of these (e.g. 'Emergency Shelter, Uninhabitable Location'). Leave blank to log all changes.

- [Return to Top](#table-of-contents)

## `Event Log` (Custom Object)

Stores information of meaningful changes to the contact record

- **Contact** (`WarriorSrv__ContactRef__c`) — *Master-Detail(Contact)*: The contact referenced by this event log.
- **Event Log Number** (`Name`) — *Auto Number*: System Generated title format: EL-{0}
- **Event Name** (`WarriorSrv__EventNameTrig__c`) — *Text(100)*: The field event being changed by its prefix and its new value.
- **Event New Value** (`WarriorSrv__EventNewValueTrig__c`) — *Text(50)*: The new value of the tracked field. 
- **Event Old Value** (`WarriorSrv__EventOldValueTrig__c`) — *Text(50)*: The old value of the tracked field. 

- [Return to Top](#table-of-contents)

## `Metric` (Custom Object)

Stores monthly aggregated metrics generated by a scheduled job, capturing point-in-time counts and activity across contact's, Cases, and Referrals. Records are system-generated and should not be manually created or edited.

- **Became Employed** (`BecameEmployedTrig__c`) — *Number*: Number of contact's who transitioned from Unemployed to Employed during the previous calendar month, based on Event Log records capturing status changes.
- **Became Stably Housed** (`BecameStablyHousedTrig__c`) — *Number*: Number of contact's whose housing status changed to Stably Housed during the previous calendar month, based on Event Log records where a prior value existed and the new value was recorded as Stably Housed.
- **Closed Benefits Cases** (`ClosedBenefitsCasesTrig__c`) — *Number*: Number of Benefits Cases that were closed during the previous calendar month, based on Case records with a Closed Date in that period and categorized under the Benefits record type.
- **Closed Education Cases** (`ClosedEducationCasesTrig__c`) — *Number*: Number of Education Cases that were closed during the previous calendar month, based on Case records with a Closed Date in that period and categorized under the Education record type.
- **Closed Employment Cases** (`ClosedEmploymentCasesTrig__c`) — *Number*: Number of Employment Cases that were closed during the previous calendar month, based on Case records with a Closed Date in that period and categorized under the Employment record type.
- **Closed Housing Financial Assist Cases** (`ClosedHousingFinancialAssistCasesTrig__c`) — *Number*: Number of Housing Cases categorized as Financial Assistance that were closed during the previous calendar month, based on Case records with a Closed Date in that period and mapped service categories (e.g., rental assistance, utilities, repairs).
- **Closed Housing Homeless/Prevent Cases** (`ClosedHousingHomelessPreventCasesTrig__c`) — *Number*: Number of Housing Cases categorized as Homelessness or Homelessness Prevention that were closed during the previous calendar month, based on Case records with a Closed Date in that period and mapped service categories (e.g., homeless, at risk for homelessness, SSVF-related services).
- **Closed Housing Other Cases** (`ClosedHousingOtherCasesTrig__c`) — *Number*: Number of Housing Cases that were closed during the previous calendar month and categorized into the Housing:Other metric grouping because they did not match the defined Financial Assistance or Homelessness/Homelessness Prevention housing category mappings.
- **Closed Legal Cases** (`ClosedLegalCasesTrig__c`) — *Number*: Number of Legal Cases that were closed during the previous calendar month, based on Case records with a Closed Date in that period and assigned to the Legal record type.
- **Closed Mental Health Cases** (`ClosedMentalHealthCasesTrig__c`) — *Number*: Number of Healthcare Cases categorized as Mental Health that were closed during the previous calendar month, based on Case records with a Closed Date in that period and mapped service category values.
- **Closed Other Cases** (`ClosedOtherCasesTrig__c`) — *Number*: Number of Cases that were closed during the previous calendar month and categorized under the Other record type or service category grouping when they did not fit into any defined primary service area.
- **Closed Other Healthcare Cases** (`ClosedOtherHealthcareCasesTrig__c`) — *Number*: Number of Healthcare Cases that were closed during the previous calendar month and categorized as Other Healthcare based on service category values that do not fall under Mental Health or Physical Health mappings.
- **Closed Physical Health Cases** (`ClosedPhysicalHealthCasesTrig__c`) — *Number*: Number of Healthcare Cases categorized as Physical Health that were closed during the previous calendar month, based on Case records with a Closed Date in that period and mapped service category values.
- **Closed Transportation Cases** (`ClosedTransportationCasesTrig__c`) — *Number*: Number of Cases categorized as Transportation (under the Other record type grouping) that were closed during the previous calendar month, based on Case records with a Closed Date in that period and mapped service category values.
- **Connected Benefits Cases** (`ConnectedBenefitsCasesTrig__c`) — *Number*: Number of Benefits Cases that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case.
- **Connected Education Cases** (`ConnectedEducationCasesTrig__c`) — *Number*: Number of Education Cases that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case.
- **Connected Employment Cases** (`ConnectedEmploymentCasesTrig__c`) — *Number*: Number of Employment Cases that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case.
- **Connected Housing Financial Assist Cases** (`ConnectedHousingFinancialAssistCasesTrig__c`) — *Number*: Number of Housing Cases categorized as Financial Assistance that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case and mapped service category values.
- **Connected Housing Homeless/Prevent Cases** (`ConnectedHousingHomelessPreventCasesTrig__c`) — *Number*: Number of Housing Cases categorized as Homelessness or Homelessness Prevention that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case and mapped service category values.
- **Connected Housing Other Cases** (`ConnectedHousingOtherCasesTrig__c`) — *Number*: Number of Housing Cases that had at least one associated Case Referral created during the previous calendar month and were categorized into the Housing:Other grouping because they did not match defined Financial Assistance or Homelessness/Homelessness Prevention mappings.
- **Connected Legal Cases** (`ConnectedLegalCasesTrig__c`) — *Number*: Number of Legal Cases that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case.
- **Connected Mental Health Cases** (`ConnectedMentalHealthCasesTrig__c`) — *Number*: Number of Healthcare Cases categorized as Mental Health that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case and mapped service category values.
- **Connected Other Cases** (`ConnectedOtherCasesTrig__c`) — *Number*: Number of Cases that had at least one associated Case Referral created during the previous calendar month and were categorized under the Other record type or service category grouping when they did not fit into any defined primary service area.
- **Connected Other Healthcare Cases** (`ConnectedOtherHealthcareCasesTrig__c`) — *Number*: Number of Healthcare Cases that had at least one associated Case Referral created during the previous calendar month and were categorized as Other Healthcare based on service category values that do not fall under Mental Health or Physical Health mappings.
- **Connected Physical Health Cases** (`ConnectedPhysicalHealthCasesTrig__c`) — *Number*: Number of Healthcare Cases categorized as Physical Health that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case and mapped service category values.
- **Connected Transportation Cases** (`ConnectedTransportationCasesTrig__c`) — *Number*: Number of Cases categorized as Transportation (under the Other record type grouping) that had at least one associated Case Referral created during the previous calendar month, based on referral records linked to the Case and mapped service category values.
- **Currently Employed** (`CurrentlyEmployedTrig__c`) — *Number*: Total number of contact's with an Employment Status of Employed at the time the monthly metrics job is executed, based on current Contact record values.
- **Currently Unemployed** (`CurrentlyUnemployedTrig__c`) — *Number*: Total number of contact's with an Employment Status of Unemployed at the time the monthly metrics job is executed, based on current Contact record values.
- **Eligible Not Enrolled VA Healthcare** (`EligibleNotEnrolledVAHealthcareTrig__c`) — *Number*: Total number of contact's identified as Eligible for VA Healthcare but not currently Enrolled, based on Contact record values at the time the monthly metrics job is executed.
- **Enrolled In Civilian Healthcare** (`EnrolledInCivilianHealthcareTrig__c`) — *Number*: Total number of contact's currently Indicates as enrolled in Civilian Healthcare, based on Contact record values at the time the monthly metrics job is executed.
- **Enrolled in VA Benefits Portal** (`EnrolledInVABenefitsPortalTrig__c`) — *Number*: Total number of contact's currently Indicates as enrolled in the VA Benefits Portal, based on Contact record values at the time the monthly metrics job is executed.
- **Green Status** (`GreenStatusTrig__c`) — *Number*: Total number of contact's currently classified with a Condition Rating of Green at the time the monthly metrics job is executed, based on Contact record values.
- **New Caregivers Added In Period** (`NewCaregiversAddedInPeriodTrig__c`) — *Number*: Number of new contact's with a Caregiver record type created during the previous calendar month, based on Contact Created Date.
- **New Family Members Added In Period** (`NewFamilyMembersAddedInPeriodTrig__c`) — *Number*: Number of new contact's with a Family Member record type created during the previous calendar month, based on Contact Created Date.
- **New Other contact's Added In Period** (`NewOthercontact'sAddedInPeriodTrig__c`) — *Number*: Number of new contact's created during the previous calendar month that do not fall under Warrior, Caregiver, or Family Member record types, based on Contact Created Date.
- **New Warriors Added In Period** (`NewWarriorsAddedInPeriodTrig__c`) — *Number*: Number of new contact's with a Warrior record type created during the previous calendar month, based on Contact Created Date.
- **Open Benefits Cases** (`OpenBenefitsCasesTrig__c`) — *Number*: Total number of Benefits Cases that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status.
- **Open Education Cases** (`OpenEducationCasesTrig__c`) — *Number*: Total number of Education Cases that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status.
- **Open Employment Cases** (`OpenEmploymentCasesTrig__c`) — *Number*: Total number of Employment Cases that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status.
- **Open Housing Financial Assist Cases** (`OpenHousingFinancialAssistCasesTrig__c`) — *Number*: Total number of Housing Cases categorized as Financial Assistance that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status and mapped service category values.
- **Open Housing Homeless/Prevention Cases** (`OpenHousingHomelessPreventionCasesTrig__c`) — *Number*: Total number of Housing Cases categorized as Homelessness or Homelessness Prevention that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status and mapped service category values.
- **Open Housing Other Cases** (`OpenHousingOtherCasesTrig__c`) — *Number*: Total number of Housing Cases that are currently open and categorized under the Housing:Other grouping because they do not match defined Financial Assistance or Homelessness/Homelessness Prevention mappings, based on Case records not in a Closed status.
- **Open Legal Cases** (`OpenLegalCasesTrig__c`) — *Number*: Total number of Legal Cases that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status.
- **Open Mental Health Cases** (`OpenMentalHealthCasesTrig__c`) — *Number*: Total number of Healthcare Cases categorized as Mental Health that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status and mapped service category values.
- **Open Other Cases** (`OpenOtherCasesTrig__c`) — *Number*: Total number of Cases that are currently open and categorized under the Other record type or service category grouping because they do not fit into any defined primary service area, based on Case records not in a Closed status.
- **Open Other Healthcare Cases** (`OpenOtherHealthcareCasesTrig__c`) — *Number*: Total number of Healthcare Cases that are currently open and categorized as Other Healthcare because they do not fall under Mental Health or Physical Health mappings, based on Case records not in a Closed status and mapped service category values.
- **Open Physical Health Cases** (`OpenPhysicalHealthCasesTrig__c`) — *Number*: Total number of Healthcare Cases categorized as Physical Health that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status and mapped service category values.
- **Open Transportation Cases** (`OpenTransportationCasesTrig__c`) — *Number*: Total number of Cases categorized as Transportation (under the Other record type grouping) that are currently open at the time the monthly metrics job is executed, based on Case records not in a Closed status and mapped service category values.
- **Orange Status** (`OrangeStatusTrig__c`) — *Number*: Total number of contact's currently classified with a Condition Rating of Orange at the time the monthly metrics job is executed, based on Contact record values.
- **Red Status** (`RedStatusTrig__c`) — *Number*: Total number of contact's currently classified with a Condition Rating of Red at the time the monthly metrics job is executed, based on Contact record values.
- **Total Caregiver Population** (`TotalCaregiverPopulationTrig__c`) — *Number*: Total number of contact's with a Caregiver record type at the time the monthly metrics job is executed, based on current Contact record values.
- **Total Family Member Population** (`TotalFamilyMemberPopulationTrig__c`) — *Number*: Total number of contact's with a Family Member record type at the time the monthly metrics job is executed, based on current Contact record values.
- **Total Other Population** (`TotalOtherPopulationTrig__c`) — *Number*: Total number of contact's that do not fall under Warrior, Caregiver, or Family Member record types at the time the monthly metrics job is executed, based on current Contact record values.
- **Total Warrior Population** (`TotalWarriorPopulationTrig__c`) — *Number*: Total number of contact's with a Warrior record type at the time the monthly metrics job is executed, based on current Contact record values.
- **Yellow Status** (`YellowStatusTrig__c`) — *Number*: Total number of contact's currently classified with a Condition Rating of Yellow at the time the monthly metrics job is executed, based on Contact record values.

- [Return to Top](#table-of-contents)

## `Service Record` (Custom Object)

Stores information regarding a contact's individual service history

- **Age at Enlistment** (`WarriorSrv__AgeAtEnlistmentAuto__c`) — *Formula(Number)*: Calculates the age when the contact enlisted.
- **Age at Separation** (`WarriorSrv__AgeAtSeparationAuto__c`) — *Formula(Number)*: Calculates the age the contact was when they separated from service.
- **Branch of Service** (`WarriorSrv__BranchOfServicePick__c`) — *Picklist*: Indicates the branch of service in which the contact served.
- **Contact** (`WarriorSrv__ContactRef__c`) — *Master-Detail(Contact)*: The contact this service record belongs to.
- **Grade** (`WarriorSrv__GradePick__c`) — *Picklist*: Indicates the current or prior Grade.
- **Is Active** (`WarriorSrv__IsActiveAuto__c`) — *Formula(Checkbox)*: Indicates the contact is still active.
- **Between Korea and Vietnam Era** (`WarriorSrv__IsBetweenKoreaAndVietnamEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served between Korea and Vietnam Era (February 1955 – July 1964)
- **Between WWII and Korean War Era** (`WarriorSrv__IsBetweenWWIIAndKoreanWarEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served between WWII and Korean War Era (August 1947 – May 1950)
- **Combat Deployed** (`WarriorSrv__IsHasCombatDeployed__c`) — *Checkbox*: Indicates the contact was deployed to a combat zone.
- **Has copy of DD-214** (`WarriorSrv__IsHasCopyOfDD214__c`) — *Checkbox*: Indicates the contact has a copy of their own DD-214.
- **Korean War Era** (`WarriorSrv__IsKoreanWarEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the Korean War Era (June 1950 – January 1955)
- **Persian Gulf Era** (`WarriorSrv__IsPersianGulfEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the Persian Gulf Era (August 1991 – September 2001)
- **Post September 11, 2001** (`WarriorSrv__IsPostSeptember112001Auto__c`) — *Formula(Checkbox)*: Indicates the contact served after September 11, 2001.
- **Post Vietnam Era** (`WarriorSrv__IsPostVietnamEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the Post Vietnam Era (May 1975 – July 1991)
- **Vietnam Era** (`WarriorSrv__IsVietnamEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the Vietnam Era (August 1964 – April 1975)
- **World War II Era** (`WarriorSrv__IsWorldWarIIEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the World War II Era (September 1940 - July 1947)
- **Rank** (`WarriorSrv__RankPick__c`) — *Picklist*: Indicates the contact's Rank.
- **Service Component** (`WarriorSrv__ServiceComponentPick__c`) — *Picklist*: The service component of the contact.
- **Service End Date** (`WarriorSrv__ServiceEndDate__c`) — *Date*: The end of the contact's service contract.
- **Service Eras** (`WarriorSrv__ServiceErasAuto__c`) — *Formula(Text)*: Indicates all the service eras the contact has served in.
- **Service Start Date** (`WarriorSrv__ServiceStartDate__c`) — *Date*: The start date of the contact's contract.
- **Service Status** (`WarriorSrv__ServiceStatusPick__c`) — *Picklist*: The contact's current service status.
- **Station Where Separated** (`WarriorSrv__StationWhereSeparated__c`) — *Text(255)*: The duty station that the contact ended their service at.
- **Theater of Operation(s)** (`WarriorSrv__TheaterOfOperationsPick__c`) — *Picklist (Multi-Select)*: Indicates the theaters of operation in which the veteran participated (combat deployed) during their time in service.
- **Type of Discharge** (`WarriorSrv__TypeOfDischargePick__c`) — *Picklist*: The category of the contact's discharge.
- **Years Served** (`WarriorSrv__YearsServedAuto__c`) — *Formula(Checkbox)*: The years the veteran served based on this service record.
- **Service Record Number** (`Name`) — *Auto Number*: Auto generated format SR-{0}

- [Return to Top](#table-of-contents)

## `Support Action` (Custom Object)

Used to track individual support actions provided to a Contact, including services or financial assistance delivered as part of a Case, with associated value, date, and responsible parties.

- **Action Date** (`WarriorSrv__ActionDate__c`) — *Date*: Indicates the date the action took place.
- **Action** (`WarriorSrv__ActionPick__c`) — *Picklist*: The actions taken.
- **Amount** (`WarriorSrv__Amount__c`) — *Currency*: Indicates the value of the Support Action.
- **Case** (`WarriorSrv__CaseRef__c`) — *Lookup(Case)*: The Case that received this support action.
- **Contact** (`WarriorSrv__ContactRef__c`) — *Master-Detail(Contact)*: The contact who received the support action.
- **Description** (`WarriorSrv__Description__c`) — *Text(255))*: Notes or description of the support action taken.
- **Support Action Number** (`Name`) — *Auto Number*: Auto-generated format SA-{YYYY}{MM}{DD}{0}
- **Support Action Supplier** (`WarriorSrv__SupportActionSupplierRef__c`) — *Lookup(Account)*: Indicates the payor of this support action.

- [Return to Top](#table-of-contents)

## `User` (Standard Object)

- **Bypass Validation Rules** (WarriorSrv__IsBypassVR__c) - *Checkbox*: Allows the User to bypass validation rules.

- [Return to Top](#table-of-contents)