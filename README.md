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

Though they are both part of the VC data model, [Verifiable Credentials - VCs](https://www.w3.org/TR/vc-data-model/#credentials) are distinct from [Verifiable Presentations - VPs](w3.org/TR/vc-data-model/#presentations). Presentations are typically generated or derived from VCs and presented by credential holders for verification.

The VC data model defines two concrete data syntaxes, JSON and JSON-LD. JSON-LD allows the VC data model to be extensible and interoperable while remaining distributed in its architecture.

When combined with DIDs, VCs provide a decentralized data sharing model where interconnected webs of signed and linked data can be used to establish trust across contexts.

Here are the few advantages of having verifiable credentials. 

- Defined by a common standard (W3C) that enhances interoperability  
- Cryptographically secured using digital signatures 
- Provides control over the information sharing  
- Multiple credentials in a single presentation 

To learn more about the VCs data model, refer to the details on W3C [here](https://www.w3.org/TR/vc-data-model/). Watch a few videos on this topic published by the MATTR [here](https://www.youtube.com/watch?v=6H099_hTRc4&list=PL1v34OMpKjALowB6oxDYmCvoYfWeiUe_4&index=6). 

- #### JSON-LD:
JSON-LD is a JSON-based format used to serialize Linked Data. Linked Data plays a very important role when it comes to exchanging verifiable information. JSON-LD is designed to facilitate sharing and discovering data in web-based environments. There are several available guides online that describe JSON-LD in detail. We’re going to focus on two required properties of JSON-LD that consistently show up in the VC data model, namely @context and type. 

Verifiable Credentials make use of JSON-LD to extend the data model to support dynamic data vocabularies and schemas. This allows us to not only use existing JSON-LD schemas but to utilize the mechanism defined by JSON-LD to create and share new schemas as well. To a large extent this is what JSON-LD was designed for; the adoption and reuse of common data vocabularies.

For more details, refer to the specification of [JSON-LD](https://www.w3.org/TR/json-ld11/). 

### International organisations supporting digital identities and trust

- #### W3C (World Wide Web Consortium)
The World Wide Web Consortium (W3C) is an international community that develops open standards to ensure the long-term growth of the Web. W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work

For more details, visit [W3C](https://www.w3.org/) website. 

Below is the list of specifications on which W3C has worked in the space of decentralised identities. 

  - [JSON-LD](https://www.w3.org/TR/json-ld/)
  - [Linked Data Proofs](https://w3c-ccg.github.io/data-integrity-spec/)
  - [Revocation List 2020](https://w3c-ccg.github.io/vc-status-rl-2020/)
  - [Verifiable Credentials Data Model](https://www.w3.org/TR/vc-data-model/)
  - [Verifiable Presentation Request Specification](https://w3c-ccg.github.io/vp-request-spec/)
  - [Confidential Storage](https://identity.foundation/confidential-storage/)

- #### DIF (Decentralised Identity Foundation)
DIF is an engineering-driven organization acting as the center for development, discussion, and management of all activities required to create and maintain an interoperable & open ecosystem for the decentralized identity stack. DIF has the capability to set up IPR protected working groups, deliver specs and standards, and offer infrastructure for the community.

Following are the notable specifications from DIF. 

- [DIDComm 2.0](https://identity.foundation/working-groups/did-comm.html)
- [Well Known DID Configuration](https://identity.foundation/.well-known/resources/did-configuration/) 
- [Universal Resolver](https://github.com/decentralized-identity/universal-resolver) 
- [Universal Registrar](https://github.com/decentralized-identity/universal-registrar)
- Identity Hubs 
- [Sidetree Protocol](https://identity.foundation/working-groups/sidetree.html)
- DID SIOP (Self-Issued OpenID)

- #### IETF (Internet Engineering Task Force) 
The Internet Engineering Task Force (IETF) is a large open international community of network designers, operators, vendors, and researchers concerned with the evolution of Internet architecture and the smooth operation of the Internet.

For more details, please visit [IETF](https://www.ietf.org/) website.  

Following is the list of specifications that IETF has contributed to in terms of identity space.

- [JSON Web Message](https://datatracker.ietf.org/doc/html/draft-looker-jwm-01)
- [JSON Web Encryption (JWE)](https://datatracker.ietf.org/doc/html/rfc7516)
- [JSON Web Key (JWK)](https://datatracker.ietf.org/doc/html/rfc7517)
- [JSON Web Signature (JWS)](https://datatracker.ietf.org/doc/html/rfc7515)


- #### OIDF (OpenID Foundation)
The OpenID Foundation (OIDF) promotes, protects and nurtures the OpenID community and technologies. The OpenID Foundation is a non-profit international standardization organization of individuals and companies committed to enabling, promoting and protecting OpenID technologies. Formed in June 2007, the Foundation serves as a public trust organization representing the open community of developers, vendors, and users. OIDF assists the community by providing needed infrastructure and helping in promoting and supporting the expanded adoption of OpenID. This entails managing intellectual property and brand marks as well as fostering viral growth and global participation in the proliferation of OpenID.

For more details, please visit [OIDF](https://openid.net/foundation/) website and the specifications below. 

- [OpenID Connect](https://openid.net/connect/)
- [OpenID Connect Credential Provider](https://mattrglobal.github.io/oidc-client-bound-assertions-spec/v0.1/)


### Credential value chain
- ###### Credential (Semantic) Generation/Issuance 

A Verifiable Credential (VC or just Credential) in a JSON-LD format adhering to the W3C VC Data Model spec. The schema is always required for the reference of credentials. The values required by the operation are validated where available and used to construct the Verifiable Credential. The Credential is issued using JSON-LD with linked data proofs, the type values of the Credential and the Subject Claims must be represented by a schema in @context. 

If you wish to issue a ZKP-enabled Verifiable Credential, the provided **issuer id** must be a did:key with a key type of **bls12381g2**. The platform will automatically detect this capability and issue a ZKP-enabled BBS+ credential


- ###### Verify credentials 
Send any JSON-LD Verifiable Credential that conforms to the W3C Verifiable Credentials data model to perform verification checks and return a response:

- Issuer DID can be resolved
- JSON-LD context is valid for subject claims
- Proof is valid & the credential has not been tampered with
- Is not in a revoked status on a RevocationList2020 This endpoint can be used to check any Credentials issued by any service provider. 

- Credential Verification 
- Claim credentials 

- Credential Schema 
- Format 
- Vocab 
[Support interoperability]

- Associated Specs for issuance, verification and claim 

## Standard-first Approach 

Standards enable user choice and prevent vendor lock-in, enabling interoperability of data models and protocols for cryptography, messaging, storage, and so much more.

Wherever possible, our products leverage and support existing standards. Where gaps exist, we propose modifications or develop new specifications with our technical community. Our commitment to interoperability reduces risk while future-proofing implementations. 


## Specs, Protocols, and Standards
The decentralised identity/Self-sovereign Identity ecosystem has various building blocks which enable interactions between various parties. 

1. Protocols for Secure Connections 
2. Protocols for Secure Data
3. Public Key Registry


1. A standard, open protocol for establishing unique, private and secure connections between multiple parties without requiring the assistance of an intermediary “connection broker,” like Google, WhatsApp, an email provider, or a phone carrier. Once two parties have exchanged the DIDs, they can communicate securely facilitated by an umbrella protocol called DIDComm. 

2. 



Most specifications related to decentralized identity follow a similar path on the road toward standardization. Typically the stages are:

1. **Draft** → serves as a proposal for a new standard, typically done by one entity
2. **Community Group** → peer-reviewed by community members, adopted and developed by multiple parties in an open environment
3. **Working Group** → dedicated and chartered group with a mandate to complete a specification
4. **Standard** → completed specification, widely adopted and used by many industry partners


##### Supported Standards Status
With respect to each standard, the status indicates the current and likely continued future conformance of MATTR VII to the particular version of the standard indicated. The status is influenced by the product roadmap, future iterations of the standard itself, the changing standards landscape, and other such factors.

Support statuses are categorized as either:

1. **Stable** - MATTR VII conforms to the standard and conformance is expected to continue into the foreseeable future. Deprecation of support for the standard and/or adoption of a new version is unlikely over any reasonable time horizon.

2. **Provisionary** - MATTR VII conform to the standard however deprecation of support for the standard and/or adoption of a new version is possible within the foreseeable future.

3. **Deprecated** - MATTR VII previously conformed to the standard, the support for which has now ceased.


##### Format, Schema and Vocab 

- **DID Format**

```
did:key:z6MkjBWPPa1njEKygyr3LR3pRKkqv714vyTkfnUdP6ToFSH5
```

- **Format of Web Credentials/ Issuance**

```
{
  "id": "c6667bb7-9442-49a5-bb0b-fce269e97fc6",
  "credential": {
    "@context": [
      "https://www.w3.org/2018/credentials/v1",
      {
        "@vocab": "https://w3id.org/security/undefinedTerm#"
      },
      "https://schema.org"
    ],
    "type": [
      "VerifiableCredential",
      "CourseCredential"
    ],
    "issuer": {
      "id": "did:key:z6MkndAHigYrXNpape7jgaC7jHiWwxzB3chuKUGXJg2b5RSj",
      "name": "tenant"
    },
    "issuanceDate": "2021-07-26T01:05:05.152Z",
    "credentialSubject": {
      "id": "did:key:z6MkfxQU7dy8eKxyHpG267FV23agZQu9zmokd8BprepfHALi",
      "givenName": "Chris",
      "familyName": "Shin",
      "educationalCredentialAwarded": "Certificate Name"
    },
    "proof": {
      "type": "Ed25519Signature2018",
      "created": "2021-07-26T01:05:06Z",
      "jws": "eyJhbGciOiJFZERTQSIsImI2NCI6ZmFsc2UsImNyaXQiOlsiYjY0Il19..o6hnrrWpArG8LQz2Ex_u66_BtuPdp3Hkz18nhNdNhJ7J1k_2lmCCwsNdmo-kNFirZdSIMzqO-V3wEjMDphVEAA",
      "proofPurpose": "assertionMethod",
      "verificationMethod": "did:key:z6MkndAHigYrXNpape7jgaC7jHiWwxzB3chuKUGXJg2b5RSj#z6MkndAHigYrXNpape7jgaC7jHiWwxzB3chuKUGXJg2b5RSj"
    }
  },
  "issuanceDate": "2021-07-26T01:05:05.152Z"
}

```

- **Verify the Credentials**

**REQUEST:** 
```
{
  "id": "c6667bb7-9442-49a5-bb0b-fce269e97fc6",
  "credential": {
    "@context": [
      "https://www.w3.org/2018/credentials/v1",
      {
        "@vocab": "https://w3id.org/security/undefinedTerm#"
      },
      "https://schema.org"
    ],
    "type": [
      "VerifiableCredential",
      "CourseCredential"
    ],
    "issuer": {
      "id": "did:key:z6MkndAHigYrXNpape7jgaC7jHiWwxzB3chuKUGXJg2b5RSj",
      "name": "tenant"
    },
    "issuanceDate": "2021-07-26T01:05:05.152Z",
    "credentialSubject": {
      "id": "did:key:z6MkfxQU7dy8eKxyHpG267FV23agZQu9zmokd8BprepfHALi",
      "givenName": "Chris",
      "familyName": "Shin",
      "educationalCredentialAwarded": "Certificate Name"
    },
    "proof": {
      "type": "Ed25519Signature2018",
      "created": "2021-07-26T01:05:06Z",
      "jws": "eyJhbGciOiJFZERTQSIsImI2NCI6ZmFsc2UsImNyaXQiOlsiYjY0Il19..o6hnrrWpArG8LQz2Ex_u66_BtuPdp3Hkz18nhNdNhJ7J1k_2lmCCwsNdmo-kNFirZdSIMzqO-V3wEjMDphVEAA",
      "proofPurpose": "assertionMethod",
      "verificationMethod": "did:key:z6MkndAHigYrXNpape7jgaC7jHiWwxzB3chuKUGXJg2b5RSj#z6MkndAHigYrXNpape7jgaC7jHiWwxzB3chuKUGXJg2b5RSj"
    }
  }
}
```

**RESPONSE:**

```
{
  "verified": true
}

```

- **Create a presentation template:**

**REQUEST:**

```
{
    "domain":"YOUR_TENANT_SUBDOMAIN.vii.mattr.global",
    "name":"certificate-presentation",
    "query":[{
        "type": "QueryByExample",
        "credentialQuery": [{
            "required": true,
            "reason": "Please provide your certificate.",
            "example": {
                "@context": ["https://schema.org"],
                "type": "CourseCredential",
                "trustedIssuer": [{
                    "required": true,
                    "issuer": "did:key:z6MkjBWPPa1njEKygyr3LR3pRKkqv714vyTkfnUdP6ToFSH5"
                }]
            }
        }]
    }]
}
```

**RESPONSE:**

```

{
    "id": "f95e71b0-9bdf-11ea-aec9-3b5c35fc28c8",
    "domain": "YOUR_TENANT_SUBDOMAIN.vii.mattr.global",
    "query": [
        {
            "type": "QueryByExample",
            "credentialQuery": [
                {
                    "required": true,
                    "reason": "Please provide your certificate.",
                    "example": {
                        "@context": [
                            "https://schema.org"
                        ],
                        "type": "CourseCredential",
                        "trustedIssuer": [
                            {
                                "required": true,
                                "issuer": "did:key:z6MkjBWPPa1njEKygyr3LR3pRKkqv714vyTkfnUdP6ToFSH5"
                            }
                        ]
                    }
                }
            ]
        }
    ],
    "name": "certificate-presentation"
}

```

- **Revokable Credential** 

```
 {

  "@context": [

    "https://www.w3.org/2018/credentials/v1",

    "https://schema.org",

    "https://w3id.org/vc-revocation-list-2020/v1"

  ],

  "type": [ ... ],

  "credentialStatus": {

    "id": "https://tenant.vii.mattr.global/core/v1/revocation-lists/cc641396-3750-43c8-b8b8-f30d74eb3fb3#4",

    "type": "RevocationList2020Status",

    "revocationListIndex": "4",

    "revocationListCredential": "https://tenant.vii.mattr.global/core/v1/revocation-lists/cc641396-3750-43c8-b8b8-f30d74eb3fb3"

  },

  "issuer": {

    "id": "did:key:z6MkndAHigYrXNpape7jgaC7jHiWwxzB3chuKUGXJg2b5RSj",

    "name": "tenant.vii.mattr.global"

  },

  "credentialSubject": { ... },

  "issuanceDate": "...",

  "proof": { ... }

}

```



### Project learnings 
Any project learnings can be captured here. 


### Support 
This section should cover the support details 


### Credits
Thank you to all our partners and contributors who have been involved in this project such as [ARUCC](https://arucc.ca/en/), [Digitary](https://www.digitary.net/) and [MATTR](https://mattr.global/). 

### License
Copyright (C) 2021 T-Systems International GmbH and all other contributors

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.

You may obtain a copy of the License at https://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the [LICENSE]() for the specific language governing permissions and limitations under the License.
