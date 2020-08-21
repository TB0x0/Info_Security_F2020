# Identity Management and Access control

### Access Control

The 3 A's authentication, authorization, accountability should also include identification

#### Identification

We need some way to identify users. Most common on the internet is a user ID. To identify a subject just ask for user ID. After that is received the authentication process verifies the identification of the subject.

Authentication information must be prepared in advance and stored somewhere like an authentication server so that it can be referenced.

- Identity Establishment:
 - Applies to subjects and objects
 - Performed by trusted 3rd parties or in-house
 - Might establish and/or rely on 'seminal' documents (original documents like registrations, certificates)

 - The Reference Monitor:
  - Enforces access control rules and manages the process
  - **Isolation** - Must be isolated (tamper-proof)
  - **Completeness** - Must be impossible to bypass and invoked for every decision
  - **Verifiability** - Must be thoroughly tested
  (My examples: Active Directory, Firewalls)

  - Access Control mitigates most disclosure incidents (viewing allowed only if access policy allows it) and most unintentional data integrity incidents (read, write, edit permissions are controlled)

   - May not help against DOS, availability attacks, or trojans that leverage user permissions.

#### Authentication

- *Something you know
- Something you have
- Something you are
- Something you do*