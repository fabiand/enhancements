# KubeVirt Enhnacement Proposals (EPs)

A KubeVirt Enhancement Proposal (EP) is a way to propose, communicate and coordinate on new efforts for the KubeVirt project.
You can read the full details of the project in [VEP-0000](sig-architecture/0000-vep-process/README.md).

This document is adopted from and very similar to the [Kubernetes KEP Process].

> [!NOTE]
> SIG members should read [SIGS_README.md](SIGS_README.md)

## Overview

Allmost all EPs must go through SIGs.
A SIG has to sponsor an EP, the SIG has to approve it, the SIG is responsible
for contacting related SIGs, and the SIG will become the owner of the newly
proposed feature - including but not limited to any potential code, and services
(such as CI).

## Quick start for the EP process

1. Think of a sponsoring SIG
2. Socialize an idea with a sponsoring SIG.
   You can send your idea to their mailing list, or add it to the agenda for one of their upcoming meetings.
   Make sure that others think the work is worth taking up and will help review the EP and any code changes required.
3. Follow the process outlined in the [EP template](NNNN-kep-template/README.md)

## FAQs

### Do I have to use the EP process?

More or less, yes.

Having a rich set of EPs in one place will make it easier for people to track
what is going in the community and find a structured historical record.

EPs are required for most non-trivial changes.  Specifically:
* Anything that may be controversial
* Most new features (except the very smallest)
* Major changes to existing features
* Changes that are wide ranging or impact most of the project (these changes
  are usually coordinated through SIG-Architecture)

Beyond these, it is up to each SIG to decide when they want to use the EP
process.  It should be light-weight enough that EPs are the default position.

### Why would I want to use the EP process?

Our aim with EPs is to clearly communicate new efforts to the KubeVirt contributor community.
As such, we want to build a well curated set of clear proposals in a common format with useful metadata.

Benefits to EP users (in the limit):
* Exposure on a KubeVirt blessed web site that is findable via web search engines.
* Cross indexing of EPs so that users can find connections and the current status of any EP.
* A clear process with approvers and reviewers for making decisions.
  This will lead to more structured decisions that stick as there is a discoverable record around the decisions.

### Do I put my EP in the root EP directory or a SIG subdirectory?

Almost all EPs should go into SIG subdirectories.  In very rare cases, such as
EPs about EPs, we may choose to keep them in the root.

If in doubt ask [SIG Architecture](https://git.k8s.io/community/sig-architecture/README.md) and they can advise.

### What will it take for EPs to "graduate" out of "beta"?

Things we'd like to see happen to consider EPs well on their way:
* A set of EPs that show healthy process around describing an effort and recording decisions in a reasonable amount of time.
* EPs exposed on a searchable and indexable web site.
* Presubmit checks for EPs around metadata format and markdown validity.

Even so, the process can evolve. As we find new techniques we can improve our processes.

### What is the number at the beginning of the EP name?

EPs are now prefixed with their associated tracking issue number. This gives
both the EP a unique identifier and provides an easy breadcrumb for people to
find the issue where the current state of the EP is being updated.

### My FAQ isn't answered here!

The EP process is still evolving!
If something is missing or not answered here feel free to reach out to [SIG Architecture](https://git.k8s.io/community/sig-architecture/README.md).
If you want to propose a change to the EP process you can open a PR on [EP-0000](sig-architecture/0000-kep-process/README.md) with your proposal.

[Kubenetes KEP Process]: https://github.com/KubeVirt/enhancements/blob/master/keps/README.md
