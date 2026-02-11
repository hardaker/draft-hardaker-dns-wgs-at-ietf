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
DNS work being conducted within the IETF.  Wes Hardaker was asked to
gather information from the community at large through email, hallway
discussions, and meetings and create a small team to discuss potential
structural changes to be shared with the community.  This document is
the result of that effort.

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

- Create a new DNSPROT or similar group for working on protocol development and maintenance.
  - This group should have a fairly wide charter that tasks it with work on the DNS protocol itself.
  - Things requiring special processing rules likely belong in DNSPROT
  - Documentation about protocol semantics should be in DNSPROT
- Create a new DNSDEP or similar group for working on protocol deployment and operational concerns.  \[Really need a better new name\]
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
