# ✨ Flows

The following flows are included with WarriorServe. Review each flow after installation and determine whether to use as delivered or customize for your organization.

---

## 1. AL Get Contact

**Type:** Autolaunched Flow

Used by the **Screen Flow: Intake Guided Entry** to retrieve refreshed Contact data during the intake process for dynamic screen behavior.

### Notes
- Must be activated.
- Intended as a supporting utility flow.
- Not designed as a customization template.

---

## 2. RT Case Referral After Save: Partner Notification

**Type:** Record-Triggered Flow (After Save)

Sends a Case Referral notification to the referred to contact after a Case Referral record is created.

### Notes
- Intended as a template.
- Update email content, recipients, and criteria to match your organization’s process.
- Save changes as a new version and activate.

---

## 3. RT Contact After Save: WWP Registration Requested

**Type:** Record-Triggered Flow (After Save)

Sends a WWP registration notification when a veteran, family member, or caregiver selects **Register me for WWP**.

### Notes
- Intended as a template.
- Update messaging, recipients, and logic as needed.
- Save changes as a new version and activate.

---

## 4. RT Service Record Before Save: Prevent Overlapping Dates

**Type:** Record-Triggered Flow (Before Save)

Prevents overlapping Service Record date ranges and displays a custom error message when conflicting records exist.

### Notes
- Intended as a template.
- Update validation logic or error messaging if needed.
- Save changes as a new version and activate.

---

## 5. Screen Flow: Intake Guided Entry

**Type:** Screen Flow

Guided intake experience that captures key client information, supports a holistic intake process, and provides recommendations based on entered data.

### Notes
- Intended as a template.
- Customize screens, questions, logic, and outcomes to fit your intake model.
- Save changes as a new version and activate.

---

## 6. Screen Flow: Partner Search and Referral Creation

**Type:** Screen Flow

Allows users to search partner organizations in Salesforce and optionally create a Case Referral from the results.

### Notes
- Intended as a template.
- Customize search criteria, screens, and referral behavior as needed.
- Save changes as a new version and activate.