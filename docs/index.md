This is a preliminary draft of the ToIP Governance Architecture TSS (ToIP Standard Specification), a Draft Deliverable of the GSWG. 

###Contributors
To comply with the intellectual property rights protections in the charter of the ToIP Foundation (as required by all Joint Development Foundation projects hosted the Linux Foundation), all contributors to this Pre-Draft Deliverable MUST be current members of the ToIP Foundation and the Governance Stack Working Group (GSWG). The following contributors each certify that they meet this requirement:

* Drummond Reed, Evernym
* Scott Perry, Scott S. Perry CPA PLLC

###Terminology
In this document, the key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).

All other terms in First Letter Capitals will be defined in the Governance Glossary to be published by the Concepts and Terminology Working Group.

###Purpose
The purpose of this TSS is to specify the standard requirements that apply to all ToIP-compatible governance frameworks (GF) regardless of their layer in the ToIP Stack. 

Note: The technical counterpart to this TSS is the ToIP Technical Architecture TSS.

###Motivations
The overall purpose of the ToIP Governance Stack is to enable users of the ToIP Technology Stack to make Transitive Trust decisions based on Governance Frameworks that are both human-readable and machine-verifiable. While Governance Frameworks can be specialized for all four layers of the ToIP Stack, certain requirements apply to all ToIP-Compliant Governance Frameworks regardless of layer. The goal of this specification is to specify all of those requirements in a single specification. 

###ToIP Governance Metamodel 
The purpose of the ToIP Governance Metamodel is to provide an overall template for ToIP-Compliant Governance Frameworks from which the GSWG will then develop layer-specific templates.

The ToIP Governance Metamodel is currently defined on its [own wiki page](https://wiki.trustoverip.org/display/HOME/ToIP+Governance+Metamodel). The contents of that page will be incorporated into this section of the TSS.

###Identification Requirements
To support Transitive Trust across trust boundaries, ToIP-Compliant Governance Frameworks (GF) need to provide standard, persistent, verifiable identification of themselves, their Governance Authorit(ies), their Controlled Documents, and the ToIP Roles, Credentials, and other components they define.

The following MUST have Public Decentralized Identifiers (DIDs) compliant with the ToIP Technology Stack:

* Governance Authority (GA)
* Master Document
* All Participants fulfilling Roles defined in the GF (e.g., Issuers, Stewards, Member Directories)

The following SHOULD have Public DID URLs compliant with the ToIP Technology Stack:

* Each Controlled Document
* Each Policy or other reference-able subcomponent of a Controlled Document
* Verification Requirements

To support Transitive Trust, the following verification requirements apply to ToIP-Compliant Governance Frameworks (GF): 

* The GA MUST publish a Digital Signature over the hash of the current version of its Master Document in its current DID Document.
* The GA SHOULD issue VCs to all Participants verifying the GF role played by the Participant.
* If the GA specifies certification policies, Certification Authorities SHOULD issue Certification VCs to Holders as directed by the GF.
* GA SHOULD consider publishing Certification VCs to a Credential Registry and/or a Member Directory.
* Transparency Requirements

To support Transitive Trust, a publicly-available ToIP-Compliant Governance Framework: 

* MUST be published on the Web.
* MUST publish its DID URL in its DID Document.
* MUST publish its Public Keys in its DID Document.
* MUST publish its Public Service Endpoints in its DID Document.
* Equity, Accessibility, and Inclusion Requirements

To support Transitive Trust, a publicly-available ToIP-Compliant Governance Framework:

* SHOULD be published in all human languages spoken by its Trust Community.
* SHOULD be accessible under the W3C Accessibility Guidelines.
* SHOULD include provisions for digital guardianship if applicable to its Trust Community.
* SHOULD NOT discriminate against legitimate members of its Trust Community.

###Technical Interoperability Requirements
To support the interoperability necessary for Transitive Trust, a publicly-available ToIP-Compliant Governance Framework:

* MUST specify technical interoperability using ToIP Standard Specification (TSS) whenever possible.
* SHOULD specify interoperability using a ToIP Interoperability Profile (TIP) whenever a TSS is not yet available.

