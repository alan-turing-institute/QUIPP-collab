# Quantifying UncertaInty and Preserving Privacy in Synthetic Data Sets (QUiPP)

## What's the problem?

- We know that the only way to answer key questions in x, y, z is to use data that is ultimately derived from sensitive personally identifiable data (examples)
  - Census data (small individual sample, aggregated population, 4 years in arrears, transient groups missing, bias from participation  imbalance)
  - Other government data on society (more real-time):
    - Tax records
    - Electoral register
    - Student records
    - Employment records
    - Migration records
    - Birth and death records
    - Land registry
    - Rental agreements (private and public)
  - Health records (rare diseases, combinatorial uniqueness)
    - Hospitals
    - GPs
- We know it's not ok to release these data sets
  - Research ethics / responsible AI
  - Legal restrictions
  - Consent / trust from - individual?s | public?
- Access control only goes so far and presents a high barrier to entry
  - Is privacy budget here or later?
  - is statistical disclosure control here or later
- Anonymisation not as easy as people may think
  - Not enough to remove names and identifiers
  - Obviously wrong toy example
  - Reidentification attacks - where it's gone wrong
- Lots of techniques proposed to de-identify data
  - Differential privacy approaches
    - Aggregation and noise with maths
  - Deep learning apporaches
  - Other well-known approaches
- Problem is we don't know how privacy and utility trade off with these techniques and how these introduce uncertainty into the data  (privacy - utility line on slide)
  - Totally secret -> Max privacy, no utility
  - Totally open unaltered -> Max utility, no privacy
  - In between some trade off where we buy privacy by reducing utility. Can we quantify how well privacy is preserved and the additional uncertainty introduced in the data?
  - Don't know where the various privacy preservation techniques lie on this line
- How do data providers, research subjects and public:
  - Understand how the algorithms and measures work
  - Trust that privacy is sufficiently preserved
  - Trust that utility is sufficently preserved (e.g. relevant relations and structure preserved, no additional bias introduced)
- That's what we're doing

## What are we doing?

- We're making a **tools** to allow people to:
  - Quantify the balance between preserving privacy and preserving utility
  - Understand how uncertainty is propagated within a system
- We're considering how methods and measures depend on the domain
  - How do these depend on the structure of the data (e.g. time series, spatial structure)?
  - How do these depend on how the data is generated (e.g. one-off snapshot, regular updates, streaming, introduction of new variables)?
  - How do these depend on the questions being asked of the data (e.g. classification, regression, simulation)?

- We're **not**:
  - Making new data synthesis techniques
  - Making new uncertainty propagation techniques
  - Generating new sensitive data sets
  
- We **are**:
  - Evaluating existing techniques, and providing tools for you to do the same
  - Taking techniques from specific domains and applying them across new domains
  - Generating new synthetic data sets
  - Adapting and extending techniques for **quantifying** privacy preservation, utility preservation and uncertainty quantification
  - Make all our tools, analyses and guidance available under permissive open source licences

## How can we help you?
- Generate less sensitive versions of your sensitive data
- Understand how various privacy preserving techniques trade off privacy and utility for **your** data

## How can you help us?
- Access us to sensitive data sets
- Understanding the structure of your data
- Understanding the questions you are asking of it
- Validating our measures of privacy and utility preservation for **your** data and questions

## How are we working?
- Open data, analysis and guidance
- Collaboratively (come work with us)
- Reproducible, extensible tools to let people incorporate **their** data and data science analyses
- Something to set expectations around what we can do ourselves
  - Highlight end to end tool set 

## Links to other projects
- RADDISH: Incorporating reeal-time data into disaster response
- SPENSER: Generating custom dynamic synthetic populations
- Computational models of police demand dynamics: Understanding dynamics of police demand
- SIPHER: Early years health interventions
- Other health examples from Sebastian
- Data Safe Haven (we don't need perfection, we can safely share data with wider researcnh audience while providing access to data science tooling)
- Turing Way: Dissemination of learning
- Ethics in AI: Transparency and interprebility  
- Your project here

