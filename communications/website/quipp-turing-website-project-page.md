

## Project title
Quantifying Utility and Preserving Privacy in Synthetic Data Sets (QUIPP)

## Organisers
- Dr Martin O'Reilly (The Alan Turing Institute)
- Dr Alison Heppenstall (University of Leeds)
- Dr Nik Lomax (University of Leeds)
- Dr Nick Malleson (University of Leeds)
- Dr Sebastian Vollmer (The Alan Turing Institute, University of Warwick)

## Details

- Project page main contact
- Name: Martin O'Reilly
- Email: moreilly@turing.ac.uk
- Start: 01 Oct 2019
- End: 31 Mar 2021

## Content
### Project sub-heading *
> - 1 sentence summary/sub-heading
> - 1 sentence, present tense, e.g. Using…, Developing…, Investigating…_

Understanding the balance between utility, privacy and the uncertainty associated with synthetic data sets.

### Brief description *

Clear, concise, ~3 sentences – e.g.
> - 1st sentence: the problem being addressed
> - 2nd sentence: the potential solution/method
> - 3rd sentence: applications, output

Sensitive datasets are often too inaccessible to make the most effective use of them (for example healthcare or census micro-data). Synthetic datasets are an alternative, but poorly understood in terms of how well they preserve the privacy of individuals on which the synthesis is based, and also of their utility (how representative of the underlying population the data are).

We are evaluating how well data synthesis methods preserve both individuals’ privacy and the utility of datasets for analysis. Where methods sufficiently preserve both privacy and utility, then synthetic datasets could be made available in more accessible environments.

Generating synthetic data introduces additional uncertainty compared to the original dataset. We are quantifying this uncertainty and understanding how it propagates through space and time when synthetic data is used for modelling purposes.

We are evaluating a range of data synthesis techniques in the contexts of both health and urban analytics applications and developing an open-source pipeline for data owners to easily use to evaluate the potential effectiveness and impact of using synthetic data for their own applications.

### Aims/expected outcomes *

> - What is the work hoping to achieve?
> - What would define success?
> - Why is this work worth doing?
> - 100-300 words

We are evaluating a range of existing synthetic data generation techniques to understand how they ensure the privacy of individuals yet remain useful for answering the same research questions as the original sensitive dataset. This will involve evaluating these data synthesis techniques against a range of privacy and utility measures.

We are also evaluating the uncertainty introduced by these data synthesis methods and how this uncertainty propagates when the synthetic data is combined with other data and is used in simulations that evolve in space and time.

In addition to making our analysis reproducible and openly available, we will also ensure that we make our work reusable by others by packaging our evaluation code into robust, reliable, reusable benchmarking tools. These tools can be used by researchers, practitioners, data holders and other stakeholders to evaluate these data synthesis techniques for their own datasets and application contexts.

We will develop our open benchmarking tools to ensure that it is easy for others to add additional data synthesis methods, evaluation datasets and measures for evaluating privacy, utility and uncertainty.

### Explaining the science *

> - Is there theory or methods that would be good to explain to understand the project’s work better? 
> - Use plain English where possible
> - 100-300 words

There are a variety of methods for generating synthetic microdata: our goal is to include as wide a range of these as possible in our evaluation platform.  We ensure that it is straightforward for any user to extend the platform by adding new methods into the benchmarking pipeline. For an overview of some key data synthesis methods [see this review from the ONS](https://datasciencecampus.ons.gov.uk/projects/synthetic-data-for-public-good/) and [this review that deals with microsimulation methods](https://ideas.repec.org/a/ijm/journl/v7y2014i1p4-25.html).

Once data has been synthesized, we want to know:
- Is it useful for replacing real individual-level data in a given application?
- What is the privacy risk to the individuals in the original dataset?

The first of these questions, on the utility of the data, strongly depends on the nature of the application, and this means having a flexible platform for specifying and quantifying many such measures.

Privacy preservation offers a wealth of theoretically-based and also more ad-hoc methods.  These ultimately aim to measure the risk to an individual when certain information is released. This applies to synthetic records too, since the synthesis depends on some individuals' data, which might be sensitive.  The underlying idea is often to perturb the underlying data, or parameters of a model, with some noise.  The results of these methods can sometimes be related to one another, but often they are incompatible, and not all measures of privacy are applicable to each synthesis method.  This makes it important to clearly present any privacy results, their implications, and link to their theoretical underpinning where possible.

We are exploring existing and novel techniques to quantify the privacy of a synthesised data set. These include data-driven methods which are independent of the synthesis algorithm used, as well as methods that embed privacy in the synthesis process. A few examples include:

  - Differential privacy
  - Plausible deniability
  - Adversarial methods

### Real world applications *
> - Where is this work being applied, what area/industry could it benefit?
> - 100-300 words

Sensitive data is critical for research in a range of fields, including healthcare, finance and government. The ability to reliably generate less sensitive synthetic datasets that are still useful in answering research questions of interest would enable this data to be made more widely available and enable a wider community of researchers to engage with these problems.

We are working with colleagues developing a [Triage dashboard for hospital emergency departments](https://www.turing.ac.uk/research/research-projects/analytics-dashboard-ae) to evaluate to what extent synthetic data can be used in place of sensitive patient data in the development of algorithms to support the patient triage process in hospital emergency departments.

We are also collaborating with researchers from [University College London Critical Care Health Informatics Collaborative](https://hic.nihr.ac.uk/) to evaluate whether data synthesis techniques can generate privacy preserving versions of their critical care patient data.

In many cases, researchers are already working with datasets that have been de-identified or otherwise altered to preserve the privacy of the individuals to which the data pertains, often resulting in a reduction in the resolution of the data with respect to various properties (e.g. location, age, timing). In these cases, data synthesis techniques are often used to recreate the detail that is lost in the de-identification process and understanding the uncertainty these techniques introduce is important when interpreting the data and simulations that rely on it.

We are working with colleagues on the Turing's [SPENSER](https://www.turing.ac.uk/research/research-projects/synthetic-population-estimation-and-scenario-projection) project, who are using synthetic data generation techniques to generate more fine-grained regional and local census datasets from national level microdata samples. We are helping them evaluate additional data synthesis techniques that support dynamic population models and to understand how the uncertainty introduced by these synthesis techniques propagates through their simulations as they evolve in space and time.

### Recent updates

- [Mini workshop at SSI Collaborations Workshop 2020](https://software.ac.uk/cw20/mini-workshops-and-demo-sessions#4.3): Presentation of current progress of the project along with a demo of an early version pipeline.

### Sensitivities
> - Are there likely to be any sensitivities within or around this project?
> - For example it deals with highly sensitive subject matter such as abuse, violence, grief, etc

- [ ] Yes, there are sensitivities 
- [x] No, there aren't any sensitivities

### People
#### Participating researchers
> - Please include titles and affiliations for all participants

- Dr Oliver Strickson (The Alan Turing Institute)
- Dr Louise Bowler (The Alan Turing Institute)
- Dr Kasra Hosseini (The Alan Turing Institute)
- Dr Camila Rangel Smith (The Alan Turing Institute)
- Dr Grigorios Mingas (The Alan Turing Institute)

#### Collaborating organisations/universities

> - Please include their roles as part of the project, e.g. funder, collaborator, data supplier etc

- University of Leeds (Collaborator)
- University of Warwick (Collaborator)

### Additional content

> - If there is any additional content that should be included, or doesn’t fit in other fields, please add it here.
> - This could include links to images, videos, or figures (with plain English captions) that would be helpful in communicating the project)

Q: Add link to video of presentation to ASG health theme meeting?

## Tagging
### Programmes
> - If this project is part of a programme(s) please tick below:
 
- [ ] Artificial intelligence (Safety and ethics)
- [ ] Artificial intelligence (Robotics)
- [ ] Data science at scale
- [ ] Data science for science
- [ ] Data-centric engineering
- [ ] Defence and security
- [ ] Finance and economics
- [ ] Health
- [ ] Policy
- [x] Research Engineering
- [ ] Urban analytics

### ASG / SPF
> - Is this project funded by the Strategic Priorities Fund?
 
- [x] Yes
- [ ] No

### Research areas (required)

> - Please tick the research areas that are most applicable, up to max 10

#### Algorithms
- [ ] Complexity
- [ ] Compression
- [ ] Cryptography
- [ ] Data Structures
- [ ] Distributed

#### Numerical
- [ ] Applied Mathematics
- [ ] Dynamical Systems & Differential Equations
- [ ] Information Theory
- [ ] Mathematical Physics
- [ ] Multi-Agent Systems
- [ ] Numerical Analysis
- [ ] Operations Research

#### Artificial Intelligence
- [ ] Control Theory
- [ ] Evolution & Adaptation
- [ ] Game Theory
- [ ] Knowledge Representation
- [ ] Multi-agent Reasoning
- [ ] Neural Networks
- [ ] Neuroscience
- [ ] Nonlinear Dynamics
- [ ] Pattern Formation
- [ ] Robotics
- [ ] Symbolic systems
- [ ] Systems Theory

#### Computer Systems & Architecture
- [ ] Communications
- [ ] Computing Networks
- [ ] Databases
- [ ] Human Computer Interface
- [ ] Information Retrieval
- [ ] Neural & Evolutionary Computing
- [ ] Operating Systems
- [ ] Real Time Computing
- [ ] Parallel Computing
- [ ] Visualisation

#### Machine Learning
- [ ] Applications
- [ ] Computer Vision
- [x] Deep Learning
- [ ] Natural Language Processing
- [ ] Pattern Recognition
- [ ] Reinforcement Learning
- [ ] Semi-Supervised
- [ ] Speech Recognition
- [ ] Supervised
- [ ] Unsupervised


#### Mathematical Modelling
- [ ] Agent-based Modelling
- [ ] Automata & Algebraic
- [ ] Deterministic
- [ ] Dynamic/Static
- [ ] Graph Theory
- [ ] Ensemble
- [ ] Stochastic

#### Optimisation
- [ ] Convex Programming
- [ ] Nonlinear Programming
- [ ] Stochastic Optimisation

#### Privacy & Trust
- [ ] Cryptography
- [x] Differential Privacy
- [ ] Identity Management
- [ ] Verification

#### Programming Languages
- [ ] Hardware Optimisation (FPGA/GPU)
- [ ] Literate Programming
- [ ] Probabilistic Programming
- [ ] Software Framework Development
- [ ] Theory of Programming Languages
- [ ] Visualisation

#### Social Data Science
- [ ] Cognitive Sicence
- [ ] Data Science of Government & Politics
- [ ] Developmental psychology
- [ ] Ethics
- [ ] Linguistics
- [ ] Management Science
- [ ] Research Methods
- [ ] Social Media
- [ ] Social Networks
- [ ] Social Psychology

#### Statistical Methods & Theory
- [ ] Asymptotic
- [ ] Causality
- [ ] Estimation Theory
- [ ] High Dimensional Inference
- [ ] Information Theory
- [ ] Modelling
- [ ] Monte Carlo Methods
- [ ] Non-parametric & Semi-parametric Methods
- [ ] Probability
- [x] Simulation
- [ ] Spatial Analytics
- [ ] Time Series
- [x] Uncertainty Quantification

#### Theoretical Mathematics
- [ ] Algebra
- [ ] Calculus & Analysis
- [ ] Combinatorics
- [ ] Geometry & Topology
- [ ] Logic
- [ ] Number Theory
