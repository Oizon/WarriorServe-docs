# 🧠 Lightning Web Components (LWC)

The following Lightning Web Components are included with WarriorServe.

---

## basicSettingManager

Administrative settings component used to manage core feature toggles.

### Functions
- Enable WarriorServe
- Enable Case Auto Create
- Enable Event Logging
- Enable Task Auto Create

### Behavior
- Automatically disables dependent settings when WarriorServe is turned off.

---

## advancedSettingsManager

Administrative settings component for advanced system controls.

### Functions
- Veteran Confirmation settings
- VA Facility retrieval options
- Batch and scheduler limits
- Auto-sharing options

### Behavior
- Requires user acknowledgement before changes can be made.

---

## aboutSettingManager

Informational component that provides context about WarriorServe features, configuration, and environment details.

---

## contactDataIntegrity

Displays Contact data completeness and highlights missing critical information.

### Functions
- Scores overall record completeness
- Identifies missing fields
- Helps users improve data quality before downstream automation

### Notes
Phone, Email, and Service Record data are especially important for Veteran Confirmation processes.

---

## flowPicklist

Reusable Flow component that provides dynamic, record type-dependent picklist values on Flow screens.

### Use Cases
- Guided intake flows
- Dynamic screen forms
- Reusable picklist selection logic across flows

---

## flowRecordNavigator

Reusable Flow component that redirects users to a record after Flow completion.

### Current Usage
- Guided Entry
- Partner Search and Referral Creation

### Use Cases
- Navigate users directly to newly created or selected records
- Improve post-flow user experience