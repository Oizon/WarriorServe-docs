# 🧰 Services & Utilities

The following Apex services and utility classes support WarriorServe automation, integrations, logging, and configuration.

---

## VAFacilitiesService
**Type:** Queueable, Allows Callouts

Retrieves nearby VA facilities from an external source and stores facility records in Salesforce for search, referral workflows, and reporting.

### Use Cases
- VA facility lookup
- Referral destination records
- Local facility data synchronization

---

## VeteranConfirmationStatus
**Type:** Queueable, Allows Callouts

Verifies veteran status through an external validation service and updates Contact records based on returned results.

### Possible Status Values
- Confirmed — Person is a Title 38 veteran
- Not Found in VA Records — Person was not found in the VA system
- Not Eligible (Not Title 38) — Person is a veteran but is not Title 38 eligible
- Requires VA Review — Status could not be determined automatically
- Verification Error — An error occurred during verification
- Verification Not Attempted — Default status; verification has not been run

---

## EventLogUtility

Creates and reads `EventLog__c` records used for Contact timelines, change history, and operational auditing.

### Use Cases
- Timeline displays
- Key field change tracking
- Historical review

---

## HandleException

Centralized error handling utility for capturing exceptions across synchronous and asynchronous processes.

### Functions
- Standardized error logging
- Context capture
- Async-safe exception handling

---

## MetricsGenerator
**Type:** Schedulable

Creates periodic snapshots in `Metric__c` for dashboards, KPI reporting, and trend analysis.

### Use Cases
- Executive reporting
- Operational metrics
- Historical performance tracking

---

## SettingsManagerController
**Type:** AuraEnabled Apex Controller

Server-side controller used by WarriorServe settings Lightning Web Components.

### Use Cases
- Read settings
- Save settings
- Support admin configuration UI

---

## CollectionUtils

Shared helper methods for working with Lists, Sets, and Maps across Apex logic.

### Use Cases
- Collection transformations
- Reusable helper logic
- Cleaner trigger and service code

---

## PostInstall
**Type:** InstallHandler

Runs post-install initialization tasks after package installation.

### Functions
- Seed default data
- Prepare settings
- Run startup configuration logic