# ✅ Validation Rules

The following validation rules help maintain data quality and enforce key business requirements within WarriorServe.

---

## Case Referral

### `VR01_CRE_ValidEmailRequiredForContacts`
Ensures the referred Contact has a valid email address before referral processing.

### `VR02_CRE_ContactConsentMissing`
Requires an approved consent status on the Contact before information can be shared.

### `VR03_CRE_ContactMustBeFromTheAccount`
Prevents selecting a referred Contact who is not associated with the selected Account.

### `VR04_CRE_PreventDoNotEmailChanges`
Prevents changes to Do Not Email fields after the Case Referral has been created.

---

## Contact

### `VR01_CON_FirstNameRequired`
Prevents saving a Contact record without a first name.

---

## Service Record

### `VR01_SER_ValidateEnlistDate`
Prevents saving a Service Record when the individual would be younger than 15 at service start.

### `VR02_SER_ActiveWithServiceEndDate`
Prevents an active Service Record from having a service end date.

### `VR03_SER_EndDateLaterThanStartDate`
Prevents a Service Record end date from occurring before the start date.

### `VR04_SER_NotActiveNoEndDate`
Prevents saving a non-active Service Record without a service end date.

---

## Support Action

### `VR01_SuA_PreventNegativeAmount`
Prevents saving a Support Action with a negative amount.