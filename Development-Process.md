## Roadmap
The team has a 6 months high level [[Roadmap]] which defines high-level themes and features to be addressed in this timeframe.

## Iterations
We will work in 3 weeks iterations on the items on the roadmap. All the work is organized by milestones, which subsequently will be broken down into user stories and tasks. 

At the end of each iteration we want to have a version of Superblocks Lab that can be used by the Superblocks community. The work planned during an iteration is captured in the iteration plan (see [[Iteration Plans]]). The feature highlights of each iteration are highlighted in the release notes.

## Planning

Before each iteration, we will prioritize features to implement and bugs to fix in the upcoming iteration. For new features, we create new issues and label them with `Plan Item`. Plan Items include a checklist for the `Definition of Done`. The Bugs, Plan Items, and Feature Requests assigned to a milestone encompasses the planned work for the upcoming 2 weeks. For each Plan Item, we include the checklist for:
 
### Definition of Done
- [ ] Test Plan Item created
- [ ] Release notes updated

## Inside an Iteration
We work in 3 weeks segments:
- **Week 1**: Work according to the plan 
- **Week 2**: Work according to the plan
- **Final Week**: The final countdown
  - the team tests the new features according to a test plan and updates the documentation. 
  - we make a pre-release available on the 'beta' channel and invite users to help us test the pre-release.
- **Week 1 (next iteration)**: 
  - monitoring the pre-release and fixing critical issues.
  - publish the release, sometime midweek, after 24 hours with no changes to the pre-release.

## Triage
Bugs and features will be assigned a milestone and within a milestone they will be assigned a priority. The priority dictates the order in which issues should be addressed. An `important` bug (something that we think is critical for the milestone) is to be addressed before the other bugs. 

To find out when a bug fix will be available in an update, then please check the milestone that is assigned to the issue. 

Please see [[Issue Tracking]] for a description of the different workflows we are using.

## Weekly
Each week we will manage work items, crossing off completed features, and triaging bugs. At the end of the milestone, we will strive for 0 bugs and 0 issues assigned to the milestone. Some bugs and features will then be either postponed to later milestones or moved back to the backlog.

Before we publish builds we manually execute the [[Smoke Test]] on all supported browsers.

## Its The Final Countdown!
The final week of the milestone is what we call the "The Final Countdown". During this week we will wrap up any feature work, we will test using a test plan Iteration Plans, and then we will fix the critical bugs for that milestone.

During the Final Countdown we make a build available on the beta channel. We will monitor incoming issues from this release, fix any critical bugs that arise, and then produce a final stable release for the milestone and the stable channel.
