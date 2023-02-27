## ARUCC Ecosystem 

The MyCreds<sup>TM</sup> platform, provided by Digitary is being extended to support the issuance of micro credentials, which are represented as W3C Verifiable Credentials.  
The technology platform underpinning this new capability on the MyCreds<sup>TM</sup> platform is called MATTR VII, a dedicated decentralized identity and verifiable credential lifecycle management platform.  

Using the MATTR VII capability, the MyCreds<sup>TM</sup> platform will now be able to issue education awards as digitally verifiable credentials that can be claimed into secure wallets by learners. 
Industry Partners can also utilize MATTR VII capability to request credentials from learners and verifier their authenticity and data integrity. 

This short guide covers the specifics of the onboarding processes for verifier within the MyCreds<sup>TM</sup> platform and wider ARUCC verifier network. 

### Prerequisites  

- Agreeing to the ARUCC Industry Partner Service Terms for MyCreds<sup>TM</sup> Virtual Skills Passport Verification Service. 
- Signed up / provisioned access to a MATTR VII tenant. 
- Ability to orchestrate API driven flows to call the MATTR VII issuance and/or verification capability. 
- Ability to securely store, and use ```client_credentials``` and ```client_secret``` to obtain an access token which will be used to authenticate and access MATTR VII APIs. 
- Access to the MATTR developer or compatible wallet that can claim/receive, store, present verifiable credentials, that are bound to the wallet using the holders DID. 
- Access to a domain/subdomain that can be bound to the provisioned MATTR VII tenant as a custom domain to represent a user-friendly and trusted name/brand for credential issuer or verifier. 

### ARUCC Verifier setup

Before a verifier (or industry partner), can use MyCreds<sup>TM</sup> to verify a learner's credential, they need to be set up with certain prerequisites. These prerequisites are outlined below:

Here are some of the prerequisites required to set up a verifier before credential information is verified. 

1. __Tenant Setup__: 
- A new tenant is created with the necessary information that can be initiated with the MATTR. For more information, see the [Tenant Setup](https://learn.mattr.global/tutorials/essentials/tenant-setup).
Following information is required to set up a tenant. 

   - Preferred tenant prefix/subdomain (i.e name of company)
   - Type of tenant (UAT or Production) 
   - Industry Partners are recommended to have two tenants (1 x UAT, 1 x Production) 
   - __Note__. The prefix/subdomain will be combined with the tenant type to represent the MATTR VII tenant name i.e. <prefix/subdomain>.<tenant-type> 
   - Issuer Organization Name 
   - Contact Name 
   - Contact Email Address 
   - Tenant Region (Australia, Canada, US) 

- MATTR will provision the tenant and supply the requestor with the required information, including API client and secret. This information will be sent via a secured channel or one-time access link. 

- It is assumed that each verifier will utilize a DID:Web to represent themselves. This should be setup by following the MATTR learn tutorial [Create Web DID](https://learn.mattr.global/tutorials/dids/did-web).

2. __Configure Custom Domain__: A custom domain represents your brand and reflects trust for the end-users. To create a custom domain for your organization, please follow the tutorial on creating a [Custom Domain](https://learn.mattr.global/tutorials/essentials/custom-domain). 

3. __Presentation Request Template__: The presentation template is required to determine the credential type and the claims being requested by a verifier for the credential holder i.e. Learner. To create a presentation template, please follow the MATTR learn tutorial on creating the [Presentation Template](https://learn.mattr.global/tutorials/web-credentials/verify/presentation-template/overview).

Here is the sample presentation template which a verifier can use to verify the learner's credential information. 

```
{
   "id":"f5728a34-86f3-43d7-8a19-4egcd1589a56",
   "name":"academic-credential-presentation",
   "domain":"YOUR_TENANT_SUBDOMAIN.vii.mattr.global",
   "query":[
      {
         "type":"QueryByExample",
         "credentialQuery":[
            {
               "reason":"Please provide your certificate.",
               "example":{
                  "type":[
                     "VerifiableCredential",
                     "VerifiableCredentialExtension"
                  ],
                  "@context":[
                     "https://schema.org"
                  ],
                  "trustedIssuer":[
                     {
                        "issuer":"did:web:www.organization.com”,
                        "required":true
                     }
                  ]
               },
               "required":true
            }
         ]
      }
   ]
}
```

4. __Verifier Setup__: There are two approaches available for the Verifiers in the ARUCC ecosystem, depending on the integration pattern being used: 

- <u>**Verify with call-back**</u>: The response to each presentation request is returned to the MATTR VII platform where the credential is verified. Once verified and determined to be valid, MATTR VII will return the claims from the credential as a JSON payload to the specified call-back URL.  
To use this approach, please follow the tutorial on verifying a credential using a [callback](https://learn.mattr.global/tutorials/web-credentials/verify/callback/overview), which explains the steps and configuration required. 


- <u>**Verify via OIDC Bridge**</u>: Utilizes an OAuth2/OIDC authorization request pattern to initiate the presentation request while establishing the identity of the holder as part of the flow. 
Using the presentation template configured in “step 3” above, the Verify a Credential using OIDC Bridge tutorial explains the steps and configuration required. For more details, please follow the MATTR learn tutorial [Verify a Credential using OIDC Bridge](https://learn.mattr.global/tutorials/web-credentials/verify/oidc-bridge/overview).

5. __Invoke a Presentation Request__: 
With the above setup complete, a presentation request can be initiated as outlined in each of the above tutorials. 

- Once the QR code is scanned by the wallet the appropriate flow configured against that QR code will commence and allow the holder to present their credential for verification. 

6. __Revocation__: 
Although revocation is available with the existing MyCreds<sup>TM</sup> and MATTR capabilities, it will not be available in the first phase of the pilot.