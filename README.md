## MyCreds
A project creating verifiable credentials for the educational records of ARUCC-Canada.

## About this project
The project enables a secure digital wallet (Developed by the MATTR) where university graduates can view and share their official, verified educational credentials anytime, and from anywhere. 

There are various partners and stakeholders involved in bringing this idea to life and developing an innovative platform to deliver value for the education sector in Canada. Following are the main contributors to the project. 

#### ARUCC: 
ARUCC (Association of Registrars of the Universities and Colleges of Canada) is a national body of registrars and enrollment services professionals of recognized colleges and universities. The association is the owner of MyCreds, a platform that offers a document exchange and credential wallet for students and graduates.

#### MATTR:
MATTR is a market leader in providing a platform for offering digital identities and verifiable credentials. The MATTR has taken digital trust and interactions over the internet to the next level contributed to the standards community and shaped the future of the digital identity space.

For this project, the MATTR platform is enabled to support Digitary in shaping up the credential generation, verification, and revocation capabilities.

#### Digitary:
Digitary provides solutions in the educational sector to issue and verify the digital credentials for educational degree certificates, transcripts and other sensitive documents online. 

In this project, the Digitary (In collaboration with the MATTR) is enabling the complete value chain of digital credentials. 

## How to use this project?
This section will cover the details of how this project and code can be utilised.  

## Standards and Specifications 
In this project, there are various standards and specifications which are being used to establish the integrity of the educational credentials.  

- #### Decentralised Identifiers (DIDs) v1.0: 
A globally unique persistent identifier that does not require a centralized registration authority and is often generated and/or registered cryptographically. Decentralized identifiers (DIDs) are a new type of identifier that enables verifiable, decentralized digital identity. A DID refer to any subject (e.g., a person, organization, thing, data model, abstract entity, etc.)

Following are the few benefits associated with DIDs. 

-   DIDs are globally unique, highly available and cryptographically verifiable 
-   A user can prove the ownership of one 
-   Preserves the user privacy, transparency and trust
-   Improve audit trails to support compliance   

For more details about the DID specifications, visit [here](https://www.w3.org/TR/2022/REC-did-core-20220719/). Also, you can watch some videos on the same topic on the MATTR YouTube channel [here](https://www.youtube.com/watch?v=gWgAgpfLEIQ&list=PL1v34OMpKjALowB6oxDYmCvoYfWeiUe_4&index=5)


- #### Verifiable Credentials Data Model v1.1: 

[Verifiable Credentials](https://www.w3.org/TR/vc-data-model/) are a W3C standard data model for expressing cryptographically secure digital credentials on the web.

Though they are both part of the VC data model, [Verifiable Credentials - VCs](https://www.w3.org/TR/vc-data-model/#credentials) are distinct from [Verifiable Presentations - VPs](w3.org/TR/vc-data-model/#presentations). Presentations are typically generated or derived from VCs and presented by credential holders for verification.

The VC data model defines two concrete data syntaxes, JSON and JSON-LD. JSON-LD allows the VC data model to be extensible and interoperable while remaining distributed in its architecture.

Here are the few advantages of having verifiable credentials. 

- Defined by a common standard (W3C) that enhances interoperability  
- Cryptographically secured using digital signatures 
- Provides control over the information sharing  
- Multiple credentials in a single presentation 

To learn more about the VCs data model, refer to the details on W3C [here](https://www.w3.org/TR/vc-data-model/). Watch a few videos on this topic published by the MATTR [here](https://www.youtube.com/watch?v=6H099_hTRc4&list=PL1v34OMpKjALowB6oxDYmCvoYfWeiUe_4&index=6). 

### International organisations supporting digital identities and trust

- #### W3C (World Wide Web Consortium)
The World Wide Web Consortium (W3C) is an international community that develops open standards, protocols and guidelines that ensure the long-term growth of the Web. 

For more details, visit [W3C](https://www.w3.org/) website. 

Below is the list of specifications on which W3C has worked in the space of decentralised identities. 

  - [JSON-LD](https://www.w3.org/TR/json-ld/)
  - [Linked Data Proofs](https://w3c-ccg.github.io/data-integrity-spec/)
  - [Revocation List 2020](https://w3c-ccg.github.io/vc-status-rl-2020/)
  - [Verifiable Credentials Data Model](https://www.w3.org/TR/vc-data-model/)
  - [Verifiable Presentation Request Specification](https://w3c-ccg.github.io/vp-request-spec/)
  - [Confidential Storage](https://identity.foundation/confidential-storage/)

- #### DIF (Decentralised Identity Foundation)
DIF is an engineering-driven organization acting as the center for development, discussion, and management of all the activities required to create and maintain an interoperable & open ecosystem for the decentralized identities. 

Following are the notable specifications from DIF. 

- [DIDComm](https://identity.foundation/didcomm-messaging/spec/)
- [Well Known DID Configuration](https://identity.foundation/.well-known/resources/did-configuration/) 
- [Universal Resolver](https://github.com/decentralized-identity/universal-resolver) 
- [Universal Registrar](https://github.com/decentralized-identity/universal-registrar)
- [Credential Storage](https://identity.foundation/confidential-storage/) 
- [Sidetree Protocol](https://identity.foundation/working-groups/sidetree.html)

- #### IETF (Internet Engineering Task Force) 
The Internet Engineering Task Force (IETF) is a large open international community of network designers, operators, vendors, and researchers concerned with the evolution of Internet architecture and the smooth operation of the Internet.

For more details, please visit [IETF](https://www.ietf.org/) website.  

Following is the list of specifications that IETF has contributed to in terms of identity space.

- [JSON Web Message](https://datatracker.ietf.org/doc/html/draft-looker-jwm-01)
- [JSON Web Encryption (JWE)](https://datatracker.ietf.org/doc/html/rfc7516)
- [JSON Web Key (JWK)](https://datatracker.ietf.org/doc/html/rfc7517)
- [JSON Web Signature (JWS)](https://datatracker.ietf.org/doc/html/rfc7515)

- #### OIDF (OpenID Foundation)
The OpenID Foundation is a non-profit international standardization organization of individuals and companies committed to enabling, promoting and protecting OpenID technologies. 

For more details, please visit [OIDF](https://openid.net/foundation/) website and the specifications below. 

- [OpenID Connect](https://openid.net/connect/)
- [OpenID Connect Credential Provider](https://mattrglobal.github.io/oidc-client-bound-assertions-spec/v0.1/)


## Standard-first Approach 
Standards enable user choice and prevent vendor lock-in, enabling interoperability of data models and protocols for cryptography, messaging, storage, and so much more.

Wherever possible, our products leverage and support existing standards. Where gaps exist, we propose modifications or develop new specifications with our technical community. Our commitment to interoperability reduces risk while future-proofing implementations. 


### Credits
Thank you to all our partners and contributors who have been involved in this project such as [ARUCC](https://arucc.ca/en/), [Digitary](https://www.digitary.net/) and [MATTR](https://mattr.global/). 

### License
Copyright (C) 2021 T-Systems International GmbH and all other contributors

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.

You may obtain a copy of the License at https://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the [LICENSE]() for the specific language governing permissions and limitations under the License.
