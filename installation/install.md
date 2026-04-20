### 🛠️ Installation & Configuration Requirements

Before installing WarriorServe®, complete the following steps to ensure the package deploys and functions correctly.

### Prerequisites (Before Installing the Package)

1. **Enable My Domain**

  - In Salesforce Setup:
    - Go to: `Setup → Company Settings → My Domain`
    (**Ensure you choose a domain you are comfortable making public.**)

2. **Enable Digital Experiences (Experience Cloud)**

  - In Salesforce Setup:
    - Go to: `Setup → Digital Experiences → Settings`
    - Click: **Enable Digital Experiences**

3. **Configure Default External Access (OWD)**

  - In Salesforce Setup
    - Go to: `Setup  → Sharing Settings → Edit
    - **Contact Internal**: Any except `Controlled by Parent`
    - **Contact External**: `Private`
    - **Case External**: `Private`
 
4. **Enable Folders and Enhanced Sharing**
  - In Salesforce Setup:
    - Go to: `Setup → Lightning Email Templates`
    - Toggle On: **Folders and Enhanced Sharing**

4. **Install Nonprofit Success Pack (NPSP)** (Optional)

  Allows multi-phone/email per contact and more Do Not Contact Messaging

### 🚀 Installation

1. **Log Into Org**

  - While logged into org
    - Install `WarriorServe®`
    - adjust URL to the following: `https://login.salesforce.com/packaging/installPackage.apexp?p0=XXXXXXXXXXXX`
