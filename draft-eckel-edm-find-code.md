---
title: "Find Code Related to an Internet-Draft or RFC"
abbrev: "find-code"
docname: draft-eckel-edm-find-code-latest
category: bcp

ipr: trust200902
area: General
workgroup: edm
keyword: Internet-Draft
stream: IETF

stand_alone: yes
pi: [toc, sortrefs, symrefs]

author:
 -
    ins: C. Eckel
    name: Charles Eckel
    organization: Cisco Systems
    country: United States of America
    email: eckelcu@cisco.com

normative:

informative:

--- abstract

Code related to existing IETF standards and ongoing standardization efforts may exist and be publicly accessible in many places. This document provides a set of practices to make it easier to identify and find such code.

--- middle

# Introduction

Code related to existing IETF standards and ongoing standardization efforts may exist and be publicly accessible in many places. One common place is [GitHub](https://github.com/), but there are many others. The relationship of the code to corresponding IETF standards efforts may be direct, as in the case of a client or server that supports protocol defined by an [Internet-Draft (I-D)](https://www.ietf.org/standards/ids/). It may be indirect, as in a utility that helps analyze network traffic corresponding to this same protocol. The maturity and status of the code may vary considerably, including something written quickly as a proof of concept during a hackathon, a well established and supported implementation, or a legacy project no longer actively developed or maintained. The code must be publicly available, and preferably open source, though other terms of use may exist as well. In all cases, the code may be of interest and beneficial to people contributing to the definition, implementation, or deployment of an existing or evolving IETF standard. This document provides a set of practices that make it easier to identify and find such code.

# Existing IETF Processes and Procedures

The idea that code related to IETF standards is valuable is not new. Most IETF participants are familiar with the phrase "rough consensus and running code" from the [IETF Tao](https://www.ietf.org/tao.html). The existence of multiple independently developed and interoperable implementations was explicitly required by {{?RFC1264}} for internet standards on routing protocols. Subsequent updates relaxed this requirement, but the value of running code is still appreciated, and several current RFCs define processes and procedures related to running code.

## Implementation Status

A simple process that allows authors of I-Ds to record the status of known implementations by including an Implementation Status section is defined in {{?RFC7942}}. The intent of this section is to allow the reader to assign due consideration to I-Ds that have the added benefit of running code, which may serve as evidence of valuable experimentation and feedback that make the protocols and corresponding documents more mature. However, it is stated that the Implementation Status section should be removed from I-Ds before they are published as RFCs. As a result, the value of the code is limited to that required to develop the standard, and the mechanism does not help find the code once the RFC is published.

## GitHub

The IETF chartered the GitHub Integration and Tooling [(GIT)](https://datatracker.ietf.org/wg/git/about/) working group to establish and document practices and policies for use of GitHub by working groups for managing their work. This resulted in {{?RFC8874}}, which provides a set of guidelines for working groups that choose to use GitHub for their work, and {{?RFC8875}}, which specifies a set of administrative processes and conventions for such working groups. Within the working group, the concept of work is limited to the development of I-Ds that may eventually become RFCs. Any concept of code is limited to that which appears as text within these documents. In many cases, there is additional code that is closely associated with the documents but not contained within them. This code may be of interest to the community of people contributing to the development of the documents or to the implementation or deployment of eventual standards defined by the documents.

## Hackathon

The IETF Hackathon {{?RFC9311}} encourages the IETF community to collaborate on running code related to existing and evolving Internet standards. Each Hackathon has a wiki that provides a brief description of each project. It is common for there to be one of more I-Ds or RFCs associated with each project, and for there to be one or more related code repositories. These resources are often listed on the wiki, but they are documented and shared with project teams in other ways as well. After the Hackathon, the wiki remains available, but the information within it is typically not updated or maintained.

# Proposal

This section specifies a set of practices that use existing mechanisms to associate code with an I-D or RFC. Following these practices makes it easier for others working with the I-D or RFC to find such code.

## GitHub Repository

A [GitHub repository](https://docs.github.com/en/github/getting-started-with-github/quickstart/create-a-repo#create-a-repository) should be setup for an I-D, as outlined in [Section 3.2 of RFC 8874](https://www.rfc-editor.org/rfc/rfc8874.html#section-3.2). The [i-d-template](https://github.com/martinthomson/i-d-template) can be used to get started. It provides useful features, including integration with the Datatracker (see [Datatracker](#datatracker)). The resulting repository should be associated with the I-D using the Datatracker `github_repo` tag. This should be done even if GitHub is not to be used to collaborate on the I-D.

A GitHub repository typically exists within a [GitHub organization](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations). This is not always the case (e.g., a repository in a personal GitHub account), and even when it is, the GitHub organization may not be appropriate to associated with the I-D. In the event there is an appropriate GitHub organization, it should be associated with the I-D using the Datatracker `github_org` tag. Examples of such GitHub organizations are:

- [IETF HTTP Working Group](https://github.com/httpwg)
- [IETF QUIC Working Group](https://github.com/quicwg)
- [Internet Architecture Board](https://github.com/intarchboard)

## README

The GitHub repository associated with the I-D should include a [README](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/about-readmes). The README should include information about the repository, whether or not it is being used to collaborate on the I-D, and any code associated with the I-D. The latter may be achieved by including direct links to such code or by including links to other resources that include information about such code. These resources may be a file, folder, or [wiki](https://docs.github.com/en/communities/) within the GitHub repository or the GitHub organization associated with the I-D. The QUIC Working Group's [Implementations wiki](https://github.com/quicwg/base-drafts/wiki/Implementations) is an example.

## Datatracker

The IETF [Datatracker](https://datatracker.ietf.org/) supports the association of `Additional Resources` with a `Document` (e.g., an I-D or RFC) or a `Group` (e.g., [working group](https://datatracker.ietf.org/wg/), [research group](https://datatracker.ietf.org/rg/)). An `Additional Resource` can be, among others things, a GitHub organization or a GitHub repository.

It is recommended that this Datatracker mechanism be used to associate an appropriate GitHub organization and repository with an I-D. Ideally the organization and repository are setup per the guidelines in {{?RFC8874}} and {{?RFC8875}}. In the event the working group or research group is not using GitHub, or the I-D has not yet been adopted by the group, another GitHub organization or repository may be used instead. A GitHub organization is associated with the I-D using the `github_org` tag. A GitHub repository is associated with the I-D using the `github_repo` tag.

## Implementation Status

An Implementation Status section, as defined {{?RFC7942}}, should be added to an I-D. It should state any GitHub organization or GitHub repository associated with the I-D.

## Inline Errata

In the event an I-D becomes an RFC, people looking for code are less likely to reference the Datatracker, and the Implementation Status section may have been removed or outdated. Any GitHub organization or GitHub repository associated with the RFC should be made available as [inline errata](https://mailarchive.ietf.org/arch/msg/edm/ku3cd5xTla7tbtohVYWWW7-XTIg/). An example of this is [RFC 3261 with inline errata](https://www.rfc-editor.org/rfc/inline-errata/rfc3261.html).

## Known Limitations

Known limitations of this proposal, and ongoing efforts to address them, include the following:

- The ability within the Datatracker to associate `Additional Resources` with an I-D or RFC is not well known or used.
  - The [IETF Tools Team](https://www.ietf.org/about/groups/tools/) has made the ability to view and edit `Additional Resources` more prominent in the Datatracker.
  - The functionality is promoted in IETF Hackathons.
- The ability and procedure to submit errata is not well known or used, and errata that is submitted is not always processed in a timely fashion.
  - An experiment with [collaborative annotations](https://rfc-annotations.research.icann.org/) for RFCs related to DNS has been sponsored by ICANN.

# Implementation Status

The practices proposed in this document are followed by {{?RFC9311}}.

# Security Considerations

TBD.


# IANA Considerations

This document has no IANA actions.



--- back

# Acknowledgments
{:numbered="false"}

Vijay Gurbani [started](https://mailarchive.ietf.org/arch/msg/edm/1AV0yGy5cetLjmP6aOu0xyD2kHE/) the discussion that inspired this effort.

Robert Sparks highlighted a [datatracker mechanism](https://mailarchive.ietf.org/arch/msg/wgchairs/DA-fWpq_nsy_5kPhJEheBlyaaqI/) to add a reference to a GitHub repository or organization using the `github_repo` or `github_org` tag, respectively.

Martin Thompson created the [i-d-template](https://github.com/martinthomson/i-d-template) repository can be used to setup a GitHub repository for an I-D.

Spencer Dawkins pointed out the RFC editor's ability to [inline errata](https://mailarchive.ietf.org/arch/msg/edm/ku3cd5xTla7tbtohVYWWW7-XTIg/) and noted that something similar could be done to point to code.

Adam Roach played in important role in enabling the RFC editor's ability to [inline errata](https://mailarchive.ietf.org/arch/msg/edm/ku3cd5xTla7tbtohVYWWW7-XTIg/).

Mark Nottingham provided illustrative example of how the [QUIC](https://github.com/quicwg/base-drafts/wiki/Implementations) working group uses wiki pages to track early implementations.

Yaron Sheffer highlighted limitations with the current errata process and the existance of the ICANN project for [collaborative annotations](https://rfc-annotations.research.icann.org/) of RFCs related to DNS.

Many other people shared thoughts on the email lists for [WG Chairs](https://mailarchive.ietf.org/arch/browse/wgchairs/) and [EDM](https://mailarchive.ietf.org/arch/browse/edm/) about how to make it easier to find code. These helped shape the practices outlined in this document.
