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
