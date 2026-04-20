##### Validation Rules:

* **VR01\_CRE\_ValidEmailRequiredForContacts:** Ensures the referred contact has a valid email.
* **VR02\_CRE\_ContactConsentMissing:** Requires consent to share information on the contact record.
* **VR03\_CRE\_ContactMustBeFromTheAccount:** Prevents referring contacts who are not part of the case's account.
* **VR04\_CRE\_PreventDoNotEmailChanges:** Prevents changing the Do Not Email Fields after creation.
* **VR01\_CON\_FirstNameRequired:** Prevents saving a contact record if they do not have a first name.
* **VR02\_CON\_DisallowNeedsChangeAfterIntake:** Prevents changing the intial needs after the first day of the contact being created.
* **VR01\_SER\_ValidateEnlistDate:** Prevents creating a service record where someone is listed as under 15 years old upon service starting.
* **VR02\_SER\_ActiveWithServiceEndDate:** Prevents end date if service says there should be one yet.
* **VR03\_SER\_EndDateLaterThanStartDate:** Prevents a service record where they end before starting.
* **VR04\_SER\_NotActiveNoEndDate:** Presents saving a service record not active without an end date.
* **VR01\_SuA\_PreventNegativeAmount:** Prevents inserting a negative amount.