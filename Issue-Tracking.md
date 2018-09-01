This page describes how we track issues in the `superblocks-lab` repository.

## Popular queries

- [Inbox tracking](https://github.com/SuperblocksHQ/superblocks-lab/issues?utf8=%E2%9C%93&q=is%3Aopen+no%3Aassignee+-label%3Afeature-request+-label%3Aplan-item+)
- [Verification Needed](https://github.com/SuperblocksHQ/superblocks-lab/labels/verification-needed)


## Inbox tracking and Issue triage
New issues or pull requests submitted by the community are checked by a team member. We have setup a bot which notifies us when a new issue is posted in the repository.

### Inbox Tracking

The [Inbox query](https://github.com/SuperblocksHQ/superblocks-lab/issues?utf8=%E2%9C%93&q=is%3Aopen+no%3Aassignee+-label%3Afeature-request+-label%3Aplan-item+) contains all the
- **open issues or pull requests** that
- are **not feature requests** nor **test plan items** nor **plan items** nor **extension candidates** and
- have **no owner assignment**.

The **inbox tracker** should do the following initial triage:
- Is the issue **invalid**? Close it and justify the reason.
- Is the issue **a general question**, like *How can I compile TypeScript*? Close it and redirect the user to [Stack Overflow](http://stackoverflow.com/questions/tagged/superblocks).
- Else, assign the issue to the **owner** of a feature area.

**Everyone** should do the following secondary triage to their assigned issues (the **inbox tracker** may do some of these steps too, if obvious):
- If an issue needs more info, assign the `needs-more-info` label, add an assignee (yourself if still unknown) and ask for more information in a comment.
- Ensure that the issue has a **type** label, that is, `bug`, `feature-request`, `debt`, `needs-more-info`
- Do a best effort to identify duplicates
- If the issue is a feature-request then the initial owner optionally unassigns himself from the issue.
- If the issue is an important `bug`, assign an `important` label.
- If the issue needs to be fixed in this release, assign it to the current milestone (eg: blocks a scenario, completes a new feature, etc.).
- If needed, follow-up with the author.

#### GitHub issue tracking tip

Use `l` and `a` to quickly edit labels and assignees.
See a complete list of GitHub shortcuts [here](https://help.github.com/articles/using-keyboard-shortcuts/#issues-and-pull-requests). (Or try pressing `?` when not focusing any input field on GitHub's UI)

### Ongoing Issue Management
- We close issues that we are not planning to work during the next 12 months. (Adding the `*out-of-scope` label lets the bot close the issue and add a generic comment.)

### Planning
During the iteration planning process we use the following sources as input:
- Review feature requests with many reactions.
Issues we plan to work on during an iteration are assigned to the current milestone.

## Filing bugs as development team member
When team members files a bug they perform steps of the inbox tracker for the issue they filed. Therefore bugs filed by the development team do not need to be triaged by the inbox tracker. 

## Verification

Issues need to be verified.

Verification is a service that you request from others either implicitly with the `bug`-label or explicitly with the `verification-needed`-label.


Follow the these rules:

1. Query for issues that are to be verified
2. Start with issues you created (filter by `Author`) but didn't close
3. Pick an item
    - Start with setting `verified`-label (prevents duplicate verifications)
    - Verify the issue
    - If you cannot verify the issue due to missing or hard-to-understand repro steps, add a `verification-steps-needed` label and remove the `verified` label
    - If the issue still shows, add the `verification-found`-label and remove the `verified` label
    - Go back to #3

## Duplicates
Duplicate bugs are closed with a comment `duplicates #issue`. Please try to reference an earlier issue **unless** a later issue is more appropriate (has more context, better scenarios, repro steps, etc.).
