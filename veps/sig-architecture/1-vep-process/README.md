# Summary

Rework the existing KubeVirt design proposal process into a more
formal - still lean - Enhancement Porposal process.

# Motivation

Today it's a [very small group](https://github.com/kubevirt/community/blob/main/OWNERS#L7-L14)
which can approve design-proposals.
While certain individuals can approve design proposals, once they are merged
it is not clear who is owning them post-merge.

In this proposal we are proposing to change the process and shape them
around SIGs.
At the heart this proposal is requiring

1. designs to be sponsored by a SIG
2. to make a SIG responsible for the design process (reviews of design, code, documentation)
3. to make a SIG responsible for managing the design process (collaboration with other SIGs as needed)
4. to make a SIG owning the feature once it has been merged. The SIG is responsible for maintaing, fixing, running, everything it.

This has a few effects - see the following Goals section.

## Goals

1. The design process now has a mechanism to distribute designs among SIGs
2. SIG approvers are empowered to approve designs, increase the approvers pool
3. The ownership of an implemented feature becomes clear
4. Ensure that designs converge (accept, reject)
5. Formalize this process as an Virtualization Enhnacement Proposal (VEP) process

## Non Goals

1. Create unnecessary paperwork

# Proposal

## Definition of Users

* VEP Author - The person writing a design/enhancement proposal
* SIG - A formal KubeVirt SIG
* SIG Approver - A member of a SIG with approval permissions

## User Stories

* As a VEP Author I want to know who I can work with in order to move
  my proposal forward
* As a SIG I want to have a say in what is getting pushed into my domain
  in order to make sure that we are able to maintain it
* As a SIG Approver I want to ensure that a design is sound before a
  VEP Author is approaching an implementation.

## Repos

- https://github.com/kubevirt/enhancements

# Design

Key elements:

- Ownership: SIGs own a freature from it's inception (design) all the way to it's end
- Approvals: SIG approvers will be allowed to approve designs
- Responsibilities: SIG Approvers are responsible for driving a design, and connecitng it to other SIGs as needed

Process elements:

- VEP Author creates a GitHub Issue for getting a unique identifier and starting the process
- VEP Author creates a PR to propose the design targeting a specific SIG
- SIG decides on an approver to sheppered the VEP
- SIG collaborates with other SIGs to ensure it's throughly reviewed
- SIG approves or rejects VEP
- SIG owns future maintenance of the implementation

Technical elements:

- VEPs will live in a new dedicated repository `kubevirt/enhancements`
- `OWNER_ALIASES` will be mirrored from kubevirt/kubveirt in order to have the same sigs in the EP repository
- GitHub Issues will be used to create unique identifiers

## API Examples

None.

## Scalability

Instead of relying on a small approvers pool, now the process starts
with routing VEPs in the beginning of their life-time to SIGs.
This is expected to increase the time-to-merge-or-reject for VEPs.
And to distribute the work better.

## Update/Rollback Compatibility

We move back to the community/design-proposals process.

## Functional Testing Approach

Require this process for KubeVirt v1.3+

# Implementation Phases

Beta for KubeVirt v1.3
GA in KubeVirt v1.4