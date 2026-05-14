---
title: "Community considerations on DNS WG structures at IETF"
abbrev: "Community considerations on DNS WGs"
category: historic

docname: draft-hardaker-dns-wgs-at-ietf-latest
submissiontype: IETF
consensus: true
v: 3
area: "Operations and Management"
workgroup: "Domain Name System"
keyword:
 - DNS
venue:
  group: "Domain Name System"
  type: "Working Group"
  mail: "ietf@ietf.org"

author:
  -
    fullname: Wes Hardaker
    organization: Google, Inc.
    email: ietf@hardakers.net
  -
    fullname: Lars-Johan Liman
    organization: Netnod
    email: liman@netnod.se
  -
    fullname: Joe Abley
    organization: Cloudflare
    email: jabley@cloudflare.com

normative:
  BCP14:

informative:
  DNS-at-IETF:
    title: dns-at-ietf mailing list
    target: https://mailarchive.ietf.org/arch/browse/dns-at-ietf/

--- abstract

There has been an increasing level of discussion within the IETF about
the best Working Group (WG) structures for handling the wide array of
DNS work being conducted within the IETF.  Wes Hardaker was asked to
gather information from the community at large through e-mail, hallway
discussions, and meetings and create a small team to discuss potential
structural changes to be shared with the community. This document
describes the team’s aggregated findings, their derived
recommendations, and topics where the team did not find sufficient
commonality within the collected opinions.

This document is published to retain the record for historic reference.

--- middle

# Introduction

There has been an increasing level of discussion within the IETF about
the best Working Group (WG) structures for handling the wide array of
DNS work being conducted within the IETF.  Wes Hardaker was asked to
gather information from the community at large through e-mail, hallway
discussions, and meetings and create a small team to discuss potential
structural changes to be shared with the community.  See
{{announcement}} for the announcement. This document is the result of
that effort.  The main venue for this effort was [DNS-at-IETF].

The DNS@IETF recommendation team consisted of Wes Hardaker, Joe
Abley and Lars-Johan Liman.  Together they reviewed all the feedback
about what respondents thought about the effectiveness of
the DNS related WGs within the IETF between September 2025 through
March 2026.  Material reviewed (118 pages) included relevant e-mail
(both public and private), notes taken during discussions, and WG/Area
recordings from IETF meeting proceeding archives. After review, the
team met multiple times in early 2026 to extract any commonality
among the expressed opinions and developed recommendations based on
them to offer the DNS community and the IESG.  The main
recommendations were then reviewed and reported in IETF#125 (March
2026).

This document describes the team’s findings ({{findings}}),
their derived recommendations ({{recommendations}}) and topics where
the team did not find sufficient commonality within the collected
opinions ({{noagreement}}).

This document is published for historical reference and also to
provide a stable reference for future assessment of the DNS work in
the future.

## Working Group Names Used In This Document

The team uses a few new WG names below, but recognize that both these
recommendations and these not-yet-existing WG names are subject to
change and thus should be considered placeholders.  It is up to the
IESG and the community to decide what WGs and their names should be
used.  Such decisions are beyond the scope of this document. These are
terse definitions that are further defined in the rest of the
document.

- DNSPROT: A potential new WG dedicated to the development
  of the DNS protocol features themselves.

- DNSDEP: A WG dedicated to developing documents related to the
  deployment, and operation in general, of the DNS protocol.  Note
  that in discussions, some believe this should be called DNSOP still
  or potentially DNSOPS.

- DNSDISPATCH: A WG dedicated to recommending where new DNS
  proposals should be directed for potential adoption and development.

- DNSOP: the still existing (in March 2026) DNSOP WG.  Note
  that at the time this writing the current charter of the DNSOP
  WG includes all of the tasks described above in the
  DNSPROT, DNSDEP and DNSDISPATCH WGs.

## Requirements language

Although the document does not specify a protocol, the {{BCP14}} is used
to stress importance of some recommendations and for better clarity.

# Findings {#findings}

The team found some clear points within the collected opinions.
These findings are listed here and were later distilled into
recommendations ({{recommendations}}).  Note that items listed here do
not necessarily indicate unanimous agreement, but do reflect a
significant majority among the opinions.  Note also that some of the
concerns listed below are at least partially addressed later in the
recommendations section.

## Observed Commonality in Feedback Received

- It would help DNS engineers within the IETF to create two WGs:
  one for operations and one for protocol development.
  - One WG should concentrate on operations and hopefully
    streamline the process to get these from I-Ds to RFCs.  Also, this
    can be a forum for reporting operational issues and elaborating
    recommendations and guidance.
  - One WG should concentrate on longer term protocol development
    efforts, potentially in a higher-volume discussion.
  - An issue mentioned with splitting of work into separate WGs is
    that some people would need to attend and participate in both
    WGs anyway.  Though this is clear for some IETF participants,
    there were indications it doesn’t apply to everyone.  Some
    participants may also be able to concentrate more centrally on
    one, and merely watch/monitor the other.
- A separated DNSDISPATCH mechanism would be beneficial for helping decide
  where and how new work should be conducted.
  - Main protocol and operations WGs can then concentrate on the work
    they are chartered for.
  - DNSDISPATCH followers know where to track new works of interest.
  - A downside of this approach could be a potential slow down of new
    work, and an increase in agenda time in face-to-face IETF meetings.
- No structure can solve the "human problems".
  - It will still be up to the Area Directors (ADs) and chairs to deal with
    common management issues and disagreements, for example.
  - This includes how and where work is handled in more nuanced cases.
  - WG chairs need to be supported in handling these situations.
  - WG chairs will need to coordinate both within their own WGs and between
    their WG and other related WGs.  Collaboration needs to
    occur between all DNS@IETF WGs and IESG Area Directors (ADs) about
    all current DNS topics of concern.
- Narrowly chartered WGs are necessary for more challenging
  development problems.
  - DELEG and ADD were two WG examples referred to in discussions and
    comments, with DELEG being an especially agreed-upon example of a
    body of work that needed a separated, dedicated WG.
- The team did not receive enough feedback indicating that the other DNS
  WGs not mentioned here, like DNSSD and REGEXT, need structural
  modifications.  Thus we have no findings related to these WGs and
  do not provide recommendations that affect them.

## Feedback That Did Not Achieve Common Agreement {#noagreement}

- Always requiring running code.
  - Requiring running code before adoption had a wide set of opinions
    with no commonality among them.
  - Requiring running code before document publication had generally
    more agreement, but opinions varied about whether this was
    required for all types of documents.
  - Based on this, we believe each WG will need to make their own
    decision on this matter.
- Where to develop BCP documentation is an open question.
  - Some believe operational WGs like DNS-OARC should drive BCP development.
  - However, there was general agreement that the publication of BCPs
    should remain in the IETF to ensure multiple protocol reference
    commonality remain within the IETF.
  - It may be that interim meetings held in conjunction with external
    conferences would be a good idea to better gather input from
    network operators managing DNS infrastructure.
- Although a few people did suggest splitting the main DNS WGs into
  three or more WGs, most of the feedback received indicated that
  two primary WGs would be sufficient.  For example, some IETF
  participants believe there should be a DNSAPP or similar WG
  focused on applications and protocols that make use of the DNS
  protocol. Furthermore, some people offered opinions that more than
  two would impose additional complications.
- There was general disagreement about whether or not to close the
  existing DNSOP WG if new ones were formed, or whether it should be
  rechartered in the process.
  - Some believed that a clean break would be beneficial to signal the
    change in structure.
  - Others believed that DNSOP was already the right name and there
    was no need to change it, aside from narrowing its charter.

# Recommendations {#recommendations}

Based on the findings above ({{findings}}), the DNS@IETF team
extrapolated information from discussions to derive a set of suitable
recommendations that the IESG ADs should consider:

- Create a new DNSPROT (DNS Protocol) or similar WG for working on
  protocol development and maintenance.
  - This WG should have a fairly wide charter that tasks it with
    work on the DNS protocol itself.
  - One potential recommendation for deciding whether things belong in
    this WG is whether or not the work was likely to develop
    special processing rules.
  - Documentation about protocol semantics should progress in DNSPROT.
- Create a new DNSDEP (DNS Deployment) WG for working on protocol
  deployment and operational concerns.
  - This WG should have a fairly wide charter that tasks it with
    work that doesn’t require special processing rules, needs
    algorithms or other simple IANA actions, or are BCPs that document
    existing behaviors.
  - Work should include guidance documents about "How you use the
    protocol".  Examples such as algorithm rollover guidance, BCPs, or
    split horizon considerations.
- Create a DNSDISPATCH WG for providing guidance to authors and work proponents
  about where new DNS work should be conducted.
  - This will alleviate the current DNSOP WG from needing to fulfill this role.
  - To avoid introducing delays and agenda constraints (as discussed
    in {{findings}}), this WG should conduct its work almost
    entirely over a mailing list.  Only the more complex or difficult
    cases should require interim or, worst case, in-person meeting
    time. Ideally, in-person meetings should be rare.
  - A significant portion of submissions to DNSDISPTACH can likely be
    handled quickly and efficiently.
  - DNSDISPATCH can recommend dispatching work to any areas of the
    IETF, including but not limited to DNSPROT, DNSDEP, AD-sponsored,
    another-WG, a BOF, or the ISE.
  - The DNSDISPATCH chairs should require that documents clearly
    articulate the problem space and proposed solution before
    consideration.
  - DNSDISPATCH may decline to provide a recommendation for documents.
    This would include documents not within scope of the IETF or that were
    not sufficiently mature to understand the problem or solution
    space, for example.
  - Chairs of the DNSDISPATCH WG need to be strict in managing,
    enforcing and carrying out its objective.
  - The DNSDISPATCH WG will not prioritize work within the other
    WGs, and its dispatch decisions cannot result in automatic
    adoption.  Each WG will continue to follow its own processes
    for formal adoption.
  - The DNS directorate (dnsdir) will be considered as a resource
    available to the DNSDISPATCH WG, just as it is available to other
    WGs.
  - The DNSDISPATCH WG might use a pool of willing shepherds to
    assist the chairs and authors with process related help for
    incoming documents.
  - The DNSDISPATCH WG will make informed recommendations to authors
     (and work proponents, in general) and document where they should
     take their work.
      - The output of a dispatch discussion should include a short
        shepherd write up (perhaps a paragraph in length)
      - These should be light weight write ups that are sent to the
        mailing list for archiving.  This should not require
        datatracker changes.
      - DNSDISPATCH chairs should create a light template as a boiler
        plate to be used by most cases.
  - DNS WGs may require, in their charter, that new work proposals
    first get a dispatch suggestion before being considered in their
    WG.
  - After a dispatch recommendation, new work proponents are encouraged
    to follow the recommendation and approach the relevant WG chairs,
    AD, ISE, etc with a follow-on request (including but not limited
    to adoption requests).
  - The chairs of the DNSDISPATCH WG should work closely with the
    chairs of the other WGs.  They may need to work together for
    handling more difficult topics and to collaborate on advice or
    questions for the DNSDISPATCH WG participants.
- WG management may be significantly different in each of these
  WGs.
  - With an effective split in functionality, each WG may choose to
    have different forms of execution, meeting, progression, and
    publication requirement strategies.
  - For example, some WGs may require running code, while others
    may not.
- Documents may occasionally (hopefully rarely) need to move after
  being dispatched when the problem or solution scope changes during
  its development and refinement.
  - For example, problems that become large may need to move to an
    entirely new WG.
  - Sometimes, however, the dispatch and adoption location decision
    might have been wrong, but might as well stay in the current
    WG.
  - The AD(s) and WG chairs will need to handle this (rare)
    problem on a case-by-case basis.

## Example Dispatch Scenarios

The DNS@IETF team recognized that some examples might be helpful
in better understanding how the envisioned DNSDISPATCH WG might
process incoming work.  As such, we offer the following three example
scenarios that highlight how dispatch workflows might happen.

1. Maxwell Coulomb writes a document that describes a new way that DNS
   can be used by DHCP clients. They take this document to DNSDISPATCH
   where, after some discussion (including references to other
   discussions in DHCP WGs), the chairs post a
   recommendation drawn from consensus to the list saying that in
   their opinion the best DNS WG for this document would be
   DNSDEP. Maxwell then approaches the DNSDEP chairs by sending a
   message to the chairs that includes a mailing list archive link to
   the DNSDISPATCH recommendation. The chairs review and decide that
   this is a good candidate document for DNSDEP and send a request for
   comment to the DNSDEP mailing list.

2. Marie Ampère writes a document that describes a new protocol for
   encoding video into linked, short ASCII messages, including
   examples of how this allows video to be published in the DNS. They
   take this document to DNSDISPATCH where, after some discussion, the
   chairs post a recommendation that this is not a good fit for any
   DNS WG since it does not really represent DNS-specific
   work. Thus, the chairs draw a consensus that a dispatch
   recommendation will not be provided.

3. Marmaduke Nxdomain writes a document in response to some
   operational problems that have been discussed in another forum,
   proposing some changes to DNS best practices to avoid such
   failures. After some discussion, including references to
   presentations and related observations surfaced in a recent
   DNS-OARC meeting, the chairs decide that this is a good candidate
   document for DNSDEP but that the document would benefit from some
   restructuring and rewriting first so that the substantive issues
   can be better considered in the WG. The chairs solicit a
   volunteer shepherd to help Marmaduke with the next steps. The
   shepherd helps Marmaduke update the text and later discuss the
   document with the DNSDEP chairs, including a reference to the
   DISDISPATCH recommendation.

# Operational Considerations

The new structure hopes to streamline the processing and handling of
DNS documents and, thus, will hopefully foster improved development of
operational guidance and provide mitigations to operational issues.

# Security Considerations {#security}

None

# IANA Considerations

None

--- back

# Acknowledgments

Wes greatly thanks the team members (Lars-Johan Liman and Joe
Abley) he corralled into helping him consume all of the review
content, and for the insights they brought to the discussion about
this problem space.

A significant number of people (too large to list here) offered their
opinions on this subject and we greatly appreciate everyone's time,
energy and desire to help the IETF be as efficient as possible in the
DNS space.

# Original project announcement {#announcement}

The following text is the announcement about this opinion collection
project that was sent to various DNS IETF lists on 2025-10-06 by
Mohamed Boucadair in his role as the OPS AD.

``` text

From: mohamed.boucadair@orange.com
Subject: Kick-off DNS work structure consultation
Date: Mon, 06 October 2025 07:49 UTC

Hi DNSOP, all,
(+ all concerned WGs: opsawg, intarea, deleg, dnssd, add, dconn, regext)

Background

As you know, DNS-related activities in the IETF are wide, affecting many other protocols within the IETF's standardization efforts. Because of this, the DNS and its adjacent work is carried out in a wide number of WGs and even areas (INT, OPS, ART).

Currently, DNSOP is acting as the central hub for much of the core DNS work and has been for the past decade or more (and prior to that in DNSEXT as well). But, the full history of the slowly evolving structure of the DNS related WGs is beyond the scope of this message (although certainly the lessons learned from the changing structure over time remain important to consider).

Recently there has been a flurry of hallway discussions about whether the current DNS-related WGs structures are working as efficiently as possible, and whether it is time to make some changes about where recommended DNS related work gets dispatched to and subsequently developed in. It may be that change is needed. It may be that no change is needed. However, it has become clear that a discussion needs to happen, and the results of that community discussion should drive any change to be implemented. See also the provisions about this discussion in the recent DNSOP Charter [1].

As indicated in my message [2], and now that the first intermediate DNSOP chartering step is done, we want to hear from everyone about what is working, and what is not, with the current structure of DNS WGs. What are the requirements for creating the most optimal work environment? Specifically, should the current DNSOP structure be maintained, modified, etc.?

Mission

The main goals of this effort are as follows:

* Provide an overview of current IETF DNS landscape & interactions
* List issues/features with the current work structure
* Propose options to soften/mitigate the issues
* Sketch a transition plan
* Propose Charter(s) (New and/or Updates to existing ones)

Task leader, team, and Call for Feedback

In order to avoid impacting ongoing DNSOP work and given the load the DNSOP Chairs already experience, I decided that this discussion is better moderated by other community members than the DNSOP WG Chairs.

I'm delighted to announce that Wes Hardaker has agreed to collect information from the community to help me, other ADs/IESG decide what the best path forward is.

Wes and a small team will gather the thoughts and opinions of those working on the DNS within the IETF and distill them down to a set of recommendations for the IESG about whether the community believes that structural changes are needed or not and, if so, to what existing or new charters.

To accomplish this, we need help from the community. Specifically, we want feedback from everyone with an opinion on the subject (including from those who think "everything is fine as is").

Below is provided a list of sample questions that are worth considering (thanks Wes for the inputs), but opinions of any sort on the subject are welcome.  Note that though Wes has his own opinions, he intends to only collect information from the community and will only respond with an acknowledgment and maybe follow on questions, if needed. Wes is willing to meet with anyone wanting to discuss this during IETF#124 in person or over a virtual meeting before hand.

After thoughts, opinions, and suggestions are collected from the community, Wes will be convening a small discussion team of interested parties to help review the collected material. If you're interested in helping on the review and recommendation team, please let Wes know. Responsible ADs, with Wes help, will decide on the small team membership later this year.

A timeline is included below detailing the course of events over the next 6 months.

Mailing List to collect feedback & discuss

A new mailing is created to collect public opinions and discussion: dns-at-ietf@ietf.org<mailto:dns-at-ietf@ietf.org>.

If you have opinions you don't want to share publicly, please send them to dns-structure-anon@hardakers.net<mailto:dns-structure-anon@hardakers.net> or to me and Wes or only to me and I will anonymize them before bringing them to the discussion team.

Information to be gathered

- How do we deal with the quantity of work that approaches DNSOP or similar?
- Is one overarching group like DNSOP good, or do we need an
  ops/protocol split like DNSOP and DNSEXT were in the past
    - and how do we ensure WGs/Chairs communicate and collaborate efficiently?
- What is the right combination of operational vs protocol maintenance group(s)?
- How to make sure that new work takes into account operational and deployment considerations?
- How do we dispatch new work coming into the IETF related to the DNS protocol?
    * DNSOP did this for the past few years.
    * Should small, contained proposals generally be dispatched to OPSAWG or similar?
    * Do we need a DNSDISPATCH group or leverage DISPATCH WG?
    * What is the right balance between a bunch of small groups vs one or a couple larger ones?
    * How to address different problem spaces and attract interested people?
    * What is the overhead on the participants that need to attend all these meetings?
    * How do we ensure there is enough expertise available?
- How do we ensure that there is sufficient support for things that are adopted (before they're adopted)?
- Do we have an over-arching policy for requiring running code/deployment(-promises) first, or is it per-WG?
- Is the current split between mDNS/EPP/RDAP/RPP, and full DNS working well?
- What should change?
- What shouldn't change?

Timeline

| Event                                          | Expected Ends|
|------------------------------------------------+--------------|
| OPSAREA Session discussion                     | IETF#124     |
| Collect feedback, suggestions, etc.            | Nov 31       |
| Analysis team craft recommendation(s)          | Jan 2026     |
| Team recommendations given to the community    | Feb 2026     |
| Analysis team meets with IESG members          | Feb 2026     |
| IESG announces plans                           | IETF#125     |


Thank you

Cheers,
Med

[1]: https://datatracker.ietf.org/doc/charter-ietf-dnsop/

[2]: https://mailarchive.ietf.org/arch/msg/dnsop/9aztqcxfpgCEkhQT3LGxkWuMui8/
```
