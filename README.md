## MyCreds
A project for creating verifiable credentials of educational records for ARUCC-Canada

## About this project
The project enables a secure digital wallet (i.e. MyCreds) where graduates can view and share their official, verified educational credentials anytime, and from anywhere. 
There are various government bodies, partners and stakeholders are involved in brining this idea to life and making the MyCreds an innovative platform to deliver value in the Canadian educational sector. 

#### ARUCC: 
ARUCC (Association of Registrars of the Universities and Colleges of Canada) which is a national body of registrars and enrollments services professionals of recognized colleges and universities. The association is the owner of the MyCreds, a platform which offers a document exchange and credential wallet for students and graduates. This initiative is being collaboration i

#### MATTR: 
MATTR is a market leader in providing a platform for offering digital identities and verifiable credentials. MATTR has taken digital trust and interactions over the internet to the next level, contributed in the standards community and shaping up the future of the digital identity space.   

#### Digitary:
Digitary provides solution in educational sector to issue and verify the digital credentials for the educational degree certificates, transcripts and other sensitive documents online. 

## How to use this project?
Section covering the details of how this project and code can be utilised 

### Standards and Specifications 
In this project, there are various standards and specifications which are being used to establish the integrity of the educational credentials.  

- #### Decentralised Identifiers (DIDs) v1.0: 
A globally unique persistent identifier that does not require a centralized registration authority and is often generated and/or registered cryptographically. Decentralized identifiers (DIDs) are a new type of identifier that enables verifiable, decentralized digital identity. A DID refers to any subject (e.g., a person, organization, thing, data model, abstract entity, etc.)

For more details about the DID specifications, visit [here](https://www.w3.org/TR/2022/REC-did-core-20220719/). Also you can watch some videos on the same topic at MATTR YouTube channel [here](https://www.youtube.com/watch?v=gWgAgpfLEIQ&list=PL1v34OMpKjALowB6oxDYmCvoYfWeiUe_4&index=5)


A sample DID document is presented below for reference.

```
{
  "@context": [
    "https://www.w3.org/ns/did/v1",
    "https://w3id.org/security/suites/ed25519-2020/v1"
  ]
  "id": "did:example:123456789abcdefghi",
  "authentication": [{
    
    "id": "did:example:123456789abcdefghi#keys-1",
    "type": "Ed25519VerificationKey2020",
    "controller": "did:example:123456789abcdefghi",
    "publicKeyMultibase": "zH3C2AVvLMv6gmMNam3uVAjZpfkcJCwDwnZn6z3wXmqPV"
  }]
}
```

- #### Verifiable Credentials Data Model v1.1: 

[Verifiable Credentials](https://www.w3.org/TR/vc-data-model/) are a W3C standard data model for expressing cryptographically secure digital credentials on the web.

Though they are both part of the VC data model, [Verifiable Credentials - VCs](https://www.w3.org/TR/vc-data-model/#credentials) are distinct from [Verifiable Presentations - VPs](w3.org/TR/vc-data-model/#presentations). Presentations are typically generated or derived from VCs and presented by credential holders for the purposes of verification.

The VC data model defines two concrete data syntaxes, JSON and JSON-LD. JSON-LD allows the VC data model to be extensible and interoperable while remaining distributed in its architecture.

When combined with DIDs, VCs provide a decentralized data sharing model where interconnected webs of signed and linked data can be used to establish trust across contexts.

To learn more about the VCs data model, refer to the details on W3C [here](https://www.w3.org/TR/vc-data-model/). Watch a few videos on this topic published by MATTR [here](https://www.youtube.com/watch?v=6H099_hTRc4&list=PL1v34OMpKjALowB6oxDYmCvoYfWeiUe_4&index=6). 

- #### JSON-LD:
JSON-LD is a JSON-based format used to serialize Linked Data. Linked Data plays a very important role when it comes to exchanging verifiable information. JSON-LD is designed to facilitate sharing and discovering data in web-based environments. There are several available guides online that describe JSON-LD in detail. We’re going to focus on two required properties of JSON-LD that consistently show up in the VC data model, namely @context and type. 

For more details, refer to the specification of [JSON-LD](https://www.w3.org/TR/json-ld11/). 

### International organisations supporting digital identities and verifiable credentials  

- #### W3C (World Wide Web Consortium)
The World Wide Web Consortium (W3C) is an international community that develops open standards to ensure the long-term growth of the Web. W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work

For more details, visit [W3C](https://www.w3.org/) website. 

Below is the list of specifications which W3C has worked in the space of decentralised identities. 

  - [JSON-LD](https://www.w3.org/TR/json-ld/)
  - [Linked Data Proofs](https://w3c-ccg.github.io/data-integrity-spec/)
  - [Revocation List 2020](https://w3c-ccg.github.io/vc-status-rl-2020/)
  - [Verifiable Credentials Data Model](https://www.w3.org/TR/vc-data-model/)
  - [Verifiable Presentation Request Specification](https://w3c-ccg.github.io/vp-request-spec/)
  - [Confidential Storage](https://identity.foundation/confidential-storage/)


- #### IETF (Internet Engineering Task Force) 
The Internet Engineering Task Force (IETF) is a large open international community of network designers, operators, vendors, and researchers concerned with the evolution of the Internet architecture and the smooth operation of the Internet.

For more details, please visit [IETF](https://www.ietf.org/) website.  

Following is the list of specifications which IETF has contributed to in terms of identity space.

- [JSON Web Message](https://datatracker.ietf.org/doc/html/draft-looker-jwm-01)
- [JSON Web Encryption (JWE)](https://datatracker.ietf.org/doc/html/rfc7516)
- [JSON Web Key (JWK)](https://datatracker.ietf.org/doc/html/rfc7517)
- [JSON Web Signature (JWS)](https://datatracker.ietf.org/doc/html/rfc7515)


- #### OIDF (OpenID Foundation)
The OpenID Foundation (OIDF) promotes, protects and nurtures the OpenID community and technologies. The OpenID Foundation is a non-profit international standardization organization of individuals and companies committed to enabling, promoting and protecting OpenID technologies. Formed in June 2007, the Foundation serves as a public trust organization representing the open community of developers, vendors, and users. OIDF assists the community by providing needed infrastructure and help in promoting and supporting expanded adoption of OpenID. This entails managing intellectual property and brand marks as well as fostering viral growth and global participation in the proliferation of OpenID.

For more details, please visit [OIDF](https://openid.net/foundation/) website and the specifications below. 

- [OpenID Connect](https://openid.net/connect/)
- [OpenID Connect Credential Provider](https://mattrglobal.github.io/oidc-client-bound-assertions-spec/v0.1/)


### Project learnings 
Any project learnings can be captured here. 


### Support 
Section covering the support details 


### Credits
Thank you to all our partners and contributors who have been involved in this project such as [ARUCC](https://arucc.ca/en/), [Digitary](https://www.digitary.net/) and [MATTR](https://mattr.global/). 

### License
Copyright (C) 2021 T-Systems International GmbH and all other contributors

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.

You may obtain a copy of the License at https://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the [LICENSE]() for the specific language governing permissions and limitations under the License.
