---
description: >-
  Exploring what a new data model could look like for auditing and the relevant
  data groupings to be considered
---

# Auditing data model

## Data groupings

Based on the [current auditing process](current-auditing-process.md) the data groupings have been identified along with what information would be included.

****

**Proposer identity**

The proposer needs to verify their identity to prove they are part of a proposal team. In the short term this may be a matching email though in the future this would likely simply be a DID that is attached to the proposal when it gets created.&#x20;

****

**Proposal identity**

The proposer needs to verify that they own a given proposal to report any progress updates on it. In the short term this may be matching an email to verify along with the associated Ideascale proposal information (name or URL) however in the future this could be a proposal identifier value that is associated to the proposers DIDs.



**Progress report**

A progress report revolves around giving an overview of what has happened with the project over the recent weeks or month. This could be a project status change (e.g. in progress, blocked, completed), a what happened overview update, what is happening next, what went well, what didn't go well any any blockers.&#x20;



**Milestones**

Milestones are currently not added as a separate data structure in the Ideascale process nor are they part of progress reports. Milestones for proposals involve adding a break down of each grouping of work for a given proposal with details on what is included and estimations as to how long it will take to complete. If milestones were added to proposals then data could be added in progress reports for status updates on specific milestones with information relevant to that milestone. Milestones have a higher value on larger projects that should break down their projects into milestones so the community has an easier way to gage the progress against all the milestones they provided.



**KPI report**

The definition of each KPI for a given proposal should be available with general proposal data. The proposal team may want to update their KPIs every now and then when required but this wouldn't be a part of reporting KPI updates. A KPI report should allow a proposer to specify a KPI from the list of their proposal KPIs and provide a new value for the metric and optionally text to highlight any explanations or useful information about the new value.



## Reporting - proposal vs team vs project



**Proposal** - Reporting by proposal would mean that every proposal created should go through the full reporting process.

**Team** - Reporting by team would mean a self determined team making progress reports and adding further reporting details about proposals under the main team report.

**Project** - Reporting by project would mean having a self determined project that makes progress reports and adding further reporting details about proposals under the main project report.



**Analysis**

People often have projects with multiple proposals across funding rounds and also multiple proposals in a single funding round. Teams between proposals may often be fluid where someone may contribute to a few of the proposals people are working on but not the others. A group of proposals as a project is the stronger connection between related proposals as they are about a specific idea. People could have multiple projects with multiple proposals in each project - there are no constraints to the structure. The benefit of using projects as a reporting structure is it allows that project to provide reporting on the proposals they have worked on. In project structures there may be funded proposals that have not had any progress due to other funded proposals being the priority. The project structure helps keep reporting processes leaner and more efficient.

****

## **Data model**



### **Progress** **report**

**Data model**

```
{
    projectId: string,
    progressOverview: string,
    proposals: [
        {
            id: string
            status: ['not-started', 'in-progress', 'blocked', 'completed'],
            progress: string,
            upcomingWork: string,
            blockers: string
            milestones: [
                {
                    id: string
                    status: ['in-progress', 'blocked', 'completed']
                    url: string
                    progress: string,
                    upcomingWork: string
                }
            ]
        }
    ],
    successes: [
         {
           type: ['technical', 'commercial', 'team-and-leadership', 'partnership', 'project-schedule', 'education', 'other']
           description: string
         }       
    ]
    issues: [
        {
            type: ['technical', 'personnel', 'resource', 'financial', 'legal', 'partner', 'supplier-or-contractor', 'delayed', 'other']
            description: string
        }
    ]
}
```

**Data model descriptions**

```
{
    projectId: Unique project identifier, required
    progressOverview: Brief progress overview, required
    proposals: [ Proposals for the given project, required
        {
            id: Unique proposal identifier, required
            status: Current status for a proposal, required
            progress: Progress for proposal, required if not blocked
            upcomingWork: What work is being completed next, required if not blocked
            blockers: Blockers for proposal, required if blocked
            milestones: [ Milestones for proposals, optional
                {
                    id: Unique milestone identifier, required
                    status: Current status for the milestone, required
                    url: Link to find out more about the milestone progress, optional
                    progress: Progress update for the milestone, required
                    upcomingWork: What work will be coming next, optional
                }
            ]
        }
    ]
    successes: [ List of successes that happened, optional
         {
           type: Type of success
           description: Description of the success
         }       
    ]
    issues: [ List of issues that happened, optional
        {
            type: Type of issue
            description: Description of the issue and how it will or has been overcome
        }
    ],
}
```

### **KPI report**

**Data model**

```
{
    projectId: string,
    keyPerformanceIndicators: [
        {
            id: string
            value: number
            description: string
        }
    ],
}
```

**Data model descriptions**

```
{
    projectId: Unique project identifier, required
    keyPerformanceIndicators: [
        {
            id: Unqiue KPI identifier, required 
            value: New metric value for KPI, required
            description: Information about the KPI metric change such as new approaches used to increase the metric, optional
        }
    ],
}
```
