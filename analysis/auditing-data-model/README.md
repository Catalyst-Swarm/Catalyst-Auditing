---
description: >-
  Exploring the different data groups relevant for auditing and what a new data
  model could look like
---

# Auditing data model

Review the [data model design decisions](data-model-design-decisions.md) to understand how this data model was created.

## Data groupings

Based on the [current auditing process](../current-auditing-process.md) the different types of data can be identified and grouped along with a description of the data.

***

### **Identity**

**Proposer identity**

The proposer needs to verify their identity to prove they are part of a proposal team. In the short term this may be a matching email though in the future this would likely be a DID for each team member that is attached to the proposal when it gets created.

**Proposal identity**

The proposer needs to verify that they own a given proposal to report any progress updates on it. In the short term this may be matching an email to verify along with the associated Ideascale proposal information (name or URL) however in the future this could be a proposal identifier value that is associated to the proposers DIDs.

****

### **Proposal management**

**Milestones**

Milestones are currently not added as a separate data structure in the Ideascale process nor are they part of progress reports. Milestones for proposals involve adding a break down of each group of work for a given proposal with details on what is included and estimations as to how long it will take to complete. If milestones were added to proposals then data could be added in progress reports for status updates on specific milestones with information relevant to that milestone. Milestones have a higher value on larger proposals that should break down their execution plan into milestones so the community has an easier way to gage the progress against the milestones they provided.

**KPIs**

Proposals currently should add success metrics that they are going to record for their proposal. These are currently added in the main text of the proposal and are not managed individually with their own identifiers. To more effectively report KPIs against proposals these KPIs should be stored with their own identifiers that proposers will use when reporting against them. This prevents a proposer from needing to write the KPI in each KPI report. KPIs can also change over time or be added to as the team learns about a better way to measure success of their proposal. This another reason why proposers need to be able to manage the KPIs they are recording.

****

### Reporting

**Progress report**

A progress report revolves around giving an overview of what has happened with the proposal over the recent weeks or month. This could include a proposal status change (e.g. in progress, blocked, completed), an overview of what happened, what went well, what didn't go well any any blockers.

**KPI report**

The definition of each KPI for a given proposal should be available with general proposal data. The proposal team may want to update their KPIs every now and then when required but this wouldn't be a part of reporting KPI updates. A KPI report should allow a proposer to specify a KPI from the list of their proposal KPIs and provide a new value for the metric. Optionally they may want to add text to highlight any explanations or useful information about the progress of any particular KPI.

## **Data model**

****

### **Proposal management**

A data model for the milestones and KPIs that a proposer should be able to add to their proposal and manage.

**Data model**

{% embed url="https://gist.github.com/georgelovegrove/8ba984a5b4662d7b92fb75bd1a6890e3" %}

****

### **Progress** **report**

**Data model**

{% embed url="https://gist.github.com/georgelovegrove/9169ae0c13b108b809ef27748c997370" %}

****

### **KPI report**

**Data model**

{% embed url="https://gist.github.com/georgelovegrove/8b259fd91fe2a1954663be8bb19b5009" %}
