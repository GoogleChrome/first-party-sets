<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 2; ALERTS: 1.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>



## Privacy Sandbox


<table>
  <tr>
   <td>
<h1>First-Party Sets</h1>


<h1>Submission</h1>


<h1>Guidelines</h1>


   </td>
   <td><strong>Doc Owners: </strong>, 
<p>
<strong>Contributors:</strong> ,  , , , , <strong> \
Status</strong>: <strong> \
Updated: </strong>
   </td>
  </tr>
</table>



# Sign-offs


<table>
  <tr>
   <td><strong>Role</strong>
   </td>
   <td><strong>Co-Creator</strong>
   </td>
   <td><strong>Status:</strong> ✓ Approved
   </td>
  </tr>
  <tr>
   <td>Author
   </td>
   <td>, 
   </td>
   <td>DP, LGTM 10/5
   </td>
  </tr>
  <tr>
   <td>PM
   </td>
   <td>
   </td>
   <td>HC LGTM 10/5
   </td>
  </tr>
  <tr>
   <td>Eng lead
   </td>
   <td>
   </td>
   <td>KG LGTM w/ comments 10/7
   </td>
  </tr>
</table>



<table>
  <tr>
   <td><strong>Role</strong>
   </td>
   <td><strong>Primary Reviewer </strong>(confirm with <a href="http://goto.google.com/k-staffing">go/k-staffing</a>)
   </td>
   <td><strong>Back-up Reviewer</strong>
   </td>
   <td><strong>Status:</strong> ✓ Approved or FYI
   </td>
  </tr>
  <tr>
   <td>Chrome Partnerships
   </td>
   <td>darojas@ (Ads)
<p>
mastromatto@ (Ads)
<p>
jney@ (ACT)
   </td>
   <td>barbesmith@ 
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Communications/PR
   </td>
   <td>westoverscott@
   </td>
   <td>smithcolin@ 
<p>
joshcruz@
   </td>
   <td>LGTM 10/11 - SW
   </td>
  </tr>
  <tr>
   <td>GBO (always non-blocking/FYI)
   </td>
   <td>klebeau@
   </td>
   <td>rahularora@
   </td>
   <td>FYI
   </td>
  </tr>
  <tr>
   <td>Product Inclusion
   </td>
   <td>lianea@
   </td>
   <td>
   </td>
   <td>FYI
   </td>
  </tr>
  <tr>
   <td>Marketing
   </td>
   <td>cmcduffy@
   </td>
   <td>martinal@
   </td>
   <td>LGTM cmcduffy
   </td>
  </tr>
  <tr>
   <td>Dev Rel
   </td>
   <td>maudn@
<p>
dutton@
   </td>
   <td>merewood@
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Legal
   </td>
   <td>melissaknight@
<p>
mkellogg@ 
   </td>
   <td>ctanaka@
   </td>
   <td>LGTM 10/7/2022 with some comments (MRSK)
   </td>
  </tr>
</table>



# Context (_not to be published_)

In July 2022, Chrome published an updated design and policy scheme for First-Party Sets (FPS). The updated design features two main changes: (1) leveraging the Storage Access API for cookie access, and (2) using use case-based subsets, each with their own specific policy requirements, to categorize domains within a single set (_see updated [explainer](https://github.com/WICG/first-party-sets)_). 

This document provides developers (the primary audience) and interested parties with guidance on how sets are to be submitted to the canonical FPS list that Chrome will apply. This document will be published in the First-Party Sets repository on GitHub.

This version of the First-Party Sets Submission Guidelines will be published as an early preview of Chrome’s intended set creation process and policy, and is **not** a signal of the process launching officially. This preview will align with the feature flag testing availability of FPS in M108.


# Schedule/Timeline (_not to be published_)



* README file **draft** **completed**: end of **September** 2022 
* README file reviewed and **approved**: end of **October** 2022 [status: on-track]
* README file **published** on Github: **November** 2022


# Publication Contents

_Everything in the box below will be published._


<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: Long single-cell table. Check to make sure this is meant to be a code block. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



```
Note: The First-Party Sets set creation process is not yet live, but is available for <link>testing in GitHub</link>. This document is being shared as an early preview. You may submit a set to test the process, but sets will need to be resubmitted when the process launches for General Availability in Chrome.

First-Party Sets Submission Guidelines
Overview
First-Party Sets ("FPS") provides a framework for developers to declare relationships among sites, to enable limited cross-site cookie access for specific, user-facing purposes. This framework may help user agents, such as the Chrome browser ("Chrome"), to decide when to allow or deny a site access to their cookies when in a third-party context.

FPS is a Privacy Sandbox proposal being incubated in the W3C's WICG. For a full overview, consult the explainer. The First-Party Sets Submission Guidelines ("Guidelines") are put forth by Chrome to define requirements and expectations for sets submitted by developers. Chrome remains committed to pursuing standardization of FPS through engaging with developers, other browser vendors, and other interested parties.
Definitions
A First-Party Set, or set, is a collection of domains that is subject to the formation requirements, has passed the validation requirements, and has been successfully submitted to the canonical FPS list. 

A subset is a defined use case within a set. Set members, or domains, will always be part of a subset. 

A set primary is the domain a set submitter has identified as the representative of its set. Other domains within the set have a defined relationship with the primary. 

A set member is a domain that is part of a set that is not the primary. A set member will always be part of a subset within the set.

The canonical FPS list is a publicly viewable list in a JSON file format housed in the FPS GitHub repository that is the source-of-truth for all sets that are subject to the formation requirements and have passed the validation requirements. Browsers, such as Chrome, can consume this file to apply to their behavior.

A pull request (PR), is the method of requesting a change on GitHub (like adding or modifying a set to the canonical FPS list). 

A submission is an addition or modification to the canonical FPS list submitted by the submitter that is subject to the formation and the validation requirements.

A submitter is the individual or, if an individual is acting on behalf of their organization, the organization that has submitted a pull request against the canonical FPS list to create or modify a set for validation.

An equivalent domain is the primary, service, or associated domain in a set for which there is a ccTLD variant in the same set. The equivalent domain has the same effective second-level domain (eSLD, or eTLD+1 minus eTLD) as a ccTLD variant in the same set.
Set Formation Requirements
The table below describes the types of subset that FPS currently supports, including requirements to help prevent misuse of the subset. 

All submissions are subject to the formation requirements detailed in this section as well as the technical validation requirements in the next section. 

Subset Type
Subset Definition
Service
Domains that serve another set member to support functionality or security needs. 
Service domains should not be the entry point to a user's journey on a site, but may be surfaced to a user as part of their journey.
Service domains must share a common owner with the set primary.
Submitters must provide an explanation of how each domain in this subset supports functionality or security needs.
Service domains must have a registered DNS entry
Associated
Domains whose affiliation with the set primary is clearly presented to users.
Submitters must provide an explanation of how they clearly present the affiliation across domains to users and why users would expect their domains to be affiliated (e.g., an About page, header or footer, shared branding or logo, etc).

ccTLD (country code top-level domain) variants for the subsets above are also supported. The requirements for these domains are as follows:
ccTLD
Domains that represent variations for a particular country or a geographical area. 
ccTLD variants must share an identical eSLD with its equivalent domain.
The eTLD of each ccTLD variant must be present in the ccTLD section of the Public Suffix List (PSL).
ccTLD variants must share a common owner with its equivalent domain. 
Set submissions

New submissions to the canonical FPS list must be filed as pull requests (PRs) on GitHub. Submitters should ensure that submissions follow the schema template provided below. Anyone with a GitHub account may make a submission.

Modifications to existing sets, including deletions, must also be submitted as new PRs against the canonical FPS list.
The canonical FPS list will be validated against this schema whenever a user files their PR:
{
   "type": "object",
   "properties": {
       "sets":  {
           "type": "array",
           "items": {
               "type": "object",
               "properties": {
                   "ccTLDs": {
                       "type":"object",
                       "additionalProperties":{
                           "type": "array",
                           "items":{
                               "type": "string"
                           }
                       }
                   },
                   "primary" : {"type":"string"},
                   "associatedSites": {
                       "type": "array",
                       "items":{
                           "type": "string"
                       }
                   },
                   "serviceSites": {
                       "type":"array",
                       "items":{
                           "type": "string"
                       }
                   },
                   "rationaleBySite": {
                       "type":"object",
                       "additionalProperties":{
                           "type": "string"
                       }
                   }
               },
               "required": ["primary"],
               "dependentRequired": {
                   "associatedSites": ["rationaleBySite"],
                   "serviceSites": ["rationaleBySite"]
               },
           },
       }
   }
}

A hypothetical example of the FPS canonical list is provided below for reference. A submission should follow the structure below, with new submissions being added like the section highlighted in gray. 
{
 "sets": [
   {
     "primary": "https://primary.com", 

    "associatedSites": ["https://associate1.com", "https://associate2.com", "https://associate3.com"], 

     "serviceSites": ["https://servicesite1.com"], 

     "ccTLDs": {
       "https://associate1.com": ["https://associate1.ca", "https://associate1.co.uk", "https://associate1.de"],
       "https://associate2.com": ["https://associate2.ru", "https://associate2.co.kr", "https://associate2.fr"],
       "https://primary.com": ["https://primary.co.uk"]
     }
   },
  {
     "primary": "https://primary2.com", 

    "associatedSites": ["https://associateA.com", "https://associateB.com"], 

     "serviceSites": ["https://servicesiteA.com"],

     "rationaleBySite": {
       "https://associateA.com": "rationale for site",
       ""https://associateB.com": "rationale for site",
       "https://serviceSiteA.com": "rationale for site"
      },

     "ccTLDs": {
       "https://associateA.com": ["https://associateA.ca", "https://associateA.co.uk"],
       "https://associateB.com": ["https://associateB.ru", "https://associateB.co.kr"],
       "https://primary2.com": ["https://primary2.co.uk"]
     }
   }
 ]
}

Set Validation Requirements

It is important that users' interests are protected from invalid submissions, and that web browsers use objective methods to validate submissions. As such, Chrome will rely on several technical methods to validate submissions. These technical checks, comprising both set-level checks and subset-level checks, will be conducted on GitHub, where results will be accessible and viewable by the public. 
Set-level technical validation

Upon submission of a PR, a series of technical checks will run on GitHub to verify the following; 
Each domain must be prefixed by the https:// scheme. Sets may only include domains served over secure (https://) schemes. 
Each domain must be a registrable domain (i.e., eTLD+1 using a snapshot (refreshed every 6 months) of the Public Suffix List (PSL) to determine eTLD) at the time of submission. 
Each domain must not already be present in the canonical FPS list.
Each domain must satisfy the /.well-known/ metadata requirement:
The /.well-known/ metadata requirement demonstrates that the submitter has administrative access to the domains present in the set, since administrative access is required to modify the /.well-known/ file. This will help prevent unauthorized actors from adding domains to a set. 
The primary domain must serve a JSON file at /.well-known/first-party-set". The contents of the file must be identical to the submission. Each member domain must serve a JSON file at /.well-known/first-party-set". The contents of the file must name the primary domain.
Example for  primary.com/.well-known/first-party-set:
{
"primary": "https://primary.com",
 "associatedSites": ["https://associate1.com", "https://associate2.com", "https://associate3.com", "https://associate4.com"],
 "serviceSites": ["https://servicesite1.com"],
 "rationaleBySite": {
       "https://associate1.com": "rationale for site",
       "https://associate2.com": "rationale for site",
       "https://associate3.com": "rationale for site",
       "https://serviceSite1.com": "rationale for site"
      },

"ccTLDs": {
     "https://associate1.com": ["https://associate1.ca", "https://associate1.co.uk", "https://associate1.de"],
     "https://associate2.com": ["https://associate2.ru", "https://associate2.co.kr", "https://associate2.fr"],
     "https://primary.com": ["https://primary.co.uk"]
}
The /.well-known/first-party-set file for the set primary must follow the schema specified below:
{
               "type": "object",
               "properties": {
                   "ccTLDs": {
                       "type":"object",
                       "additionalProperties":{
                           "type": "array",
                           "items":{
                               "type": "string"
                           }
                       }
                   },
                   "primary" : {"type":"string"},
                   "associatedSites": {
                       "type": "array",
                       "items":{
                           "type": "string"
                       }
                   },
                   "serviceSites": {
                       "type":"array",
                       "items":{
                           "type": "string"
                       }
                   },
                   "rationaleBySite": {
                       "type":"object",
                       "additionalProperties":{
                           "type": "string"
                       }
                   }
               },
               "required": ["primary"],
               "dependentRequired": {
                   "associatedSites": ["rationaleBySite"],
                   "serviceSites": ["rationaleBySite"]
               },
           }

Example for associate1.com/.well-known/first-party-set:
{
   "primary":"https://primary.com"
}
The /.well-known/first-party-set file for set members must follow the schema specified below:
{ 
	"type": "object",
	"properties": {
           "primary" : {"type":"string"}
       },
	"required": ["primary"]
}
Subset-level technical validation

Additionally, more granular technical checks will also run on GitHub for service domains and ccTLD variants in the submissions. 
service domains must satisfy the following conditions:
Must not have robots.txt, or have a robots.txt with a "no index" header. 
Must not have ads.txt.
Must have a homepage that redirects to a different domain or results in 4xx (client error) or 5xx (server error).

ccTLD variants must satisfy the following conditions:
Must be present on ICANN's list of known ccTLDs.
Must share a common eSLD with the primary domain, 'service' domain, or 'associated' domain in the same set.

Validation success

If a set submission passes all technical checks successfully, the submitter will be notified that their PR was successful on GitHub. At this time, approved PRs will be manually merged in batches to the canonical FPS list once per week (Tuesdays at 12pm Eastern Time (ET)). 

Validation failure

A submission may fail for the following reasons:
A domain fails to pass any of the set-level technical checks.
A domain fails to pass any of the subset-level technical checks.
In the case of submission failure, the submitter will be notified through a PR failure on GitHub. The PR failure notification may also provide additional information on why the submission may have failed. All technical checks governing set submissions are conducted on GitHub, and consequently all submission failures resulting from technical checks will be viewable on GitHub. 

If you feel that a specific technical check has mistakenly caused a submission failure, leave a comment on the failed PR after consulting the error log. The Chrome team will investigate and reach out if further action is required.
Browser Behavior
When the submission process launches for General Availability in Chrome, Chrome will consume the canonical FPS list on a regular basis (e.g., every 2 weeks) and ship it to clients as an updateable component. Individual clients (with internet access) will refresh the list they apply each time they restart, or on start-up, if newly downloaded. 

In addition to the formation requirements and validation requirements above, sets are subject to subset-level limitations imposed by the browser to help prevent misuse of subsets. The table below describes how Chrome will treat each subset. 

Subset Type
Browser Behavior
Service
No limit on number of domains.
Only other domains in the same set may call requestStorageAccessFor on behalf of a service domain. 
This access will be auto-granted. 
A service domain calling requestStorageAccess for itself, or calling requestStorageAccessFor for any other domain, will be auto-rejected.
Associated
requestStorageAccess will be auto-granted for up to three domains in the order listed.
requestStorageAccess will be auto-rejected for any domain beyond the third listed. 

While there is no limit on the number of ccTLDs that may be associated with a single associated or service domain in the same set, a ccTLD variant inherits the restrictions imposed on its equivalent domain. For example, requestStorageAccess calls will be auto-rejected when called by a ccTLD variant which is an alias of a service domain.
To test this behavior in Chrome, please consult the First-Party Sets testing instructions.
Set Lifetime
Submitters should expect that sets will be subject to expiration and / or renewal requirements. This prevents sets from becoming stale, as technical checks improve, additional subsets are created, and / or alternative technologies are introduced over time. For example, sets created during the testing period will need to be refreshed at the time of third-party cookie deprecation in Chrome. At that time, submitters may expect additional clarity around set renewal requirements.
Responsibilities of the Submitter
The submitter is responsible for maintaining the integrity of their set(s) and should be able to demonstrate conformance with the formation requirements above.
For example, in the case that conformance with ownership requirements (for ccTLD variants and service domains) must be demonstrated, submitters should use resources verifiable by public documentation, or recognized in filing documentation with an incorporating or registration agency in the submitter's jurisdiction of incorporation or registration, or created or recognized by a government agency. Alternatively, in some cases, conformance with ownership requirements may be attested to by a professional opinion letter signed by a lawyer or public notary. The person signing the legal opinion should have a valid license within the jurisdiction of the country in which the main entity is operating by maintaining an office or residence.
Enforcement Activities

At this time, validation of set submissions will be based on the methods described in these Guidelines, and Chrome will not apply additional enforcement activity governing set submissions, however Chrome reserves the right to act in cases of egregious and blatant disregard of these Guidelines. All submissions are publicly visible and subject to the scrutiny of the broader web community, including users, civil society, and other interested parties.

Chrome will continue to evaluate how best to maintain the appropriate guardrails for set submissions, including developing more rigorous technical checks and introducing additional enforcement mechanisms. If Chrome determines that additional verification steps are necessary to provide a safe and reliable ecosystem for users, the team will notify developers with the appropriate notice. 
Feedback 
Chrome is committed to engaging and receiving feedback from the broader ecosystem, including through the W3C (World Wide Web) Consortium, on the future development of the First-Party Sets standard and this version of the First-Party Sets Submission Guidelines.

For feedback on the First-Party Sets standard, please engage on GitHub or on WICG calls. For feedback or questions on these Guidelines, please file an issue in this repository.
```