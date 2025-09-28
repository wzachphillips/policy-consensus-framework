

# Key Concepts

This document will attempt to serve as both a glossary of key terms as well as an explanation of core concepts of the framework. For complete project background and founding principles, see [charter.md](../charter.md).

## Table of Contents
- [Framework Implementation Modalities](#framework-implementation-modalities)
- [Framework Phases](#framework-phases)
  - [Issue Phase](#issue-phase)
  - [Policy Refinement Phase](#policy-refinement-phase)
- [Primary Framework Objects](#primary-framework-objects)
- [Object Details](#object-details)
  - [Problem Statements](#problem-statements)
  - [Assertions](#assertions)
  - [Premises](#premises)
  - [Policy Proposal Items](#policy-proposal-items)
  - [Policy Proposal](#policy-proposal)
- [Key Processes](#key-processes)
  - [Decomposition](#decomposition)
  - [Consensus Aggregation](#consensus-aggregation)

## Framework Implementation Modalities

This framework is designed to work across vastly different scales while maintaining core principles. There are two primary implementation modalities:

**Small Group Mode (4-49 participants)**
- Direct facilitated discussion and consensus building
- Qualitative validation and evidence review
- Face-to-face or small group dynamics
- Emphasis on collaborative dialogue and mutual understanding

**Platform Mode (50+ participants)**
- Systems-mediated processes with quantitative consensus aggregation
- Algorithmic sorting and statistical validation
- Democratic voting mechanisms and structured participation
- Emphasis on scalable processes and diverse perspective integration

**Core Hypothesis**: Larger participant populations enable greater perspective diversity, leading to more robust and widely-supported policy proposals.

For detailed discussion of implementation approaches, scaling considerations, and practical guidance, see [implementation.md](implementation.md). Current research priorities and contribution opportunities are outlined in [roadmap.md](../roadmap.md).

## Framework Phases

### Issue Phase
The issue phase represents the review and discussion of current policy. This step focuses on correctly aligning the information about existing policies around a certain topic / region and seeks to break the discussion down into the simplest parts. This is to facilitate clearer discussion and reduce the overall complexity in each argument.

#### Value Proposition

The hypothesis of this phase is that breaking the issues down to their most simple elements accomplishes a few things:
- Removes extraneous topics from the discussion that are not constructive additions.
- Makes provided supporting evidence more objective and easy to evaluate.
- Helps dampen the impact of partisanship when discussing the issue.

#### Validation Metrics

- User Sentiment analysis on how they felt when participating in the process.
  - Did they feel the process helped the discussion be more effective?
  - Did they feel the process helped them communication with people with other perspectives?
  - Did the process expose them to valid new perspectives on a given issue?
  - Did the process change their mind, even if only partially on a given topic?

### Policy Refinement Phase

The policy refinement phase is the point where users of the platform can leverage the information gathered in the Issue Phase and create recommendations for modified policy proposals. This process is also democratic and is used to discuss and refine key topics

#### Value Proposition

This phase is an attempt to solve the lack of citizen unification around modified policy proposals. The thought is that this phase accomplishes a few key things:
- Creates a structured way to discuss the key components of policy.
- Breaking down to the smallest unit of policy change better allows users with different perspectives to identify areas they agree on.
- Highlights which areas are universally supported and which items are most contentious (This provides context on areas where continued work is needed, and feeds back into the `Issue Phase`).
- Helps provide a more constructive outlet to political discussion that produces actual policy guidance that is widely supported.
- Helps guide near-term policy priorities by focusing on the topics that there exists agreement on and promotes smaller, more actionable policies adjustments.

#### Validation Metrics

- User Sentiment analysis on how they felt about the value of the process
  - Did they feel the process helped the discussion be more effective?
  - Did they feel that seeing where alignment existed between differing perspectives help them change their opinion about the policy positions of those different than them?
  - Did they feel the process resulted in policy recommendations that were more in line with their concerns as citizens than what they are used to from existing political processes
- Number of Policy Proposals that have a consensus score > 75%


## Primary Framework Objects

- **Users:** This framework is built on the premise of having 4 or more participating users (minimum viable group) and can scale to millions of participants. Since the system is democratic in nature, the effectiveness of the overall system can be enhanced by the volume and diversity of the user population. Implementation approaches adapt to group size - see [Framework Implementation Modalities](#framework-implementation-modalities). For participation guidelines and requirements, see [contributor.md](../contributor.md).

- **Topics:** A policy topic is the highest level object in the tree that helps provide aggregation and framing for a broad discussion.

- **Topic Abstract:** A topical overview providing a background summarization the policy topic. The goal of this document is to frame the discussion in a neutral manner and to describe the current framing of any major cultural perspectives. 

- **Current Policy Summary:** This document is intended to be an effective summary of the current policies that pertain to this topic within a given region. Implementations will likely provide some regional breakdown by country and territory.

- **Current Policy:** A specific piece of legislation that codifies a law or other rule. This object contains metadata and reference information containing the full text of the policy.

- **Region:** The specific region that a Current Policy or Policy Proposal is relative to

- **Problem Statement:** A stance statement relative to one or more defined policies. All problem statements must be explicitly related to at least one policy and must be flagged for review if an upstream policy is updated.

- **Assertion:** A decomposition of the problem statement. If problem statements are statements of opinion, then an assertion is a supporting concept that represents the key component of the problem statement.

- **Premise:** A Premise is generic object that facilitates key collaborative efforts. A premise is basis of an assertion that can be questioned and tested for validity.

- **Supporting Artifact:** A supporting artifact is a document, website, policy, or other piece of metadata that can be linked to a premise object to either suggest support for or against another object.

- **Policy Proposal Item:** An idea for a singular policy change that represents a change from an existing policy. 

- **Policy Proposal:** A user provided policy proposal that aggregates a collection of Policy Proposal Items

- **Consensus Votes:** A collected vote provided by `Users` that expresses support for or against a given other object. Primary objects that can receive votes are Artifacts and Policy Proposal Items and final Policy Proposals.

- **Aggregate Validation Scores:** An aggregation of consensus votes to a higher level object. Used to clarify how current voting either supports or rejects the associated object. Score is slightly contextual given the associated object.


## Object Details

### Problem Statements

- Problem statements are expressions of opinion provided by a user. This object is expected to be less constrained and more of a starting point for the decomposition process.
- Users should be able to indicate support for a problem statement but not negative support. The reason for this is to simply help highlight supporting problem statements, not to argue the finer points. This will happen at the next level

### Assertions

- Through a process called decomposition, the framework attempts to break down the problem statement into key assertions. This is a logical exercise that focuses on distilling the problem statement, which may use imprecise language, into a set of more precise assertions. 
- Assertions are expected to be reusable and connect to multiple problem statements. This builds a body of knowledge over time and reduces work that participants need to redo.

### Premises

- Premises need to represent the simplest decomposition of assertions. The idea is that an assertion relies on one or more premises that justify the assertion. 
- Premises can be linked to multiple assertions.
- Premises should inherently be decomposed to a level where user sentiment can be expressed as either support or reject the premise. If a premise is too complex to be responded to in this manner, it should be reworked into multiple related premises and re-submitted.
- Premises will have a draft state and will require a certain level of consensus to be considered ready for review. _This is implementation specific_

### Policy Proposal Items

- Policy proposal items are user provided
- Policy proposal items can be re-used for different policy proposals
- The idea is that specific proposals are easy to understand and easy for the user base of the platform to determine support for or against
- Policy proposal items link to the original problem statement through assertions. The expected relationship is that an assertion will link 1:1 with one or more policy proposals. _Note: This relationship structure is under active development and will be refined in the decomposition process documentation._

### Policy Proposal

- A collection of policy proposal items. 
- This object is mostly just used as a container but can represent the policy narrative which is a real component involved in developing advocacy for the policy proposal as a whole
- The final phase of the process is essentially to produce a few versions of different policy proposals that feature different combinations of policy proposal items and narratives. Users can also vote specifically on the final state proposals to indicate which proposal they feel is the most effective policy proposal to address the original problem statement

## Key Processes

### Decomposition

Decomposition is the key process of the [Issue Phase](#issue-phase) that involves breaking a [Problem Statement](#problem-statements) down into continually smaller components. First to [Assertions](#assertions) which seek to clarify the key argument of the problem statement and then to [Premises](#premises) which are the foundational perspectives that underpin the Assertions.

The idea is that this process does 2 things:
1. Distills a problem statement down to its core argument
2. Makes review and discussion about the topics simpler as each topic is substantially reduced in scope and easier to research and validate

### Consensus Aggregation

Consensus Aggregation is simply the concept of allowing user-level voting to be aggregated up the object chain to establish an aggregated quantitative score. The general idea is to frame user response as either supporting or rejecting an object.

Consensus aggregation is primarily utilized in [Platform Mode](#framework-implementation-modalities) implementations (50+ participants) where systematic voting and quantitative scoring become necessary. Small Group Mode implementations typically rely on direct discussion and qualitative consensus building.

Consensus aggregation is expected to be used at multiple points across the system but will be contextualized to ensure users understand how their votes will factor into aggregation.

**Key Commitment:** All quantitative formulas used in Consensus Aggregation will be explained in detail in consensus.md. Transparency in quantitative process is critical for the health and objectivity of the framework, aligning with the project's [key tenets](../charter.md#key-tenets) of preventing oversized influence from any one source.

