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
