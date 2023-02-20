### ARUCC Verifier setup

Before a verifier (or industry partner), can use MyCreds<sup>TM</sup> to verify a learner's credential, they need to be set up with certain prerequisites. These prerequisites are outlined below:

Here are some of the prerequisites required to set up a verifier before credential information is verified. 

1. __Tenant Setup__: A new tenant is created with the necessary information that can be initiated with the MATTR. For more information, see the [Tenant Setup](https://learn.mattr.global/tutorials/essentials/tenant-setup). It is assumed that each verifier will utilize a DID:Web to represent themselves. This should be setup by following the MATTR learn tutorial [Create Web DID](https://learn.mattr.global/tutorials/dids/did-web).

2. __Configure Custom Domain__: A custom domain represents your brand and reflects trust for the end-users. To create a custom domain for your organization, please follow the tutorial on creating a [Custom Domain](https://learn.mattr.global/tutorials/essentials/custom-domain). 

3. __Presentation Request Template__: The presentation template is required to determine the credential type and the claims being requested by a verifier for the credential holder i.e. Learner. To create a presentation template, please follow the MATTR learn tutorial on creating the [Presentation Template](https://learn.mattr.global/tutorials/web-credentials/verify/presentation-template/overview).

Here is the sample payload structure for a presentation template which a verifier can use to verify the learner's credential information. 
```
{
   "id":"f5728a34-86f3-43d7-8a19-4egcd1589a56",
   "name":"academic-credential-presentation",
   "domain":"kakapo-nursing.mattrlabs.com",
   "query":[
      {
         "type":"QueryByExample",
         "credentialQuery":[
            {
               "reason":"Please provide your certificate.",
               "example":{
                  "type":[
                     "VerifiableCredential"
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

