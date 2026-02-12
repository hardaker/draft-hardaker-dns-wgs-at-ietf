---
title: "Community consensus report on DNS WG structures at IETF"
abbrev: "Community consensus report on DNS WGs"
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
DNS work being conducted within the IETF.  Wes Hardaker was askedto
gather information from the community at large through email, hallway
discussions, and meetings and create a small team to discuss potential
structural changes to be shared with the community.  See
{{announcement}} for the announcement. This document is the result of
that effort.

The DNS@IETF recommendation small team (which consisted of Wes
Hardaker, Joe Abley and Lars-Johan Liman) reviewed all materials
collected in the fall of 2025 about how respondents thought about the
effectiveness of DNS related WGs.  Material reviewed (118 pages)
included relevant e-mail, notes, WG/Area recordings. After review, the
small team met multiple times in early 2026 to extract consensus and
recommendations to offer the DNS community and the IESG.

This document describes the small team’s findings, recommendations, as
well as some topics where we did not find consensus or where we
identified topics for future consideration.

Note: we use a few new working group names below, but recognize both
these recommendations and these not-yet-existing working group names
are subject to change and thus should be considered placeholders.

# Findings

The small team found some clear points of consensus points within the
collected opinions.  These findings were later distilled into
recommendations ({{recommendations}}).

- A DNSDISPATCH mechanism would be beneficial for deciding where and how new work should be formed.
  - Working groups can then concentrate on the work they are chartered for.
  - Followers know where to follow new works of interest.
  - A downside is a potential slow down of new work, and an increase in agenda time.
- Creating two groups, one for operations and one for protocol development, would be helpful.
  - One would concentrate on operations and hopefully streamline the process to get from drafts to RFCs.
  - One would concentrate on longer term protocol development efforts, potentially in a higher-volume discussion.
  - A downside discussed is that some people would need to attend and participate in both groups anyway.  Though this is clear for some IETF participants, there were indications it doesn’t apply to everyone.  Some may also be able to concentrate fully on one, and merely watch the other.
- No structure can solve the “human problems”.
  - It is still up to the area directors and chairs to deal with disagreements of all kinds.
  - This includes how and where work is handled in more nuanced cases.
  - WG chairs need to be supported in handling these situations.
  - WG chairs MUST coordinate within and between groups and discuss DNS@IETF wide current topics of concern with each other and their ADs.
- Narrow chartered working groups are necessary for more challenging development problems
  - DELEG and ADD being two examples, with DELEG being an especially agreed-upon example of an that needed a separated, dedicated working group.
- We did not receive feedback indicating that the other DNS groups not mentioned here, like DNSSD and REGEXT, need structural modifications.

# Recommendations {#recommendations}

Based on the findings above, and extrapolating information from discussions to derive a suitable path forward, the DNS@IETF small team recommends that the area directors considering the following advice:

- Create a new DNSPROT (DNS Protocol) or similar group for working on protocol development and maintenance.
  - This group should have a fairly wide charter that tasks it with work on the DNS protocol itself.
  - Things requiring special processing rules likely belong in DNSPROT
  - Documentation about protocol semantics should be in DNSPROT
- Create a new DNSDEP (DNS Deployment) or similar group for working on protocol deployment and operational concerns.  \[Really need a better new name\]
  - This group should have a fairly wide charter that tasks it with work that doesn’t require special processing rules, needs algorithms or other simple IANA actions, or are BCPs that document existing behaviours.
  - Examples include algorithm assignments, IANA actions, BCPs, etc.
  - “How you use the protocol”
  - Alg roles, bcps, split horizon, zone cut to nowhere
- Work toward closing DNSOP in order to properly signal the change
  - Keep it open and functional until all current work is finished
  - Some work already in progress in DNSOP could move to DNSPROT or DNSDEP where work would continue, at the discretion of the authors and chairs
- Create a DNSDISPATCH group for providing guidance to authors about where new DNS work should be conducted.
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

## Suggestions that achieved no or only fairly rough consensus

- Always requiring running code.
  - Running code before adoption definitely did not have consensus.
  - Running code before publication had generally rough consensus.
  - Based on this, we believe each group will need to make their own decision on this matter as suggested above.
- BCP documentation is an open question about where best to develop them.
  - Some believe operational groups like DNS-OARC should drive BCP development.
  - There is rough consensus that publication of BCPs should remain in the IETF.
  - It may be that interim meetings held in conjunction with external conferences would be a good idea.

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
