### 📦 Core Objects

#### `Account` (Standard Object)

Standard Object for Accounts.

- **Company Facebook** (`WarriorSrv__CompanyFacebook__c`) - *URL*: The link to the account's Facebook account.
- **Company Instagram** (`WarriorSrv__CompanyInstagram__c`) - *URL*: The link to the account's Instagram account. 
- **Company LinkedIn** (`WarriorSrv__CompanyLinkedIn__c`) - *URL*: The link to the account's LinkedIn account.
- **Company X** (`WarriorSrv__CompanyX__c`) - *URL*: The link to the account's X account.
- **Elgigiblity Criteria** (`WarriorSrv__EligibilityCriteria`) - *Text*: Captures the specific requirements individuals must meet to qualify for services.
- **Basic Needs** (`WarriorSrv__IsBasicNeedsParnter`) - *Checkbox*: Indicated the account is a Basic Needs partner.
- **Benefits/VSO** (`WarriorSrv__IsBenefitsVSOPartner__c`) - *Checkbox*: Indicated the account is a Benefits/VSO Partner
- **Caregiver Support** (`WarriorSrv__IsCaregiverSupportPartner__c`) - *Checkbox*: Indicated the account is a Caregiver Support Partner
- **Education** (`WarriorSrv__IsEducationPartner__c`) - *Checkbox*: Indicated the account is a Education Partner.
- **Family Support** (`WarriorSrv__IsFamilySupportPartner__c`) - *Checkbox*: Indicated the account assist with Family Support. 
- **Funding** (`WarriorSrv__IsFundingPartner__c`) - *Checkbox*: Indicated the account is a Funding Partner.
- **Housing** (`WarriorSrv__IsHousingPartner__c`) - *Checkbox*: Indicated the account is a Housing Partner.
- **Job Placement** (`WarriorSrv__IsJobPlacementPartner__c`) - *Checkbox*: Indicated the account is a Job Placement Partner.
- **Legal** (`WarriorSrv__IsLegalPartner__c`) - *Checkbox*: Indicated the account is a Legal Partner.
- **Long Term Financial** (`WarriorSrv__IsLongTermFinancialPartner__c`) - *Checkbox*: Indicated the account is a Long Term Financial Partner.
- **Medical Devices** (`WarriorSrv__IsMedicalDevicesPartner__c`) - *Checkbox*: Indicated the account is a Medical Devices Partner.
- **Mental Health** (`WarriorSrv__IsMentalHealthPartner__c`) - *Checkbox*: Indicated the account is a Mental Health Partner.
- **Peer Support** (`WarriorSrv__IsPeerSupportPartner__c`) - *Checkbox*: Indicated the account is a Peer Support Partner.
- **Physical Health** (`WarriorSrv__IsPhysicalHealthPartner__c`) - *Checkbox*: Indicated the account is a Physical Health Partner.
- **Recreation** (`WarriorSrv__IsRecreationPartner__c`) - *Checkbox*: Indicated the account is a Recreation Partner.
- **Short Term Financial** (`WarriorSrv__IsShortTermFinancialPartner__c`) - *Checkbox*: Indicated the account is a Short Term Financial Partner.
- **Spirituality** (`WarriorSrv__IsSpiritualityPartner__c`) - *Checkbox*: Indicated the account is a Spirituality Partner.
- **Technology** (`WarriorSrv__IsTechnologyPartner__c`) - *Checkbox*: Indicated the account is a Technology Partner.
- **Transportation** (`WarriorSrv__IsTransportationPartner__c`) - *Checkbox*: Indicated the account is a Transportation Partner.
- **Volunteer Opportunities** (`WarriorSrv__IsVolunteerOpportunitiesPartner__c`) - *Checkbox*: Indicated the account is Volunteer Partner.
- **Partner Account Star Rating** (`WarriorSrv__PartnerStarRatingAuto__c`) - *Formula(TEXT)*: Visual representation of the Partner Score.
- **Partner Rating** (`WarriorSrv__PartnerRatingPickTrig__c`) - *Picklist*: Partner score filled in only by automation from Case Referrals.
- **Referral Count** (`WarriorSrv__ReferralCountTrig__c`) - *Number*: The count of Case Referrals only filled by automation.
- **Referral Type** (`WarriorSrv__ReferralTypePick__c`) - *Picklist*: Indicates the type of referral required or accepted by the organization.
- **Service Coverage** (`WarriorSrv__ServiceCoveragePick__c`) - *Picklist*: Indicates the geographic scope of services provided by the organization, specifying whether they serve local or national clients. This helps categorize organizations based on their service area for accurate referral and resource matching.
- **Service Description** (`WarriorSrv__ServiceDescription__c`) - *Text*: Describes the services provided by the organization.
- **VA Facility External Id** (`WarriorSrv__VAFacilityExternalId__c`) - *Text*: This field stores the external identifier linking this Salesforce account to the corresponding VA Facility system record. It facilitates integration and data synchronization between Salesforce and the VA Facility system.


#### `Case` (Standard Object)

Standard Object for Case Tracking.

- **Case Close Reason** (`CaseCloseReasonPick__c`) — *Picklist*: The reason the case was closed.
- **Condition** (`ConditionAuto__c`) - *Formula(Text)*: Displays color and name to visually see the condition.
- **Condition Rating** (`ConditionRatingTrig__c`) - *Formula(Text)*: Set by automation to display a color for each condition.
- **Contact Email** (`ContactEmailAuto__c`) - *Formula(Text)*:	Displays the client's email if it's available; otherwise, displays "No Email Provided". Used in Case Referral Automations.
- **Contact Name** (`ContactNameAuto__c`) - *Formula(Text)*: Displays the client's full name. If both first and last names are available, it concatenates them; otherwise, it shows whichever part is not blank. Used in Case Referral Automations.
- **Contact Phone** (`ContactPhoneAuto__c`) - *Formula(Text)*: 	Displays the client's phone number if it's available; otherwise, displays "No Phone Provided"
- **Current Salary/Wage** (`CurrentSalaryWage__c`) - *Currency*: The current Salary/Wage of the Contact.
- **Days Open** (`DaysOpenAuto__c`) - *Formula(Number)*: The amount of time a case has been or was open.
- **Desired Annualized Salary** (`DesiredAnnualizedSalary__c`) - *Currency*: 	The desired salary of the individual annualized.
- **Desired Salary Wage** (`DesiredSalaryWage__c`) - *Currency*: The desired salary/wage of the individual.
- **Enrollment Date** (`EnrollmentDate__c`) - *Date*: The date enrolled, can be used for different types of enrollment.
- **Felony Description** (`FelonyDescription__c`) - *Text*: The description of a felonious act by the individual.
- **Has Current Resume** (`IsCurrentResume__c`) - *Checkbox*: The individual has a current resume.
- **Has Felony__c** (`IsHasFelony__c`) - *Checkbox*: Indicates the individual has a Felony conviction.
- **Highest Level of Education** (`HighestLevelOfEducationPick__c`) - *Picklist*: Indicates the highest level of the individuals education.
- **Job Search** (`IsJobSearch__c`) - *Checkbox*: Warrior need help finding employment.
- **Professional Category** (`ProfessionalCategoryPick__c`) - *Picklist*: The Profession of the individual.
- **Professional Designator** (`ProfessionalDesignatorPick__c`) - *Picklist*: The Designation of the individual's profession.
- **Professional Mentorship** (`IsProfessionalMentorship__c`) - *Checkbox*: Identifies that the individual is seeking professional mentorship.
- **Record Type Name** (`RecordTypeNameAuto__c`) — *Formula(Text)*: Displays the record type name of the case. Used in Case Referral Automations.
- **Resume Assistance** (`IsResumeAssistance__c`) - *Checkbox*: Indicates that the individual requires resume assistance.
- **Resume Attached** (`IsResumeAttached__c`) - *Checkbox*: Indicates that the individual's resume is attached to this case.
- **Salary/Wage Period** (`SalaryWagePeriodPick__c`) - *Picklist*: Time Period as applies to Salary/Wage
- **Service Category** (`ServiceCategoryPick__c`) - *Picklist*: The subcategory of the case record type. Used with Condition Rating to show a color rated value.
- **Shift Desired** (`ShiftDesiredPick__c`) - *Multi-Select Picklist*: Indicates the shift the individual desires.
- **SSVF Housing Category** (`SSVFHousingCategoryPick__c`) - *Picklist*: The category of SSVF Homelessness.
- **SSVF Status** (`SSVFStatusPick__c`) - *Picklist*: The current SSVF status of the contact.
- **Target Date To Be Employed** (`TargetDateToBeEmployed__c`) - *Date*: Indicates the individuals desired date to get employment.
- **Total Value Of Support Actions** (`TotalValueOfSupportActionsTrig__c`) - *Currency*: Holds the total value of support actions for this case.
- **Work And Shift Desired** (`WorkAndShiftDesiredPick__c`) - *Multi-Select Picklist*: Work and Shift Desired

#### `Case Referral` (Custom Object)

Stores data to manage case referrals to partners.

- **Case** (`CaseRef__c`) — *Master-Detail -> Case*: Links Case Referral to Case for steamlined data association.
- **Do Not Email Contact** (`IsDoNotEmailContact__c`) — *Checkbox*: Indicates we will not send the Case Referral Email when checked.
- **Rating** (`RatingPick__c`) — *Picklist*: This picklist on the rating field ranges from 1 to 5 stars and visually represents the rating using star images.
- **Rating Auto** (`RatingAuto__c`) — *Formula(Number)*: Numerical version of the rating for easier calculations.
- **Rating Reason** (`RatingReason__c`) — *Text*: The indicated reason for the selected rating.
- **Referral Number** (`Name`) — *Auto Number*: The Unique number for this record. 
- **Referred To Account** (`ReferredToAccountRef__c`) — *Master-Detail -> Account*: The account we have made a referral to.
- **Referred To Contact** (`ReferredToContactRef__c`) — *Lookup -> Contact*: The individual at the account we are referring to.
- **Star Rating** (`StarRatingAuto__c`) — *Formula(Text)*: The visual representation of the Rating.

#### `Condition Rating` (Custom Object)

Defines standardized severity levels with unique names and color codes for classifying and prioritizing cases in WarriorServe.

- **Rating** (`RatingPick__c`) — *Picklist*: This is used to assign a color to a rating. All non specified ratings will default to Green.
- **Type API Name** (`Name`) — *Text(80)*: The exact API name that should be checked as on the Case field `ServiceCategoryPick__c`.

#### `Contact` (Standard Object)
 
Standard Object for Contacts.

- **Age** (`AgeAuto__c`) — *Formula(Number)*: The contact's current age.
- **Barriers** (`BarriersPick__c`) — *Picklist*: Indicates any barriers for the contact. (Flag for Recheck on usage)
- **Benefits** (`IsInitialBenefits`) — *Checkbox*: Indicates the contacts initially need a benefits case.
- **Caregiver Type** (`CaregiverTypePick__c`) — *Picklist*: Classifies the contact’s caregiver role and population served. Used to standardize reporting, segmentation, and program eligibility.
- **Closed Cases** (`ClosedCasesTrig__c`) — *Number*: Indicates the number of closed cases for the contact.
- **Condition Rating** (`ConditionRatingAuto__c`) — *Formula(Text)*: Indicates the contact's condition based on their current open cases.
- **Consent to Share Information** (`ConsentStatusPick__c`) — *Picklist*: Indicates the individual’s consent status for sharing their information with approved partner organizations for coordination of services. This field should reflect the most current consent decision and is used to control data sharing and integrations.
- **Current Living Situation** (`CurrentLivingConditionPick__c`) — *Picklist*: The contact’s current housing or living situation at the time the information is collected. Use this field to record where the contact is presently staying, such as rented housing, temporary shelter, institutional housing, or other current living arrangements.
- **Date Last Housed** (`DateLastHousedTrig__c`) — *Date*: Date the contact was last housed.
- **Date Unemployed Set** (`DateUnemployedSetTrig__c`) — *Date*: Date the contact was set as unemployed.
- **Deceased Date** (`DeceasedDate__c`) — *Date*: The date the contact was determined deceased.
- **Disability Percentage** (`DisabilityPercentagePick__c`) — *Picklist*: Contact VA Disability rating.
- **Education** (`IsInitialEducation__c`) — *Checkbox*: Indicates the contacts initially need a education case.
- **Eligible for Tricare** (`EligibleForTricarePick__c`) — *Picklist*: Indicates whether the contact is eligible for TRICARE benefits based on known or provided information at the time. Use this field to capture confirmed, unconfirmed, or unknown eligibility status to support service eligibility and referral decisions.
- **Eligible for VA Healthcare** (`EligibleForVAHealthcarePick__c`) — *Picklist*: Indicates whether the contact is eligible for VA Healthcare benefits based on known or provided information at the time. Use this field to capture confirmed, unconfirmed, or unknown eligibility status to support service eligibility and referral decisions.
- **Employment** (`IsInitialEmployment__c`) — *Checkbox*: Indicates the contact needs an initial employment case.
- **Employment Status** (`EmploymentStatusPick__c`) — *Picklist*: Indicates a contact's current employment status.
- **Employment Type** (`EmploymentTypePick__c`) — *Picklist*: Indicates the contact's type of emplyment.
- **Enrolled in Civilian Healthcare** (`EnrolledInCivilianHealthcarePick__c`) — *Picklist*: Indicates a contact's current Civilian Healthcare status.
- **Enrolled in Healthcare** (`EnrolledInHealthcareAuto__c`) — *Formula(Checkbox)*: 	Evaluates whether the individual is currently enrolled in any healthcare program.
- **Enrolled in School** (`EnrolledInSchoolTrig__c`) — *Number(2,0)*: Rollup field calculated from education records.
- **Enrolled in Tricare** (`EnrolledInTricarePick__c`) — *Picklist*: The contact's Tricare enrollment status.
- **Enrolled in VA Benefits Portal** (`EnrolledInVABenefitsPortalPick__c`) — *Picklist*: Indicates the contact's VA Benefits Portal status.
- **Enrolled in VA Healthcare** (`EnrolledInVAHealthcarePick__c`) — *Picklist*: The contacts VA Healthcare enrollment status.
- **Family Support** (`IsInitialFamilySupport__c`) — *Checkbox*: Indicated the contact needs an initial family support case.
- **Has Service-Connected Injury** (`HasServiceConnectedInjuryPick__c`) — *Picklist*: Indicates the contacts service-connected injury status.
- **Has Valid Drivers License** (`IsHasValidDriversLicense__c`) — *Checkbox*: Indicates the contact has a valid drivers license.
- **Healthcare** (`IsInitialHealthcare__c`) — *Checkbox*: Indicates the contact requires an initial healthcare case.
- **Home Location Type** (`HomeLocationTypePick__c`) — *Picklist*: Classifies the individual’s home location as urban, suburban, or rural for reporting purposes.
- **Homeless Events** (`HomelessEventsTrig__c`) — *Number(3,0)*: Indicates the amount of Homeless Events for a contact.
- **Housed Events** (`HousedEventsTrig__c`) — *Number(3,0)*: Counts the number of Housed Events for the contact.
- **Housing** (`IsInitialHousing__c`) — *Checkbox*: Indicates that an initial Housing case is required.
- **HUD Homeless** (`HUDHomelessPick__c`) — *Picklist*: Indicates the contact's HUD Homeless status.
- **Interest** (`InterestsPick__c`) — *Picklist (Multi-Select)*: The contact's interest.
- **Last Date Homeless** (`LastDateHomelessTrig__c`) — *Date*: The date of the last recorded Homeless Event
- **Last Four SSN** (`LastFourSSN__c`) — *Number(4,0)*: The last four digits of the contact's social security number.
- **Lead Source Organization** (`LeadSourceOrganizationRef__c`) — *Lookup(Account)*: The specific organization associated with the selected Lead Source when known. Use this field to identify the partner, agency, or organization connected to how the contact was acquired or referred.
- **Legal** (`IsInitialLegal__c`) — *Checkbox*: Indicates an initial legal case is required.
- **Mailing County** (`MailingCounty__c`) — *Text(30)*: The mailing county of the contact.
- **Marital Status** (`MaritalStatusPick__c`) — *Picklist*: Indicates the current known marital status of the contact.
- **Military Family Member** (`IsMilitaryFamilyMember__c`) — *Checkbox*: Indicates the contact is a Military Family Member.
- **Mode of Transportation** (`ModeOfTransportationPick__c`) — *Picklist*: Indicates the contact's primary mode of transportation.
- **Number of Children** (`NumberOfChildren__c`) — *Number(2,0)*: Indicates the contact's current number of children under 18.
- **Number Of Combat Related Injuries** (`NumberOfCombatRelatedInjuriesTrig__c`) — *Number(2,0)*: Number of Combat-Related Injuries rolled up from Warrior Injuries
- **Number of Household Members** (`NumberOfHouseholdMembers__c`) — *Number(3,0)*: Indicates the number of people in the contacts household.
- **Open Cases** (`OpenCasesTrig__c`) — *Number(18,0)*: Indicates the number of open cases on the contact.
- **Open Orange Cases** (`OpenOrangeCasesTrig__c`) — *Number(18,0)*: Indicates the number of Open Orange Cases for the contact.
- **Open Red Cases** (`OpenRedCasesTrig__c`) — *Number(18,0)*: The count of open red cases.
- **Open Yellow Cases** (`OpenYellowCasesTrig__c`) — *Number(18,0)*: The count of open yellow cases.
- **Other** (`IsInitialOther__c`) — *Checkbox*: Indicates an initial other case should be opened for the contact.
- **Post 9/11 Service Records** (`Post911ServiceRecordsTrig__c`) — *Number(18,0)*: Indicates the number of Post 9/11 service records assigned to the contact.
- **Preferred Method of Contact** (`PreferredMethodOfContactPick__c`) — *Picklist*: Indicates the contact's preferred way to be contacted.
- **Race** (`RacePick__c`) — *Picklist (Multi-Select)*: Indicates the racial identity of the contact.
- **Record Age** (`RecordAgeAuto__c`) — *Formula(Number)*: Indicates the age of the contact in days.
- **Record Type Name** (`RecordTypeNameAuto__c`) — *Formula(Text)*: Displays the record type by name, used in some formulas and integrations.
- **Seeking Housing Assistance** (`IsSeekingHousingAssistance__c`) — *Checkbox*: Indicates this contact is seeking housing assistance.
- **Send Newsletter?** (`IsCanSendNewsletter__c`) — *Checkbox*: Indicates the contact would like to receive a newsletter.
- **Service Record Count** (`ServiceRecordCountAuto__c`) — *Roll-Up Summary*: Number of Service Records Entered on the contact.
- **Spanish, Hispanic or Latino** (`IsSpanishHispanicOrLatino__c`) — *Checkbox*: Indicates the contact identifies as Spanish, Hispanic or Latino.
- **Special Handling** (`SpecialHandlingPick__c`) — *Picklist (Multi-Select)*: Indicates information that might be needed when speaking with this contact.
- **Title 38 Confirmed** (`IsTitle38ConfirmedTrig__c`) — *Checkbox*: Confirms the contact is a title 38 veteran status.
https://www.govinfo.gov/content/pkg/CPRT-112HPRT65875/pdf/CPRT-112HPRT65875.pdf
- **Total Value Of Support Actions** (`TotalValueOfSupportActionsAuto__c`) — *Roll-Up Summary*: Automatically stores the total of support actions where this contact was indicated.
- **Unemployed Events** (`UnemployedEventsTrig__c`) — *Number(18,0)*: Indicates the number of times this contact has had unique unemployment events set.
- **Volunteer Opportunties** (`IsInitialVolunteerOpportunties__c`) — *Checkbox*: Indicates the contacts needs an initial volunteer opportunity.
- **WWP® Alumni Enrollment Status** (`WWPAlumniEnrollmentStatusPick__c`) — *Picklist*: Indicates the contact's WWP enrollment status.
- **WWP® Decline Reason** (`WWPDeclineReasonPick__c`) — *Picklist*: Indicates the reasoning the contact declined WWP enrollment.
- **WWP® Family Support Enrollment Status** (`WWPFamilySupportEnrollmentStatusPick__c`) — *Picklist*: Indicates the WWP Family Support enrollment status of the contact.

#### `Education` (Custom object)

Allow for storing information regarding the contacts education status such as schooling attended or certifications completed.

- **Benefits Status** (`BenefitsStatusPick__c`) - *Picklist*: Indicates the contact's usage status of education benefits.
- **Contact** (`ContactRef__c`) - *Master-Detail(Contact)*: The contact who's education information this is.
- **Date Disenrolled** (`DateDisenrolledTrig__c`) - *Date*: Date the Status was changed to Disenrolled. This field is automatically set by system automation and reflects the most recent transition to Disenrolled. It is not intended for manual modification.
- **Date Graduated** (`DateGraduatedTrig__c`) - *Date*: The date the individual completed the education or training program. This field represents the actual program completion date and may be set by automation or manually updated if known.
- **Program Name** (`Name`) - *Text(80)*: The name of the education or training program the individual is enrolled in or completed. This may include degree programs, certifications, vocational training, apprenticeships, or other VA-eligible education paths.
- **Projected Graduation Date** (`ProjectedGraduationDate__c`) - *Date*: The date the contact is expecting to graduate.
- **Reason for Disenrollment** (`ReasonForDisenrollmentPick__c`) - *Picklist*: Indicates the reason the individual discontinued participation in the education or training program. This field is only applicable when Status is Disenrolled.
- **Status** (`StatusPick__c`) - *Picklist*: Indicates the current status of the education record.
- **Type** (`TypePick__c`) - *Picklist*: The type of education associated with this education record.
- **VA Education Benefit** (`VAEducationBenefitPick__c`) — *Picklist*: Education benefits used by the contact.

#### `Employment` (Custom Object)

Stores information regarding a contacts employment history or current employment.

- **Contact** (`ContactRef__c`) — *Master-Detail(Contact)*: The contact who's employment record this is.
- **Currently Employed** (`IsCurrentlyEmployed__c`) — *Checkbox*: Indicates the contact is currently employed.
- **Employer** (`EmployerRef__c`) — *Lookup(Account)*: Indicates the company employing this contact.
- **End Date** (`EndDate__c`) — *Date*: The date the contact left this position.
- **Gross Annualized Salary** (`GrossAnnualizedSalary__c`) — *Currency(16,2)*: The Salary this employment record is associated with.
- **Position** (`Name`) — *Text(80)*: The job title of this employment record. 
- **Reason for Leaving** (`ReasonForLeavingPick__c`) — *Picklist*: The reason the contact left this role.
- **Start Date** (`StartDate__c`) — *Date*: The date the contact started this position.
- **Work Type** (`WorkTypePick__c`) — *Picklist*: Indicates the current type of employment.

#### `Error` (Custom Object)

Stores infomration regarding errors that may happen during WarriorServe® usage for debugging purposes

- **Automation Name** (`AutomationName__c`) — *Text(255)*: The name of the automation, process, flow, trigger, batch, queueable, or other system logic associated with the logged error.
- **Error Number** (`Name`) — *Auto Number*: A system-generated unique identifier for each error record, used for tracking, referencing, and support. Format: {000000}
- **Exception Message** (`ExceptionMessage__c`) — *Long Text Area*: The raw exception message captured from the automation at the time of failure (e.g., `Exception.getMessage()`), used for debugging and error analysis.
- **Exception Type** (`ExceptionType__c`) — *Text(255)*: The system exception type associated with the error (e.g., NullPointerException, DmlException, CalloutException), used to categorize and analyze failures.
- **Gov Limit in Executing Code** (`GovLimitInExecutingCode__c`) — *Long Text Area*: A snapshot of Salesforce governor limit usage at the time the error occurred (e.g., SOQL queries, DML statements, CPU time, heap size), used for debugging limit-related failures.
- **Line Number** (`LineNumber__c`) — *Number(18,0)*: The line number in the executing Apex code where the exception was thrown, used to help identify the source of the error.
- **Method Name** (`MethodName__c`) — *Text(255)*: The method name in the executing Apex code where the exception was thrown.
- **Related To Id** (`RelatedToId__c`) — *Text(255)*: The Salesforce record Id associated with the error at the time it was logged. Populated automatically to identify the record being processed when the failure occurred.
- **Stack Trace** (`StackTrace__c`) — *Long Text Area*: The full Apex stack trace captured at the time of the exception (e.g., Exception.getStackTraceString()), used to identify the execution path and source of the error.

#### `Event Log` (Custom Object)

Stores information of meaningful changes to the contact record

- **Contact** (`ContactRef__c`) — *Master-Detail(Contact)*: The contact that this event log is referring.
- **Event Log Number** (`Name`) — *Auto Number*: System Generated title format: EL-{0}
- **Event Name** (`EventNameTrig__c`) — *Text(100)*: The field event being changed and its new value.
- **Event New Value** (`EventNewValueTrig__c`) — *Text(50)*: The new value of the tracked field. 
- **Event Old Value** (`EventOldValueTrig__c`) — *Text(50)*: The old value of the tracked field. 

#### `Service Record` (Custom Object)

Stores information regarding a contacts individual service history

- **Age at Enlistment** (`AgeAtEnlistmentAuto__c`) — *Formula(Number)*: Calculates the age when the contact enlisted.
- **Age at Separation** (`AgeAtSeparationAuto__c`) — *Formula(Number)*: Calculates the age the contact was when they separated from service.
- **Between Korea and Vietnam Era** (`IsBetweenKoreaAndVietnamEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served between Korea and Vietnam Era (February 1955 – July 1964)
- **Between WWII and Korean War Era** (`IsBetweenWWIIAndKoreanWarEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served between WWII and Korean War Era (August 1947 – May 1950)
- **Branch of Service** (`BranchOfServicePick__c`) — *Picklist*: 	Indicates the contact branch that they served in.
- **Combat Deployed** (`IsHasCombatDeployed__c`) — *Checkbox*: Indicates the contact was deployed to a combat zone.
- **Contact** (`ContactRef__c`) — *Master-Detail(Contact)*: The contact this service record belongs to.
- **Grade** (`GradePick__c`) — *Picklist*: Indicates the current or prior Grade.
- **Has copy of DD-214** (`IsHasCopyOfDD214__c`) — *Checkbox*: Indicates the contact has a copy of their own DD-214.
- **Home of Record City** (`HomeOfRecordCity__c`) — *Text(50)*: The home of record for the contact.
- **Home of Record State** (`HomeOfRecordStatePick__c`) — *Picklist*: The home of record state of the contact.
- **Is Active** (`IsActiveAuto__c`) — *Formula(Checkbox)*: Indicates the contact is still active.
- **Korean War Era** (`IsKoreanWarEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the Korean War Era (June 1950 – January 1955)
- **Persian Gulf Era** (`IsPersianGulfEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the Persian Gulf Era (August 1991 – September 2001)
- **Post September 11, 2001** (`IsPostSeptember112001Auto__c`) — *Formula(Checkbox)*: Indicates the contact served after September 11, 2001.
- **Post Vietnam Era** (`IsPostVietnamEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the Post Vietnam Era (May 1975 – July 1991)
- **Rank** (`RankPick__c`) — *Picklist*: Indicates the contacts Rank.
- **Service Component** (`ServiceComponentPick__c`) — *Picklist*: The service component of the contact.
- **Service End Date** (`ServiceEndDate__c`) — *Date*: The end of the contact's service contract.
- **Service Eras** (`ServiceErasAuto__c`) — *Formula(Text)*: Indicates all the service era's the contact has served in.
- **Service Record Number** (`Name`) — *Auto Number*: Auto generated format SR-{0}
- **Service Start Date** (`ServiceStartDate__c`) — *Date*: The start date of the contacts contract.
- **Service Status** (`ServiceStatusPick__c`) — *Picklist*: The contacts current service status.
- **Station Where Separated** (`StationWhereSeparated__c`) — *Text(255)*: The duty station that the contact ended their service at.
- **Theater of Operation(s)** (`TheaterOfOperationsPick__c`) — *Picklist (Multi-Select)*: Indicate the theater of operations that the Warrior has participated (combat deployed) during their time in service.
- **Type of Discharge** (`TypeOfDischargePick__c`) — *Picklist*: The category of the contacts discharge.
- **Vietnam Era** (`IsVietnamEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the Vietnam Era (August 1964 – April 1975)
- **World War II Era** (`IsWorldWarIIEraAuto__c`) — *Formula(Checkbox)*: Indicates the contact served during the World War II Era (September 1940 - July 1947)
- **Years Served** (`YearsServedAuto__c`) — *Formula(Checkbox)*: The years the veteran served based on this service record.

#### `Support Action` (Custom Object)

Used to track individual support actions provided to a Contact, including services or financial assistance delivered as part of a Case, with associated value, date, and responsible parties.

- **Action** (`ActionPick__c`) — *Picklist*: The actions taken.
- **Action Date** (`ActionDate__c`) — *Date*: Indicates the date the action took place.
- **Amount** (`Amount__c`) — *Currency*: Indicates the value of the Support Action.
- **Case** (`CaseRef__c`) — *Lookup(Case)*: The Case that received this support action.
- **Contact** (`ContactRef__c`) — *Master-Detail(Contact)*: The contact who received the support action.
- **Description** (`Description__c`) — *Text(255))*: Notes or description of the support action taken.
- **Supper Action Number** (`Name`) — *Auto Number*: Auto-Generated format SA-{YYYY}{MM}{DD}{0}
- **Support Action Supplier** (`SupportActionSupplierRef__c`) — *Lookup(Account)*: Indicates the payor of this support action.

#### `Metric` (Custom Object)
Stores an automatically generated snapshot of how your organization is doing using predefined context

- **Label** (`FieldApiName`) — *FieldType*: Use
- **Label** (`FieldApiName`) — *FieldType*: Use

A snapshot overview of how your organization has done serving their community.
//TODO finish Metric and ensure it is visible and being schedule popualted.
