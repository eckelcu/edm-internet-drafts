---
title: "Finding Code Related to an Internet-Draft or RFC"
abbrev: "finding-code"
docname: draft-eckel-edm-finding-code-latest
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

Code related to existing IETF standards and ongoing standardization efforts may exist and be publicly accessible in many places. One common place is [GitHub](https://github.com/), but there are many others. The relationship of the code to corresponding IETF standards efforts may be direct, as in the case of a client or a server that supports a proposed new protocol defined by an [Internet-Draft (I-D)](https://www.ietf.org/standards/ids/). It may be indirect, as in a utility that helps analyze network traffic corresponding to this same protocol. The maturity and status of the code may range from something written quickly as a proof of concept during a hackathon, to a well established and supported implementation, to a legacy project that is no longer actively developed or maintained. The code must be publicly available, and preferably open source, but other terms of use may exist as well. In all cases, the code is potentially of interest and beneficial to people contributing to the definition, implementation, or deployment of existing and evolving IETF standards. This document provides a set of practices aimed at making it easier to find such code.

# Existing IETF Processes and Procedures

The idea that code related to IETF standards is valuable is not new. Most IETF participants are familiar with the phrase "rough consensus and running code" from the [IETF Tao](https://www.ietf.org/tao.html) and support its pragmatic approach. The existence of multiple independently developed interoperable implementations was at one time explicitly required for internet standards on routing protocols by {{?RFC1264=RFC1264}}. Subsequent updates have relaxed this requirement, but the value of running code is still appreciated and several current RFCs define processes and procedures related to running code.

## Implementation Status


Vijay wrote, “The proposal we are considering --- i.e., putting some text in RFCs to guide legions of implementers not familiar with "IETF arcana" --- is already being used loosely as I pointed out above for QUIC.  It seems to me that we can do better by institutionalising it in some manner that {{?IMPLEMENTATION-STATUS=RFC7942}} did not. Perhaps as you suggest, the answer is to simply write a RFC 7942-bis draft.  If you think this is an avenue we should explore, I am happy to spin up a rfc7942-bis  so to provide more structure to the conversation.”
Mirja wrote, “Just very quickly some points. Having read all RFCs that we have published in the four years of my AD time I can tell you that {{?IMPLEMENTATION-STATUS}} is used form time to time. However, it also addresses a different problem then what you ask for, namely how do people in the wg know about existing implementations. QUIC decides to use another tool for this purpose; I guess for several reason, one being that many implementors in QUIC who have been new to the IETF are actually more familiar with GitHub than any IETF procedures. My expectation is that note you mentioned for QUIC will be removed before publication as RFC."

## GitHub

The IETF chartered the GitHub Integration and Tooling (GIT) working group to establish and document practices and policies for use of GitHub by working groups for managing their work. This resulted in {{?GITHUB-GUIDANCE=RFC8874}}, which provides a set of guidelines for working groups that choose to use GitHub for their work, and {{?GITHUB-ADMIN=RFC8875}}, which specifies a set of administrative processes and conventions for such working groups. Within the working group, the concept of work is limited to the development of Internet-Drafts that may eventually become RFCs. Any concept of code is limited to that which appears as text within these documents. In many cases, there is additional code that is closely associated with the documents but not contained within them. This code may be of interest to the community of people contributing to the development of the documents or to the implementation or deployment of eventual standards defined by them. This document provides a set of practices aimed at making it easier to find such code.

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
