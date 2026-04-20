### 🎯 Trigger Handlers

#### `CaseReferralTriggerHandler`

Handles post-save automation for `CaseReferral__c` records when WarriorServe is enabled. On insert, update, and delete, it recalculates referral-related summary fields on the referred partner Account, including total referral count and average partner rating. On insert and update, it can also automatically share the related Case and Contact with the partner user tied to the referred Contact when auto-sharing is enabled in settings. On insert, it additionally sends a referral email to the referred Contact unless the referral is marked do-not-email. All logic is controlled by WarriorServe settings and wrapped in exception logging for error tracking. Naming and structure are broadly aligned with the documented Apex naming standards.

#### `CaseTriggerHandler`

Handles core `Case` automation when WarriorServe is enabled. Before insert and update, it sets the Case condition rating based on the selected service category, defaulting to Green when no configured rating is found. After insert, update, and delete, it queues rollup processing to recalculate Contact-level case summary fields such as open cases, closed cases, and counts by condition severity. Before delete, it can also create event log entries for deleted Cases when event logging is enabled. All processing is wrapped in exception logging to support troubleshooting.

#### `ConditionRatingTriggerHandler`

Enforces data integrity for `ConditionRating__c` records during creation. On insert, it prevents duplicate rating names (both within the same transaction and against existing records) and ensures that each rating name matches a valid Case Service Category picklist value. This guarantees alignment between condition ratings and Case classification while maintaining clean, standardized data. All validation is wrapped with exception logging for error tracking.

#### `ContactTriggerHandler`

Handles post-save Contact automation when WarriorServe is enabled. After insert and update, it can automatically create intake Cases based on configured initial-need flags, create or reassign follow-up Tasks when a Contact’s living condition indicates possible HUD homelessness, and write Contact-related event logs. It also queues veteran status confirmation checks for Contacts with sufficient identifying information unless that process is explicitly bypassed. This trigger centralizes key Contact-driven intake and follow-up automation while relying on WarriorServe settings to control behavior.

#### `EducationTriggerHandler`

Handles status-driven field updates for Education__c records when WarriorServe is enabled. Before insert and update, it detects changes to the education status and automatically sets key milestone dates, including the date disenrolled and date graduated/certified. This ensures status transitions are consistently tracked without requiring manual data entry, while all processing is wrapped in exception logging for reliability.

#### `ErrorEventTriggerHandler`

Handles platform error events by converting Error_Event__e records into persistent Error__c records for tracking and debugging. After insert, it captures key exception details such as message, type, stack trace, method, automation name, and governor limits, ensuring system errors are logged in a structured and reportable format for ongoing monitoring and troubleshooting.

#### `SupportActionTriggerHandler`

Maintains rollup totals of financial or service-based support actions on related Cases. On insert, update, delete, and undelete of `SupportAction__c` records, it recalculates the total value of all associated support actions and updates the corresponding Case field. This ensures accurate, real-time aggregation of support provided per Case, with all processing wrapped in exception logging for reliability.
