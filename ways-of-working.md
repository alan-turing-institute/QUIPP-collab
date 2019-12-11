# Ways of working

This document lists the QUiPP project team members and describes how we use GitHub and other tools to collaborate on the project.

## Project team

| Name               | Role                    | Proportion of time on project | Time period allocated to project |
| ------------------ | ----------------------- | ----------------------------- | -------------------------------- |
| Martin O'Reilly    |
| Alison Heppenstall |
| Nik Lomax          |
| Nick Malleson      |
| Sebastian Vollmer  |
| Greg Mingas        |
| Oliver Strickson   | RSE, REG lead           | 0.5                           | Oct 2019 - End                   |
| Louise Bowler      | Research Data Scientist | 0.5                           | Oct 2019 - ?                     |
| Kasra Hosseini     | Research Data Scientist | 0.5                           | Oct 2019 - ?                     |

There is a GitHub team, [QUIPP](https://github.com/orgs/alan-turing-institute/teams/quipp), within the
alan-turing-institute organization, that should contain everyone on the project team above.

## Communication

You can reach members of the QUiPP team through their preferred communication methods:
- ...
- ...
- Louise: I'm usually around on Slack (`@louise`) and GitHub (`@LouiseABowler`), and you can also reach me via email.
- Oliver: mailto:ostrickson@turing.ac.uk (preferred), Turing Slack (`@Oliver Strickson`), and I'm trying to get better at responding to GitHub mentions (@ots22)!
- ...

We have a private group Slack channel, `#quipp`, in the Turing's Slack workspace.
The REG team members will generally be available there, but remember that not everyone will check Slack regularly.

## Git repositories

There are likely to be multiple git repositories associated with this project, hosted on GitHub.

This repository (https://github.com/alan-turing-institute/QUIPP-collab) is for project-related discussions.
It is intended to remain **private**.

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

Issues can be tagged so that we can see at a glance what type of work they describe.
Tags are particularly useful for issues of the following types:
- Datasets: These issues contain ideas for datasets. They can be closed when we gain access to the data, or when we decide not to use it.
- Events: Events that team members may be interested in attending. They can be closed after the event.

When completed, issues should be closed right away.
This can be done by pressing the "Close issue" button when viewing the issue, or by including, for example, "Closes \#1" in the description of a pull request which implements the feature requested in the issue.


### Project board

The project board in this repository shows a high-level overview of our work on this project.

If an issue concerns another repository (for example, a bug in some software that we produce), it should be made in this
other repository, and and with discussions about it taking place there, instead of in QUIPP-collab (rationale: these
discussions belong with the contents of the repo that they refer to, and are then also publicly visible).

Since it is not possible to add issues in other repos to the project board, consider creating a stub issue in this repo
that links to more specific issues in any other repositories, and encourage any discussion to take place on these more
specific issues.

The four columns of the project board show our upcoming, current and completed work plans:
- Backlog: Ideas and actions that we will work on, but not right away.
- Upcoming: Issues that we will draw from when are ready to take on another task.
- In progress: Issues that we are currently working on. The relevant team member(s) should be assigned to the issue.
- Done: Issues which have been entirely completed or which won't be worked on.


## Zotero

We store relevant literature and notes in a shared [Zotero](https://www.zotero.org/) library, `SyntheticData`.
Everyone in the team is encouraged to add interesting papers, blog posts and other resources to the library.

To join the group, set up a Zotero account and ask an existing member to add you.
The existing member should then:
- In Zotero's web interface, select the "Groups" tab
- Select the "SyntheticData" group
- Click on "Group Settings"
- Click on "Members settings"
- Under "Member Invitations", select "Send more invitations"
- Add the new user's Zotero username or email into the box, then click "Invite Members"

To avoid duplication of effort when reading, we have attached short notes to some of the papers.
Notes can be added by clicking on the name of the paper, then clicking on the appropriate button in the panel on the right.

We have recently (December 2019) started using tags to indicate the method and whether utility or privacy metrics were discussed in each paper.
A list of the tags we currently use is below, and the most up-to-date version is kept in the `*Tag key` note in the SyntheticData library itself.
You can see tags in the bottom left corner of the screen; clicking on them filters the items by the relevant tag(s).
Similarly to notes, tags can be added by clicking on the resource, then selecting the "Tags" button at the top of the panel on the right of the screen.

You may also find it useful to hide auto-generated tags that are downloaded with the paper.
To do this, click on the small colour palette below the list of tags, and uncheck "Show automatic".

Our current list of tags is:
- **Microsimulation**: Describes/proposes/uses one or more microsimulation methods
- **MI**: Describes/proposes/uses one or more multiple imputation methods
- **GAN**: Describes/proposes/uses one or more GAN methods
- **Autoencoders**: Describes/proposes/uses one or more autoencoder methods
- **SMOTE**: Describes/proposes/uses one or more SMOTE methods
- **Parametric model**: Uses parametric models for synthesis (usually with MI but not always)
- **Non-parametric model**: Uses non-parametric models for synthesis (usually with MI but not always)
- **Bayesian model**: Uses Bayesian model for synthesis
- **Utility**: Describes/proposes/uses utility metrics
- **Privacy**: Describes/proposes/uses privacy metrics
- **Library**: Describes or contains a software library
- **Review/Survey**: Is a review or survey of various methods (or a tutorial)
- **Application**: Main focus of the document is solving a problem in a specific application area
- **Book**: Is a book
- **Dataset**: Is a dataset
