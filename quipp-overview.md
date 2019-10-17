# Quantifying UncertaInty and Preserving Privacy in Synthetic Data Sets (QUiPP)

## What's the problem?

- We know that the only way to answer key questions in x, y, z is to use data that is ultimately derived from sensitive personally identifiable data (examples)
- We know it's not ok to release these data sets
- Access control only goes so far and presents a high barrier to entry
  - Is privacy budget here or later?
  - is statistical disclosure control here or later
- Anonymisation not as easy as people may think
  - Not enough to remove names and identifiers
  - Obviously wrong toy example
  - Reidentification attacks
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
  - That's what we're doing

## What are we doing?

- We're making a **tools** to allow people to:
  - Quantify the balance between preserving privacy and preserving utility
  - Understand how uncertainty is propagated within a system
- We're considering how quantifying privacy, utility and uncertainty depend on the domain
  - How do these depend on the structure of the data?
  - How do these depend on the questions being asked of the data?

- We're **not**:
  - Making new data synthesis techniques
  - Making new uncertainty propagation techniques
  - Generating new sensitive data sets
  
- We **are**:
  - Evaluating existing techniques, and providing tools for you to do the same
  - Taking techniques from specific domains and applying them across new domains
  - Generating new synthetic data sets
  - Adapting and extending techniques for **quantifying** privacy preservation, utility preservation and uncertainty quantification

## How can we help you?
- Generate less sensitive versions of your sensitive data
- Understand how various privacy preserving techniques wprk on your data and how privacy and utility trade off

## How can you help us?
- Access us to sensitive data sets
- Underastanding the structure of your data
- Understanding the questions you are asking of it
- Sense checking our measures of privacy and utility preservation
