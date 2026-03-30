---
title: "Community considerations on DNS WG structures at IETF"
abbrev: "Community considerations on DNS WGs"
category: info

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

informative:

--- abstract

There has been an increasing level of discussion within the IETF about
the best Working Group (WG) structures for handling the wide array of
DNS work being conducted within the IETF.  Wes Hardaker was asked to
gather information from the community at large through email, hallway
discussions, and meetings and create a small team to discuss potential
structural changes to be shared with the community.  This document is
the result of that effort.

--- middle

# Introduction

There has been an increasing level of discussion within the IETF about
the best Working Group (WG) structures for handling the wide array of
DNS work being conducted within the IETF.  Wes Hardaker was asked to
gather information from the community at large through email, hallway
discussions, and meetings and create a small team to discuss potential
structural changes to be shared with the community.  See
{{announcement}} for the announcement. This document is the result of
that effort.

The DNS@IETF recommendation small team (which consisted of Wes
Hardaker, Joe Abley and Lars-Johan Liman) reviewed all materials
collected between September 2025 through March 2026 about what
respondents thought about the effectiveness of the DNS related WGs
within the IETF.  Material reviewed (118 pages) included relevant
e-mail (both public and private), notes taken during discussions, and
WG/Area recordings from IETF meeting proceeding archives. After
review, the small team met multiple times in early 2026 to extract any
commonality among the expressed opinions and developed recommendations
based on them to offer the DNS community and the IESG.

This document describes the small team’s findings ({{findings}}),
their derived recommendations ({{recommendations}}) and topics where
the team did not find sufficient commonality within the collected
opinions ({{noagreement}}).

## Working Group Names Used In This Document

The team use a few new working group names below, but recognize both
these recommendations and these not-yet-existing working group names
are subject to change and thus should be considered placeholders.  It
will be up to the IESG and the community to decide what groups and
their names should actually be used.  These are terse definitions that
are further defined in the rest of the document.

- DNSPROT: A potential new working group dedicated to the development
  of the DNS protocol features itself.

- DNSDEP: A working group dedicated to developing documents related to
  the deployment of the DNS protocol.

- DNSDISPATCH: A working group dedicated to recommending where new DNS
  proposals should be directed for potential adoption.

- DNSOP: the still existing (in March 2026) DNSOP working group.  Note
  that at the time this writing the current charter of the DNSOP
  working group includes all of the tasks described above in the
  DNSPROT, DNSDEP and DNSDISPATCH group.

# Findings {#findings}

The small team found some clear points within the collected opinions.
These findings are listed here and were later distilled into
recommendations ({{recommendations}}).  Note that items listed here do
not necessarily indicate unanimous agreement, but do reflect a
significant majority among the opinions.  Note that some of the
concerns listed below are at least partially addressed later in the
recommendations section.

## Observed Commonality in Feedback Received

- A separated DNSDISPATCH mechanism would be beneficial for helping decide
  where and how new work should be conducted.
  - Working groups can then concentrate on the work they are chartered for.
  - DNSDISPATCH followers know where to track new works of interest.
  - A downside of this approach could be a potential slow down of new
    work, and an increase in agenda time in face-to-face IETF meetings.
- It would help DNS engineers within the IETF to create two groups:
  one for operations and one for protocol development.
  - One group should concentrate on operations and hopefully streamline the
    process to get these from drafts to RFCs.
  - One group should concentrate on longer term protocol development
    efforts, potentially in a higher-volume discussion.
  - An issue mentioned with splitting of work into separate groups is
    that some people would need to attend and participate in both
    groups anyway.  Though this is clear for some IETF participants,
    there were indications it doesn’t apply to everyone.  Some
    participants may also be able to concentrate more centrally on
    one, and merely watch the other.
- No structure can solve the "human problems".
  - It will still be up to the area directors and chairs to deal with
    common management issues and disagreements, for example.
  - This includes how and where work is handled in more nuanced cases.
  - WG chairs need to be supported in handling these situations.
  - WG chairs MUST coordinate within their own groups and between
    their group and other related groups.  Collaboration needs to
    occur between all DNS@IETF WGs and IESG ADs about all current DNS
    topics of concern.
- Narrowly chartered working groups are necessary for more challenging
  development problems.
  - DELEG and ADD were two examples referred to in discussions and
    comments, with DELEG being an especially agreed-upon example of a
    body of work that needed a separated, dedicated working group.
- We did not receive enough feedback indicating that the other DNS
  groups not mentioned here, like DNSSD and REGEXT, need structural
  modifications.  Thus we have no findings related to these groups and
  do not provide recommendations that affect them.

## Feedback That Did Not Achieve Common Agreement {#noagreement}

- Always requiring running code.
  - Requiring running code before adoption had a wide set of opinions
    with no commonality among them.
  - Requiring running code before document publication had generally
    more agreement, but opinions varied about whether this was
    required for all types of documents.
  - Based on this, we believe each group will need to make their own
    decision on this matter.
- Where to develop BCP documentation is an open question.
  - Some believe operational groups like DNS-OARC should drive BCP development.
  - However, there was general agreement that the publication of BCPs
    should remain in the IETF to ensure multiple protocol reference
    commonality remain within the IETF.
  - It may be that interim meetings held in conjunction with external
    conferences would be a good idea to better gather input from
    network operators managing DNS infrastructure.
- Although a few people did suggest splitting the main DNS groups into
  three or more groups, most of the feedback received indicated that
  two primary groups would be sufficient.  For example, some IETF
  participants believe there should be a DNSAPP or similar group
  focused on applications and protocols that make use of the DNS
  protocol. Furthermore, some people offered opinions that more than
  two would impose additional complications.

# Recommendations {#recommendations}

Based on the findings above, and extrapolating information from discussions to derive a suitable path forward, the DNS@IETF small team recommends that the area directors considering the following advice:

- Create a new DNSPROT (DNS Protocol) or similar group for working on protocol development and maintenance.
  - This group should have a fairly wide charter that tasks it with work on the DNS protocol itself.
  - Things requiring special processing rules likely belong in DNSPROT
  - Documentation about protocol semantics should be in DNSPROT
- Create a new DNSDEP (DNS Deployment), DNSOPS or similar group for working on protocol deployment and operational concerns.
  - This group should have a fairly wide charter that tasks it with work that doesn’t require special processing rules, needs algorithms or other simple IANA actions, or are BCPs that document existing behaviours.
  - Examples include algorithm assignments, IANA actions, BCPs, etc.
  - “How you use the protocol”
  - Alg roles, bcps, split horizon, zone cut to nowhere
- Work toward closing DNSOP in order to properly signal the change
  - Keep it open and functional until all current work is finished
  - Some work already in progress in DNSOP could move to DNSPROT or DNSDEP where work would continue, at the discretion of the authors and chairs
- Create a DNSDISPATCH working group for providing guidance to authors about where new DNS work should be conducted.
  - This will aleviate the current DNSOP WG from needing to fullfil this role in.
  - To avoid introducing delays and agenda constraints, this group should conduct its work almost entirely over a mailing list with only difficult cases requiring interim or, worst case, in-person meeting time. Ideally, in-person meetings should be rare.
  - DNSDISPATCH can recommend dispatching work to dnsprot/dnsdep/AD-sponsored/another-WG/BOF/ISE.
  - DNSDISPATCH may decline to provide a recommendation for documents that are not within scope, for example.
  - Chairs of the group need to be strict in enforcing and carrying out its objective.
  - The DNSDISPATCH group will not prioritize work within the other groups, and its dispatch decisions cannot result in automatic adoption.
  - A significant portion of submissions to DNSDISPTACH can likely be handled quickly and efficiently.
  - The DNSDISPATCH chairs should require that documents clearly articulate the problem space and proposed solution before consideration.
  - The DNS directorate is a resource available to the DNSDISPATCH working group, just as it is available to other working groups.
  - The dispatch group might use a pool of willing shepherds to assist the chairs and authors with process related help for incoming documents.
  - The dispatch group will make informed recommendations to document authors about where to take their work
    - The output of a dispatch discussion should include a short shepherd write up (perhaps a paragraph in length)
      - Light weight write ups that are sent to the mailing list for archiving.  This should not require datatracker changes.
      - DNSDISPATCH chairs should create a light template text as a boiler plate to be used by most cases.
    - DNS WGs MAY require in their charter that new work first gets a dispatch suggestion before consideration in their WG.
    - After a dispatch, document authors are encouraged to follow the recommendation and approach the WG chairs with a follow-on request (including but not limited to adoption requests).
    - Each group will continue to follow its own processes for formal adoption.
  - The chairs of the DNSDISPATCH group should work closely with the chairs of the other groups.  They may need to work together for handling more difficult topics and to collaborate on advice or questions for the DNSDISPATCH WG participants.
- Group management is expected to be significantly different in each of these groups.
  - With an effective split in functionality, it allows each group to have different forms of execution, meeting, progression, and publication requirement strategies.
  - For example, some groups may require running code, while others may not.
- Documents may occasionally (rarely we hope) need to move after being dispatched when the problem scope changes during its development and refinement.
  - For example, problems that become large may need to move to a new group.
  - Sometimes, however, the decision will be wrong but might as well stay in the current group.
  - The area director and WG chairs will need to handle this (rare) problem on a case by case basis.

## Example Dispatch Scenarios

The small team recognized that some examples might be helpful in
better understanding how the envisioned DNSDISPATCH group might
process incoming work.  As such, we came up with three example
scenarios to highlight how we envision some workflows might happen.

1. Maxwell Coulomb writes a document that describes a new way that DNS
   can be used by DHCP clients. They take this document to DNSDISPATCH
   where, after some discussion including references to other
   discussions in DHCP working groups, the chairs post a
   recommendation drawn from consensus to the list saying that in
   their opinion the best DNS working group for this document would be
   DNSDEP. Maxwell then approaches the DNSDEP chairs by sending a
   message to the chairs that includes a link to the DNSDISPATCH
   recommendation. The chairs review and decide that this is a good
   candidate document for DNSDEP to consider and send a request for
   comment to the DNSDEP mailing list.

2. Marie Ampère writes a document that describes a new protocol for
   encoding video into linked, short ASCII messages, including
   examples of how this allows video to be published in the DNS. They
   take this document to DNSDISPATCH where, after some discussion, the
   chairs post a recommendation that this is not a good fit for any
   DNS working group since it does not really represent DNS-specific
   work. Thus, the chairs decline to provide a recommendation.

3. Marmaduke Nxdomain writes a document in response to some
   operational problems that have been discussed in another forum,
   proposing some changes to DNS best practices to avoid such
   failures. After some discussion, including references to
   presentations and related observations surfaced in a recent
   DNS-OARC meeting, the chairs decide that this is a good candidate
   document for DNSDEP but that the document would benefit from some
   restructuring and rewriting first so that the substantive issues
   can be better considered in the working group. The chairs solicit a
   volunteer shepherd to help Marmaduke with the next steps. The
   shepherd helps Marmaduke update the text and later discuss the
   document with the DNSDEP chairs, including a reference to the
   DISDISPATCH recommendation.

# Security Considerations {#security}

None

# IANA Considerations

None

--- back

# Acknowledgments
{:numbered="false"}

Wes greatly thanks the small team members (Lars-Johan Liman and Joe
Abley) he corralled into helping him consume all of the review
content, and for the insights they brought to the discussion about
this problem space.

A significant number of people offered their opinions on this subject
and we greatly appreciate everyone's time, energy and desire to help
the IETF be as efficient as possible in the DNS space.

# Original project announcement {#announcement}
{:numbered="false"}

The following text is the announcement about this opinion collection
project that was sent to various DNS IETF lists on 2025-10-06 by
Mohamed Boucadair in his role as the opsarea AD.

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
