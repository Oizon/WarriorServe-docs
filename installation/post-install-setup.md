# ⚡ Post-Install Setup

Complete the following steps after installing WarriorServe.

---

## 1. Assign Administrative Access

Assign the `WarriorServe Configuration` permission set to the primary system administrator responsible for setup and maintenance.

---

## 2. Configure Core Settings

1. Open the **WarriorServe Settings and Tools** app.
2. Enable the features your organization plans to use.
3. Save changes.

Examples may include:
- Enable WarriorServe
- Enable Case Auto Create
- Enable Event Logging
- Enable Task Auto Create
- Advanced integration settings

---

## 3. Create End User Permission Set

Create a permission set for staff users and grant access as needed.

### Recommended App Access
- WarriorServe

### Recommended Object Access
- Account
- Case
- Case Referral
- Contact
- Service Record
- Event Log *(Read Only recommended)*

Adjust Create, Read, Edit, Delete, and field-level security based on your operating model.

---

## 4. Review and Activate Flows

Review each included flow and customize as needed for your organization. If changes are required, save as a new version and activate it.

### Recommended Flows to Review/Activate
- AL Get Contact
- RT Case Referral After Save Partner Notification
- RT Contact After Save WWP Registration Requested
- RT Service Record Before Save Prevent Overlapping Dates
- Screen Flow Intake Guided Entry
- Screen Flow Partner Search and Referral Creation

---

## 5. Configure Intake Quick Actions

Create and place intake actions where users can easily access them.

### Contact
Setup → Object Manager → Contact → Buttons, Links, and Actions → New Action

### Case
Setup → Object Manager → Case → Buttons, Links, and Actions → New Action

### Placement Recommendations
- Add the Intake action to Contact page layouts
- Add the Intake action to Case record pages
- Use Dynamic Actions on Lightning pages when available

### Additional Recommendation
Add the **Refer to AWP** action to Case actions if used by your process.

---

## 6. Configure Partner Search and Referral Actions

Create actions used for referral workflows.

### Case Action
Create a Quick Action on Case for launching referral creation.

### Case Referral List View Button
Create a custom button or link for launching the Case action from related contexts.

### Lightning Record Page
Edit the Case Lightning Record Page:

Related Lists → Case Referrals → Add Action

This allows users to launch referral actions directly from the related list.