# QUiPP Catch-Up and Retrospective

Friday 6th December 2019

Present: Louise, Oliver, Camila, Greg, Martin, Kasra


## Agenda

| Time   | Activity |
| ------ | -------- |
| 1pm    | Welcome to Camila! |
| 1:10pm | Pipeline catch-up |
| 1:45pm | Retrospective |
| 2:20pm | Plans for the next few weeks |


## Welcome to Camila!

_A quick overview of the project; put any useful notes/to-dos below._

Oliver and Camila have caught up already :white_check_mark:

## Pipeline catch-up

_Aim for five minutes each, with extra time hopefully available for questions etc._ :hourglass:

- Greg: `simPop` pipeline - microsimulation, or other applications. Use iterative proportional fitting to get weights of individuals, then extend to get population. Not so much of a focus on privacy in the package.
- Kasra: Went through course to understand GANs better. Measure of similarity between synthetic and real data: add synth data to minority class and see how recall is affected.
- Louise: Microsimulation with `humanleague`. Some questions about licensing but I'll include a separate licence for the initial go with the method. Coming soon - application to different datasets; will investigate those Greg has used in other microsimulation pipeline.
- Oliver: `MICE`. Targeted for filling in records. Synthetic data - insert blank row, then impute values. Different options for algorithms used. Also differential privacy - put outcomes in report.

Let's keep an eye out for methods that have commonalities - can we make parts of these pipelines easier to reuse?

## Retrospective

_About half an hour for the four points, then five minutes to wrap up and think about future actions._

We'll follow the Atlassian [_Retrospectives_](https://www.atlassian.com/team-playbook/plays/retrospective) team playbook (four Ls variation) suggested by Oliver.

Let's think about our experiences on QUiPP so far - from the start of the project or whenever your involvement began.

We'll go through each of the four points one-by-one. Take a couple of minutes to generate post-its with your thoughts on that point, and then we'll try to group our post-its on the board. If we can come up with any actions we'd like to take as a result of these points, let's write them up and take them forwards.
- What did you like?
- What was lacking?
- What did you learn?
- What do you long for going forward?

### Outcomes

#### What did you like?
- Project combines research and coding
- Other people say "this sounds really useful"
- Interest and connections from outside the project team
- Scale and ambition of the project
- Working in a big team
- Range of tooling
- Proximity/talking about things between meetings
- Exploring a wide range of ideas
- Discussion on privacy vs utility
- Enthusiasm for getting ways of working right
- Explore lots of different methods
- Hear about other different methods
- Wide range of experience from team
- Sharing information through GitHub repos is working well
- Topic is interesting with many applications
- Addition of CI early on
- Working openly
- Open code
- Organised GitHub issues
- Brainstorming sessions
- Learning from others
- Connections between different techniques


#### What was lacking?
- Synchronisation with other team members
- Medium/long-term structure/roadmap/milestones
- Clarity of goals
- No recent experience in approaching a domain area change
- Limited number of useful libraries/repos for GAN
- Time! (And quality of that time)
- Time
- Large blocks of time
- Evaluation methods for different techniques
- (In first weeks) Progress wasn't necessarily visible
- Contact with external stakeholders
- Datasets that are easy to "have a go with"
- Timeframes/milestones aren't clear
- Allocation of work/tasks isn't always clear
- What should be prioritised?
- How do we manage overlap?
- Sometimes felt "siloed" (opportunities for knowledge sharing)
- REG subteam feels closer-knit than wider project team
- Elements of the scope: datasets applications, look of the final tool


#### What did you learn?
- GitHub actions
- Census data
- Differential privacy
- Microsimulation - techniques and different types
- SDC, multiple imputation
- Applications
- Basics of generative models
- New topics, specifically utility
- Why privacy is important
- R
- Important to take a step back from so many ideas; good to have a person in charge of that
- Ways of working
- Imputation methods


#### What do you long for going forward?
- Start integrating pipelines
- Team social
- GAN on more types of data
- Compare utility and privacy of different methods
- Use QUiPP to help other projects
- Repository that contains useful examples (maybe interactive with Binder)
- Enough confidence in utility+privacy to release a synthetic datasets for someone's project
- Find more time to work on QUiPP
- A simple and medium-sized dataset sanctioned by someone who has a complex private dataset
- State of the art in generative models
- Team logo
- Find a few types of data for which utility/privacy are important
- Clarify milestones and goals
- Discover what we still don't know
- Dumping accumulated knowledge into a report/paper
- Keep on learning - develop a good understanding of several methods
- More regular opportunities to synchronise as a team
- Chance to play with CI tools

### Actions
- We have dates in the diary for our future meetings - should help with syncing up.
- Can we have a strategy meeting at some point? First one in January? Circulate planning document?
- Time - set times should help.
- Goals aren't so clear - can we think more about the problems that the Co-Is have? Can Co-Is provide examples of open datasets that might be useful to work with?
- Camila has access to data from AIDA that might make for nice examples - talk to James G.
- CI tools - let's each make sure our own parts of the pipeline can be run using CI
