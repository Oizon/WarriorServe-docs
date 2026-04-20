# 🎯 Trigger Handlers

## `CaseReferralTriggerHandler`

**Object:** Case Referral  
**Events:** After Insert, After Update, After Delete, After Undelete

Handles Case Referral automation when WarriorServe is enabled.

### Key Functions
- Recalculates referral-related summary values on the referred partner Account
- Updates metrics such as total referral count and average partner rating
- Automatically shares related Case and Contact records with the partner user tied to the referred Contact when enabled
- Maintains referral-driven partner data consistency after record changes

### Controls
- Respects WarriorServe settings
- Auto-sharing behavior is configurable
- Errors captured through centralized exception handling

## `CaseTriggerHandler`

**Object:** Case  
**Events:** Before Insert, Before Update, Before Delete, After Insert, After Update, After Delete

Handles core Case automation when WarriorServe is enabled.

### Key Functions
- Sets the Case condition rating based on the selected Service Category
- Defaults the condition rating to Green when no configured rating exists
- Queues rollup processing to recalculate Contact-level case summary metrics
- Updates values such as open cases, closed cases, and counts by condition severity
- Creates Event Log records for deleted Cases when event logging is enabled

### Controls
- Respects WarriorServe settings
- Event logging is configurable
- Errors captured through centralized exception handling

## `ConditionRatingTriggerHandler`

**Object:** Condition Rating  
**Events:** Before Insert

Enforces data integrity for Condition Rating records during creation.

### Key Functions
- Prevents duplicate rating names within the same transaction
- Prevents duplicate rating names that already exist in Salesforce
- Validates that each rating name matches a valid Case Service Category picklist value
- Maintains alignment between condition ratings and Case classification values
- Helps preserve clean, standardized configuration data

### Controls
- Runs during record creation before save
- Errors captured through centralized exception handling

## `ContactTriggerHandler`

**Object:** Contact  
**Events:** After Insert, After Update

Handles Contact-driven automation when WarriorServe is enabled.

### Key Functions
- Writes Contact-related Event Log records
- Queues veteran status confirmation checks for Contacts with sufficient identifying information
- Supports post-save automation tied to Contact lifecycle changes
- Centralizes Contact-driven operational processes

### Controls
- Respects WarriorServe settings
- Veteran confirmation can be bypassed when configured
- Errors captured through centralized exception handling

## `ErrorEventTriggerHandler`

**Object:** Error Event  
**Events:** After Insert

Converts platform error events into persistent Error records for monitoring, reporting, and troubleshooting.

### Key Functions
- Creates `Error__c` records from incoming `Error_Event__e` platform events
- Stores related record identifiers when provided
- Captures exception details such as message, type, line number, stack trace, method name, and automation name
- Preserves governor limit context from the originating process
- Supports structured operational error tracking and historical review

### Controls
- Runs after platform event creation
- Inserts error records using system mode access
- Supports partial success processing during bulk inserts

## `SupportActionTriggerHandler`

**Object:** Support Action  
**Events:** After Insert, After Update, After Delete, After Undelete

Maintains Case-level rollup totals based on related Support Action records.

### Key Functions
- Collects impacted Case records after Support Action changes
- Recalculates the total value of all related Support Actions per Case
- Updates the Case field `TotalValueOfSupportActionsTrig__c`
- Includes both new and previous Case relationships during updates
- Ensures totals remain accurate after inserts, edits, deletions, and undeletes

### Controls
- Queries and updates records using system mode access
- Supports bulk processing across multiple Cases
- Errors captured through centralized exception handling
