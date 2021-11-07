# Data model design decisions

### 1. Keeping progress reports and KPI reports separate

Progress reports should give an update of what has happened since they started or the last progress report. KPI reports gives an update for the latest results that what metrics they are tracking. The reason these should be separate is the regularity of reporting is up to the project team. Some projects may want to report at a different regularity for progress reports compared to KPI reports. Some projects may wish to do daily, weekly or bi-weekly KPI reports if that is relevant or useful for their project. Proposers may also want to automate the KPI reporting process by connecting it with APIs that supply analytics data in future iterations of the auditing process. Due to this it makes sense to keep these two types of reporting separate.



### 2. Reporting against proposals instead of projects or teams

Progress reports could be reported from different perspectives:

**Proposal** - Reporting by proposal would mean that every proposal goes through the auditing process separately. This is how it is currently done.

**Team** - Reporting by team would mean a defining team members who make progress reports that adding their progress and KPI reports under a main team report.

**Project** - Reporting by project would mean having a number of proposals under a single project that means reporting progress and KPIs about proposals will be visible under a main project report.

****

For reporting by teams this has the main issue that teams for many projects in Project Catalyst and web 3.0 in general are more dynamic and fluid. Contributors come in and out of projects for both short and longer periods of time with different levels of commitment and type of contribution. Reporting by team would then face this complexity.

Reporting by project in many cases is more effective than by proposal as it helps to indicate what proposals a given project is focussed on at the moment. For one proposal a project team may have little progress where as another proposal may be the main priority. By combining proposals under a project grouping it makes it easy to see what is happening overall. The issue with reporting by projects is some people may make a number of proposals that are not linked together. In this instance they would not benefit from having a project based reporting and nesting single proposals into a new structure.&#x20;

Reporting by proposal is what is currently done. This works as it means every funded proposal will go through the same reporting process and keeps the community up to date on each proposal. The downside is without being able to easily see the linking between proposals under a project grouping it can be misleading to people if one proposal isn't performing when it may be because there are other priorities within a wider project.

Due to the above it makes sense to continue to report by proposals with only the required information. However due to the issues of projects having multiple proposals it will also be important for proposals to eventually be grouped under a project if they want to. The important part is this project grouping should be optional. Allowing this would mean the community can see the overall picture for projects with multiple proposals where necessary but can also just see individual proposals reporting as well.



### 3. Adding milestones

Milestones aren't a part of the existing Ideascale process which makes it more difficult to more easily show progress for a proposal at a glance. By allowing proposals to add milestones it will provide a way to show how the proposal is structured into manageable chunks of work and more easily report against which items in the milestone list are completed. In the future this could be integrated into the entire process to help improve decentralized decision making.



### 4. Reporting progress instead of upcoming work

When doing progress reports you can include what the proposers have done since their last report but could also include what they are doing next. What a proposal team is working on next may be useful information but shouldn't be required in a progress report as it doesn't help with auditing and can be easily be exaggerated. Reporting what has been done with related evidence is more factual on what has happened. Proposers when reporting what has happened may decide to include information about upcoming work where necessary and also will likely discuss this in a roadmap or live check in sessions. Reporting can focus most heavily on what has actually happened.



### **5. Proposal progress status values**

Adding status values for progress reports from a fixed list of options adds an easy way for the community to see what is happening in a given proposal. This status value give high level information about whether a project hasn't started, is in progress or is completed.&#x20;

The progress status value does not deal with whether the milestones are fully reached when completing a proposal - only that execution is finished regardless of the outcome. Instead of this status value being added to a progress report it could be add in a completion report that indicates what a proposal team set out to do and what actually got completed.



### **6. Reporting types instead of success and issue types**

The current success and issue options in the current auditing process don't capture enough of the success and issue types that can occur. For instance legal is added under potential issues though this could also be a success reporting type for a team. Often the same type of things that can be a success can also be an issue. Other types listed are also often similar such as team and leadership, personnel and supplier or contractor all deal with the collaboration within a project.

**Note - **The following suggested types could be more granular to be more specific however this would come at the cost of usability when reporting. The purpose of the reporting types is to add more context to the issues that are raised by proposal teams that categorises them so they can be viewed by the community and more easily get informed and involved where necessary.

{% embed url="https://gist.github.com/georgelovegrove/9707516222a0da0630c65b964cc2f2cf" %}

### 7. Reporting blockers - Issue specific rather than overview reporting

Proposals could report blockers generally in a single piece of information and have a status update to their proposal to indicate they are blocked. Alternatively they could also mark specific issues in a progress report as blockers.

**Reporting blockers as an overview**

* Have a top level blocked status makes it clear the proposal isn't progressing.
* Top level overview and blocked status fails to communicate granularity of the blocker - Is there one or multiple? What is it about? The community would need to read to understand the blocker more specifically.
* Gives proposers an easier path to add only information about being blocked rather than a proper progress update on other areas they may be working and more specifics about the blocker.&#x20;

**Reporting blocks in issues**

* Proposal status changes can be more one way directional going from not started to in progress to completed or uncompleted. This would make overall proposal status changes easier to follow.
* Individual issues can be marked as being blocked where the proposer can add extra information about why they are blocked and how they intend to overcome the issue. This makes it easier for the community to find exact reasons why proposals are blocked making it easier for relevant people to specific problems to jump in and help.
* Marking issues as blockers helps to not prevent progress updates being given on other areas of the proposal that may not be blocked.

Overall by marking specific issues as blockers it should help encourage better reporting behaviour by allowing proposers to give updates on any part of the proposal and to individually mark issues that are blockers when necessary. Most community members will only be able to help out in certain areas. If it is easy to find proposals with issues that they can help with then this reduces the friction and increases the likelihood that they help more proposal teams.



