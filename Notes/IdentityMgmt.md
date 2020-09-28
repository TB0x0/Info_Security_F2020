# Identity Management and Access control


The 3 A's authentication, authorization, accountability should also include identification

## Identification

We need some way to identify users. Most common on the internet is a user ID. To identify a subject just ask for user ID. After that is received the authentication process verifies the identification of the subject.

Authentication information must be prepared in advance and stored somewhere like an authentication server so that it can be referenced.

**Identity Establishment**
 - Applies to subjects and objects
 - Performed by trusted 3rd parties or in-house
 - Might establish and/or rely on 'seminal' documents (original documents like registrations, certificates)

 **The Reference Monitor**  
  Enforces access control rules and manages the process
  - **Isolation** - Must be isolated (tamper-proof)
  - **Completeness** - Must be impossible to bypass and invoked for every decision
  - **Verifiability** - Must be thoroughly tested
  (My examples: Active Directory, Firewalls)

  Access Control mitigates most disclosure incidents (viewing allowed only if access policy allows it) and most unintentional data integrity incidents (read, write, edit permissions are controlled)

   - May not help against DOS, availability attacks, or trojans that leverage user permissions.

## Authentication

>Something you know<br>
Something you have<br>
Something you are<br>
Something you do

### Something you know

Passwords: static passwords or passphrases, one-time passwords, dynamic passwords

 **Password Control**

 - Don't write down passwords and put them on monitors
 - Don't use patterns or predictable words

 *NIST Guidance:*

 NIST SP 800-63-3 June 2017:

 - 8 character minimum, 64 maximum
 - disallow common passwords
 - allow all printing characters and spaces

 *Update*
 - Should offer to display secret and re-hide after a period. Improves accuracy and UX.

### Something you have

**Synchronous token**
 - Synchronized with a central server
 - Values change over time or by counter
 - Examples: SecureID, GoogleAuth

**Asynchronous token**
 - Stand alone token-smart card (Common Access Card)
 - Requires PIN

### Something you are

**Biometrics**

*Physiological*
- Face, fingerprint, hand, iris, DNA

*Behavioral*
- Keystroke, signature, voice

**Accuracy of Biometrics**
- False Reject Rate (FRR) - Actual user gets rejected (You have to redo fingerprint because it didn't work the first time)
- False Accept Rate (FAR) - A non-authorized user gets access to the system
- Crossover Error Rate (CER) - Balanced area for optimal security and best user interaction.

![Biometric Error Rate](/res/BiometricAccuracy.png)



## Authentication Helpers

Added measures and tools that help with authentication

- Google Authenticator, DUO
- Voice printing
- Location (zip, gps)

## Decentralized Access Control

- Local sites maintain independent systems to provide more local control over data

**Access aggregation** - occurs when a user gains more access to more systems

**Authorization creep** - Users gain more entitlement without shedding the old ones ( defeats least privilege and separation of duties )

## Authorization Models

- Discretionary Access Control - Owners have full control of assets and can share them as they like

- Mandatory Access Control - Subjects have clearance, objects have labels

- Non-Discretionary Access Control -

  - Role-Based Access Control - Subjects have roles and permissions are assigned to roles

  - Task-based Access Control - Focus on tasks subjects must perform
