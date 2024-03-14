# Enhancement Tracking and Backlog

- [Is My Thing an Enhancement?](#is-my-thing-an-enhancement)
- [When to Create a New Enhancement Issue](#when-to-create-a-new-enhancement-issue)
- [How to Create a New Enhancement Issue](#how-to-create-a-new-enhancement-issue)
- [Why Are Enhancements Tracked](#why-are-enhancements-tracked)
- [When to Comment on an Enhancement Issue](#when-to-comment-on-an-enhancement-issue)
- [Labels](#labels)
- [Glossary](#glossary)

This repo contains Virtualization Enhnacement Proposals (VEPs). VEPs are umbrellas for new enhancements to be added to KubeVirt. An enhancement can take one or more releases to complete. An enhancement may be filed once there is consensus in at least one KubeVirt SIG.

## Is My Thing an Enhancement?

We are trying to figure out the exact shape of an enhancement. Until then, here are a few rough heuristics.

An enhancement is anything that:

- a blog post would be written about after its release
- requires multiple parties/SIGs/owners participating to complete (ex. GPU scheduling [API, Core, & Node], StatefulSets [Storage & API])
- will be graduating from one stage to another (ex. alpha to beta, beta to GA)
- needs significant effort or changes KubeVirt in a significant way (ex. something that would take 10 person-weeks to implement, introduce or redesign a system component, or introduces API changes)
- impacts the UX or operation of KubeVirt substantially such that engineers using KubeVirt will need retraining
- users will notice and come to rely on

It is unlikely an enhancement if it is:
- implememented by modifying Kubernetes code
- fixing a flaky test
- refactoring code
- performance improvements, which are only visible to users as faster API operations, or faster control loops
- adding error messages or events

If you are not sure, ask someone in the SIG where you initially circulated the idea. If they aren't sure, jump into
[#kubevirt-dev](https://kubernetes.slack.com/messages/kubevirt-dev/) on Slack or ping someone listed in [OWNERS](https://github.com/kubevirt/enhancements/blob/master/OWNERS).

## When to Create a New Enhancement Issue and Proposal

Create an issue and PR in this repository once you:
- have circulated your idea to see if there is interest
   - through Community Meetings, SIG meetings, SIG mailing lists, or an issue in github.com/kubevirt/kubevirt
- (optionally) have done a prototype in your own fork
- have identified people who agree to work on the enhancement
  - many enhancements will take several releases to progress through Alpha, Beta, and Stable stages
  - you and your team should be prepared to work on the approx. 9mo - 1 year that it takes to progress to Stable status
- are ready to be the project manager for the enhancement

## How to Create a New Enhancement Issue and Proposal

Follow this [quick start for the EP process](proposals/README.md#quick-start-for-the-ep-process).

## Why Are Enhancements Tracked

Once users adopt an enhancement, they expect to use it for an extended period of time. Therefore, we hold new enhancements to a high standard of conceptual integrity and require consistency with other parts of the system, thorough testing, and complete documentation. As the project grows, no single person can track whether all those requirements are met. 

## When to Comment on an Enhancement Proposal

Please comment on the enhancement proposal to:
- request a review or clarification on the process
- update status of the enhancement effort
- link to relevant issues in other repos
- discuss a detail of the design, code or docs

## Labels

| Label Name | Purpose | How to use this label | Who should use this label |
| ------ | ------ | ------ | ------ |
| `sig/foo` | Denotes the SIG(s) which owns this enhancement—e.g., `SIG Foo` | Set the label using the comment `/sig foo` (on a separate line) | Anyone |
| `kind/feature` | Denotes that the issue should be tracked as an enhancement (all enhancement issues should be marked with this label) | Set the label using the comment `/kind feature` (on a separate line) | Anyone |
| `stage/{alpha,beta,stable}` | Denotes the stage of an issue in the features process | Set the label using the comment `/stage alpha` (on a separate line) | Anyone |

## Glossary

Please refer to the [Glossary](docs/glossary.md) for the definition of any terminology and acronyms used in the Enhancements subproject.
