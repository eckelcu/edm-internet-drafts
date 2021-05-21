---
title: "Find Code Related to an Internet-Draft or RFC"
abbrev: "find-code"
docname: draft-eckel-edm-find-code-latest
category: info

ipr: trust200902
area: General
workgroup: edm
keyword: Internet-Draft

stand_alone: yes
pi: [toc, sortrefs, symrefs]

author:
 -
    ins: C. Eckel
    name: Charles Eckel
    organization: Cisco Systems
    email: eckelcu@cisco.com

normative:

informative:

--- abstract

Code related to existing IETF standards and ongoing standardization efforts may exist and be publicly accessible in many places. This document provides a set of practices aimed at making it easier find such code.

--- middle

# Introduction

Code related to existing IETF standards and ongoing standardization efforts may exist and be publicly accessible in many places. One common place is [GitHub](https://github.com/), but there are many others. The relationship of the code to corresponding IETF standards efforts may be direct, as in the case of a client or server that supports a proposed new protocol defined by an [Internet-Draft (I-D)](https://www.ietf.org/standards/ids/). It may be indirect, as in a utility that helps analyze network traffic corresponding to this same protocol. The maturity and status of the code may range from something written quickly as a proof of concept during a hackathon, to a well established and supported implementation, to a legacy project that is no longer actively developed or maintained. The code must be publicly available, and preferably open source, though other terms of use may exist as well. In all cases, the code is potentially of interest and beneficial to people contributing to the definition, implementation, or deployment of an existing or evolving IETF standard. This document provides a set of practices aimed at making it easier to identify and find such code.

# Existing IETF Processes and Procedures

The idea that code related to IETF standards is valuable is not new. Most IETF participants are familiar with the phrase "rough consensus and running code" from the [IETF Tao](https://www.ietf.org/tao.html) and support its pragmatic approach. The existence of multiple independently developed interoperable implementations was explicitly required by {{?RFC1264}} for internet standards on routing protocols. Subsequent updates relaxed this requirement, but the value of running code is still appreciated and several current RFCs define processes and procedures related to running code.

## Implementation Status

A simple process that allows authors of I-Ds to record the status of known implementations by including an Implementation Status section is defined {{?RFC7942}}. The goal of this section is to allow reviewers and working groups to assign due consideration to documents that have the benefit of running code, which may serve as evidence of valuable experimentation and feedback that make the implemented protocols and corresponding documents more mature. However, it states that the Implementation Status section should be removed from I-Ds before they are published as RFCs. As a result, the value of the code is envisioned as being limited to that required to develop the standard and there is no mechanism to help find the code once the RFC is published.

## GitHub

The IETF chartered the GitHub Integration and Tooling [(GIT)](https://datatracker.ietf.org/wg/git/about/) working group to establish and document practices and policies for use of GitHub by working groups for managing their work. This resulted in {{?RFC8874}}, which provides a set of guidelines for working groups that choose to use GitHub for their work, and {{?RFC8875}}, which specifies a set of administrative processes and conventions for such working groups. Within the working group, the concept of work is limited to the development of I-Ds that may eventually become RFCs. Any concept of code is limited to that which appears as text within these documents. In many cases, there is additional code that is closely associated with the documents but not contained within them. This code may be of interest to the community of people contributing to the development of the documents or to the implementation or deployment of eventual standards defined by them.

## Hackathon

The IETF Hackathon {{?I-D.eckel-shmoo-ietf-hackathon}} encourages the IETF community to collaborate on running code related to existing and evolving Internet standards. Each Hackathon has a wiki that provides a breif description of each project. It is very common for there to be one of more I-Ds or RFCs associated with each project and for there to be one or more related code repositories. These resources are often listed on the wiki, but they are documented and shared with project teams in other ways as well. After the Hackathon, the wiki remains available, but the information within it is typically not updated or maintained.

# Proposals

## from Tommy and Mark
How about a link in data tracker to take you to said COTS service? (With a standard template, etc).
My .02 -- I'd very much rather track this sort of thing in COTS services (e.g., GitHub) rather than commissioning yet another expensive, one-off, badly-maintained datatracker feature.

# Datatracker Mechanisms
A few releases ago, we changed the way the datatracker allows you to
make references to external resources (see the section labelled
Additional Resources on a document's main page or on a groups /about page).

If you are using github for your working group or a set of drafts,
please consider pointing to the repository or organization using the
github_repo and github_org tags respectively. The datatracker will use
the urls you provide with those tags to backup the repositories.

(You'll see github and gitlab username tags in the hint for the edit
form - those are not used by the backup mechanism - there is no need to
enter any such thing for this purpose).

RjS


# Security Considerations

TBD.


# IANA Considerations

This document has no IANA actions.



--- back

# Acknowledgments
{:numbered="false"}

TBD.
