### 🛠️ Settings Management

WarriorServe® includes **modular settings components** to configure system behavior via the **WarriorServe Settings and Tools** application.

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
  * VA Facility retrieval options
  * Case Referral Auto Sharing
* **Acknowledgment Required:**

  * Users must confirm a warning prompt before accessing advanced controls.
* When **Enable WarriorServe** is unchecked, all advanced settings are disabled.
* Changes are saved independently of Basic Settings.

#### **About**

* Shows current Organization Type and Environment.
* Includes links for the following:

  * Getting WarriorServe Support.
  * How to check your Installed Version.
  * How to rename object/fields using overrides.

---

More features and configuration options will be appended as additional parts of the WarriorServe system are documented and implemented.
