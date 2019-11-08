# QUIPP Kickoff Meeting

Problem: generating synthetic datasets from sensitive data, such that the synthesized data is *not* sensitive.

- understand existing methods for doing this
- what additional uncertainty is introduced by using synthetic data to draw conclusions?
- produce tooling to allow this to be used and evaluated in practice

Which algorithms are "best" for generating synthetic data?

What is the tradeoff between privacy and utility?

How to quantify the uncertainty introduced by these techniques?

Funder: SPF ASG (AI for Science and Government)

## Links with other project

Potential links: Projects in Health, Urban Analytics, Finance and Economics (FCA, BoE) programmes at Turing.  Finance programme may employ a researcher to look at similar questions.

AI Research Centre - Turing D&S

Existing work at Leeds: methods for producing synthetic data from e.g. health surveys.  Produce a synthetic population representative of the real population.  How does this change over time?

SPENSER involves synthetic populations from microsimulation, their change over time and uncertainty.  Investigate policy outcomes.  Can run many simulations quickly, given a policy.

Uncertainty in Agent based models for smart city forecasts - quantify uncertainties in results obtained from agent-based models.

Causal inference and agent-based modelling (Alison, with Mark Gilthorpe).  Idea is to take synthetic datasets (or data where an intervention is known to have been performed), and apply causal inference methods.

Bringing the Social City to the Smart City - Heppenstall ESRC/Turing Fellowship
Uncertainty in ABM for smart city forecasts - Malleson/Heppenstall Seedcorn
Casual inference in ABM - Heppenstall Seedcorn
SPENSER - Lomax Seedcorn
 
Related is another project from the Justice or public policy theme:
 
Computational models of police demand dynamics - Dan Birks/Alison Heppenstall

Sebastian: related work on existing projects in Health: currently compiling a guide for clinicians on privacy-preserving methods (e.g. HE), particularly tradeoffs and readiness.  What is privacy and how to measure it?  GANs, autoencoders for synthetic data.  Work with NHS Scotland, MHRA (have letter of support).  Relative performance of algorithms: how well are certain correlations preserved, for example.

Hazy (?), startup.  Visiting Turing 30.10.19.

Martin: other REG work:
- SHEEP (with Adria Gascon)
- Learning Machines (with Michela van der Shar) - machine learning in production (Health and Government)

Possible directions:
- GANs
- Autoencoders
- injecting noise into training data for NNs
- alignment between privacy-preservation and other measures of quality of the 
- identification attacks on NNs

Range of attacks, where the attacker has access to:
- single data point
- large sample
- arbitrary queries
- entire model


## Challenges, questions

- Privacy depends strongly on context: e.g. knowing an integer associated with a person is a phone number.
- Updating anonymised datasets
- What distinguishes the tools developed by this project from offerings from others (Google, Privitaar)?
    - being rigourous about the privacy aspects
- How can someone (in government and industry) determine if a technique/tool is suitable for their use case?
- Obtaining permission to use a synthetic dataset, as a result of processing a confidential dataset


## Data

Potential sources of sensitive datasets

- Leeds: Longitudinal surveys, individual data

- High-street retailer (Alison)

- P&G (Leeds)

- Medical data: additional access to data must make a case for the new science it would produce.  Additional challenges with access (who may use the data and what it can be used for).

- Representative but not disclosive data

- Finland open tax records

- ONS (census, more fine grained datasets)

- Potentially BoE, FCA (via Finance programme)

- A&E Triage data (via Sebastian) - already was used within a safe haven. 1.5M admissions.  Quite comprehensive individual-level data.

- Met police (via Police Demand Dynamics project)

- TfL

Link with data safe havens.  Can deploy and evaluate these techniques within a safe haven.  Synthetic data could be a lower "tier" than original dataset, if not entirely open, or opened up to more people.

General strategy: easier to gain access to a dataset via an individual researcher who "owns" it (rather than through the organization).

Allowing researchers to train and assess a variety of ML algorithms could be a strong motivator to open up the synthetic dataset.


## Deliverables and End Goals

TODO: add project brief

- discussion/review paper on methods and tools currently available
- benchmarks with examplar datasets (those with particular spatial structure, temporal structure)
- some literate analyses
- tool for presenting benchmark of utility (assessed by a variety of specific ML tasks and models) against privacy, across the privacy preserving techniques.

## Tasks/work packages

### First three months

- Put in place the ways of working framework
- Find initial, open data sets to use for the first analyses
- Put in place the pipeline, and do an end-to-end analysis
- Project website (GH pages/Netlify/Jekyll) and Turing website project page
- Project logo

Additionally
- Contribute to Nature Med. paper on privacy preserving techniques
- Colaborate with Finance programme project literature survey on these techniques
- Investigate access to sources of sensitive data (including those listed above).
- Consider follow-up funding

Idea for documentation: Jupyter book

## Practicalities

### People

SPENSER - make a "superteam" across both projects.  


### Ways of working

- Open from the start
- Put the benchmarking pipeline in place early
- Overview of work detailed as issues on project board (GH)
- Weekly project meeting
- Decide how to publicise results (with Comms team)
- Conferences?  Is there budget for this?
- Licensing: MIT-like for code, CC-By for documentation, papers etc (or Gold open access)


## Bibliography

https://datasciencecampus.ons.gov.uk/projects/synthetic-data-for-public-good/
