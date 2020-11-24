# Ways of working

This document lists the QUiPP project team members and describes how we use GitHub and other tools to collaborate on the project.

## Project team

There is a GitHub team, [QUIPP](https://github.com/orgs/alan-turing-institute/teams/quipp), within the
alan-turing-institute organization, containing everyone on the project team below.

Current team members are:
- [martintoreilly](https://github.com/martintoreilly) (PI)
- [geoalison](https://github.com/geoalison) (Co-I)
- [niklomax](https://github.com/niklomax) (Co-I)
- [nickmalleson](https://github.com/nickmalleson) (Co-I)
- [volmersj](https://github.com/volmersj) (Co-I)
- [gmingas](https://github.com/gmingas) (REG)
- [ots22](https://github.com/ots22) (REG)
- [kasra-hosseini](https://github.com/kasra-hosseini) (REG)

Former team members:
- [crangelsmith](https://github.com/crangelsmith)
- [LouiseABowler](https://github.com/LouiseABowler)

## Communication

- We have a private group Slack channel, `#quipp`, in the Turing's Slack workspace (the REG team members will generally be available there, but remember that not everyone will check Slack regularly).

## Git repositories

There are likely to be multiple git repositories associated with this project, hosted on GitHub.

- This repository (https://github.com/alan-turing-institute/QUIPP-collab) is for project-related discussions.
- (https://github.com/alan-turing-institute/QUIPP-pipeline) is 

When creating other repositories on GitHub - to host software produced by the project, for example - please make
sure that, unless there is a specific reason not to:
- they have "public" visibility
- they contain an MIT-style licence, in a file called "LICENCE".  An exception to this may be in the case of forks of
  other software.
- they carry the `hut23` and `hut23-406` topics: these may be used to find the repositories associated with this project
  (by us and others)
- the team "QUIPP" should be granted at least "Write" permission (under Settings > Collaborators and Teams)

## Project management with GitHub

### Issues

Our upcoming work should be described in issues.

As well as a description of a task, issues can contain updates on progress and questions and comments from the rest of the team.

If it is clear who will work on an issue, that person should be assigned to the issue.

Labels can be added to issues so that we can see at a glance what type of work they describe.

Issues in this repository exist to collect notes and discussion around particular topics.  These should have one of the following labels:
- **Datasets**: These issues contain information about particular datasets that we are using or interested in.
- **Literature**: To collect discussion on particular papers (but see also Zotero, below - most papers there will not need an issue).  They should contain a link to the Zotero item.
- **Software**: To collect discussion on related software developed by others.
- **Events**: Events that team members may be interested in attending. They can be closed after the event.

### Project board

The [project board](https://github.com/alan-turing-institute/QUIPP-collab) in this repository shows a high-level overview of our work on this project.

If an issue concerns another repository (for example, a bug in some software that we produce), it should be made in this
other repository, with discussions about it taking place there, instead of in QUIPP-collab.

Since it is not possible to add issues in other repos to the project board, consider creating a stub issue in this repo
that links to more specific issues in any other repositories, and encourage any discussion to take place on these more
specific issues.

The four columns of the project board show our upcoming, current and completed work plans:
- **Backlog**: Ideas and actions that we will work on, but not right away, and in no particular order
- **Upcoming**: Issues that we will draw from, in order (top first), when are ready to take on another task.
- **In progress**: Issues that we are currently working on. The relevant team member(s) should be assigned to the issue.
- **Standing**: Issues that should be revisited regularly (and not closed)
- **For review**: Issues that are complete or near completion, but need review before they can be closed.  This includes issues containing discussion

#### Notes 
- There is no 'Done' column: just close an issue, and remove it from the project board, when the work on it is complete.
- Add issues to the board that correspond to tasks that we can work on.  Some issues in this repository should not be added to the board, because they are not tasks we can work on (for example, anything with the labels 'literature', 'software' or 'dataset').

## Zotero

We store relevant literature and notes in a shared [Zotero](https://www.zotero.org/) group library, [SyntheticData](https://www.zotero.org/groups/2386186/syntheticdata).  You will need to be a logged-in member of the group to see it (see below).

Everyone in the team is encouraged to add interesting papers, blog posts and other resources to the library.  Some papers in the group have short notes attached.

To join the group, set up a Zotero account and ask an existing member to add you.

To add a new member to the group:
 - Visit https://www.zotero.org/groups/2386186/settings/members
 - Under "Member Invitations", select "Send more invitations"
 - Add the new user's Zotero username or email into the box, then click "Invite Members"

Some of the entries have tags to indicate the class of method to which they relate, and whether utility or privacy metrics were discussed in each paper.  The `*Tag key` note in library has the complete list.
