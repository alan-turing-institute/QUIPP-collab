# HDR UK Synthetic Data Generation Interest Group
Neil Sebire and Aiden Doherty

## Goals at start of workshop
- To understand what is going on in the health data landscape using synthetic healthcare data.
- HDR UK want to understand who they can bring together and what they can do to advance work in this space.

## Summary at end of wrokshop
- Potential roles for HDRUK:
    - Collate and share what people have done in terms of information governance approaches
    - Collate and share decisions on why certain techniques chosen
    - Making synthetic datasets findable and available (e.g. via Gateway)
    - Measures for how "good" a synthetic dataset it (utility)
- Ideas for what to cover in future and are there any grand challenges in this space that HDRUK could / should focus on?
- Please make HDR UK aware of other work goign on in this space. Keen for as much diversity of collaboration and input as possible.

## Talk 1: A data custodian's view of synthetic healthcare datasets
Dr Puja Myles, Head of Observational Research, CPRD
CPRD have released a synthetic version of CPRD data

### CPRD: Clinical Practice Research Datalink
MIHR/NIHR centre. UK government health data research service.
60 million patrients for observational studies

### CPRD synthetic dataset
- Funding from Innovate UK for proof of concept project to develop high fidelity dataset to capture the complex relationships in data and can be used to validate ML algorithms.
- Key driver: to support regulation of ML algorithms used in healthcare (not primarily a data sensitivity concern).
- Addition of privacy workstream following first project steering group (raised by public representative). Initially naiively thought synthetic naturally meant private.
- Sought advice from ICO innovation hub.
- CPRD can link primary and secondary health datasets.
- Concluded in March 2020

#### Key outputs
    - A validated methodology for generating and evaluating high fidelity synthetic datasets.
    - Experimentally demonstrated these could be used to train and validate ML algorithms.
    - Ran some experiments to see if clinicians could distinguish the datasets.
    - Released initial heart health dataset.
    - Funded by NHSX to release Covid-19 dataset.

#### Approach
    - Bayesian network anlysis used to discover relationships between fields in real anonymised ground truth patient data.
    - Learned relationships used to generate 100% artificial synthetic data.

#### Privacy controls
    - Privacy checks incorporated into evaluation framework.
    - Check for and remove any sythnetic patients that exactly duplicate patients in the ground truth data.
    - Detection and comparison of outliers between synthetic and ground truth data.
    - Undertook a motivated intruder simulation where one person in research team not involved in data generation was given synthetic data and part of ground truth data to see if they could match records (given 2 weeks).
    - Risk assessment undertaken by CPRD information governance specialist.
    - Current risk assessment suggests no need to remove outliers in current synthetic datasets, but will need revisiting for every synthetic dataset generated.
    - In light of ICO innovation hub guidance, access controls introduced for synthetic datasets.
    - Researchers requesting synthetic data cannot access ground truth data.

#### Should you use synthetic data instead of real data?
- Anonymised real data which can be accessed with appropriate safeguards in place is preferred option.
- Low-medium fidelity synthetic data could be used as sample datasets to illustrate structure and for training in data management
- High-fidelity synthetic data generation is resource intensive to generate (i.e. it's not cheaper than real data)
- Valuable in some use cases:
    - Scale up data when larger sample sizes are needed
    - Conditional generation of data fields to address imbalances and minimise bias
    - Generate synthetic patient cohorts to support in silico trials to simulate effects in sub groups not typically included in RCTs (e.g. pregnant and elderly)
    External control groups for clinical testing or benchmarking data from signle-arm trial
- They are looking at whether they can use a generating a larger synthetic dataset from a model trained on a small real dataset to more closely match the distribution fo a larger sample of the real CPRD dataset.

## Talk 2: How technically close are we to a vision for synthetic healthcare datasets
Mihaela van der Schaar, University of Cambridge

Mihaela's focus is on gnerating synthetic data that will help clinical colleagues take advantage of ML, so access to real data is very helpful.

There is a lack of access to high-quality data in healthcare and other domains, due to very reasonable privacy concerns.

### Privacy challenge

- No universally accepted and quanitfiable definition of privacy exists. In ML, differential privacy is a common definition, but has limitations.
- Data guardians, not data users set terms of access, and set their own requirements.
- Regulatory efforts (e.g. GDPR, HIPAA) do not provide clear definitions, safeguards or reassurance.

### Fidelity challenge
- How should quality of synthetic data be evaluated?
- What factors determine utility of synthetic data for a specific purpose
- No single definition
- Compare joint distribution,not just single-dimensional distributions
- Do differnet uses come with different utility measures?
- Time series a particular challenge. Hard to capture correlations consistently across time. Easier to breach privacy in time-series data as only one concurrent pair of events may be sufficient to identify an instance, especially if it can be mapped to external knowledge (e.g. arrival time of person A at hospital).

### Desiderata
- We need a range of concepts for data privacy and fidelity

### ADS-GAN
- Developed to generate symthetic data meeting GDPR privacy requirements
- Unlike standard conditional GANs (pre-defined variable set), ADS-GAN optimises a different conditioning set for each patient.
- Formalise GDPR requirements as an Identifiability metric.
    - Probibility that the distance to the closest synthetic observation is closer than the distance from the closest real observation (epsilon-identifiability).
- Move away from differential privacy (very good but very strong) and define privacy in a different way.
- Adversarial training to maximise fidelity while satisfying epsilon-prrivacy constraint. [Q: Does this risk creating structure in the synthetic data that leaks info about real data - e.g. "shells" of synthetic data points at a radius of epsilon from the real data used to train the generator]

### Time-GAN
- Add stepwise supervised loss using original data as supervision.
- Takes advantage of the fact that there is more info in the training data than whether it can be distinguished from synthetic data.
- Introduced embedding network to provide a reversible mapping between features and latent representations to reduce high-dimensionality of the adversarial learning space.

### Hide-and-seek privacy challenge
- Challenge is part of NeurIPS, with support from Amsterdam UMC (provided high-quality real time-series patient data - richer but similar to MIMIC) and Microsoft Research Cambridge.
- Would liek to create a clearing house for generating synthetic data.
- Running "inspiration exchange" commumnity engagement sessions (mainly for young researchers interested in ML for healthcare).  Next one is on synthetic data. Jan 26th.

## Talk 3: Synthetic Health Data - Real World Challenges
Jonny Pearson, Lead Data Scientist, Analytics Unit - Innovation @ NHSX. jonathan.pearson@nhsx.nhs.uk

- Use synAE, synthetic A&E dataset created in 2018/19 by NHS England to identify real world issues and considerations when attempting to create and share synthetic health data and think through current sythetic data use cases in NHS. Goal to make openly shareable dataset.

### SynAE
- Linked A&E and admitted activity data through Secondary Uses Service (SUS), which colelcts and provides record level pseudonymised data from providers. Augmented with IMD and distance data.
- Original method: Foggy data erosion - a sampling with replacement approach to generate hierarchical conditional probabilities. Learning: Event hough each record made synthetic, sunset of features made probability of 
- New method: Bayesian network approach: R package called BNLearn. Learning: Much more private but at cost of quality.

### Considerations: Privacy, Utility and Quality
- Privacy: set for various user groups. Always need a privacy assessment for public users
- Utility: what is data used for. What is needed for this? Recommend fixed use case. Generic use cases v.hard to get pas information governance. Minimal data extract to satisfy the purpose.
- Quality: No utility and privacy defined, look at what methods give highest quality? E.g. realism of values, inability to distinguish between synthetic and real datasets? Consider Voas-Williamson statistic for variance comparison or Propoensity scores? What is lowest acceptable quality? Highest achieveable quality? Pick method that gives best quality.

### SynthAE lessons
- Work in open. Build methodology with dummy data that you generate synthetic data from to allow wide discussion, inviting wide range of critics, communicating with IG and users.
- Consider reidentification risk, including considering future advances. Didn't use differential privacy, but would recommend. Consider how an unravelled model could identify individual cases. Key is understanding manifold/latent space of real data, especially around less dense areas or outliers, which risk overfitting in sparse areas.
- Demonstrate appropriate use of data. Can we clearly show data subject rights are not being violated?
- Actors and threats: Sketch data ecosystem to identify different actors along data flow and potential threats.
   - False insights: People using data inappropriately
   - Anonymisation process: Reidentification risk too high.
   - Fear: Insufficient confidence isn the process of tech could mean data is never released due to daily mail fear.
- Good communications with IG, users etc.

### User needs
- Data analysts: training and sharing of models
- Academic: Development of methods before applyign to real data
- Demonstration: Visualisation of key relationships / principles
- PoC/MVP development: Develope app / infrastructure on realistically structured data before expensive / complex data access.
- Modeller: When looking at impact of change / imtervention may not need real data.
- Realistic test data: For e.g. pipeline development
- Generic synthetic data hard: Many tools use case specific. Generic datasets can reduce fidelity.
- Alternatives: Importing models into secure environments or federated learning.

### Next steps
NHSX having a series of cross-governemnt discussions about knowledge gaps and missing links in synthetic health data. Will progress to either procurement of solutions and research or develop via PhD internship programme.

- Open enablers: Any work providing guidance and tools to standardise synthetic data generation for turnign systems understanding into models.
- Longitudinal methodologies: Time dependent transactional data to facilitate patient pathway development.
- Synthetic Dicom and Text data:  Imaging and test data often more sensitive.
- Interested in filling gaps and there is funding available. happy to get the boring work doen to link up / enable more exciting work.
- Lots of interest in synthetic data in NHS data architect community. Very different uses than in the academic papers. Use e.g. agent based models and need to know about the history / provenance of the data.

## Talk 4:
Peter Charlton, Biomedical Engineer at Univerisity of Cambridge and City University, London. Working on using data from wearables with focus on hearth data.

- Heart rate monitored by Photoplethysmogram (PPG) sensor, where blood flow attenuates light signal, modulated by blood pulsations.
- Developed a synthetic PPG pulse wave database


## Talk 5: Health Data Insight - Simulacrum
Lora Frayling, Data Scientist

### HDI data access
- Collected by National Cancer REgistration Analysis Service (8NCRAS)
    - Cancer Outcomes and Services Dataset (COSD)
    - Systemic AniCancer Therapy Dataset (SACT)
- Datasets stored within Cancer Analaysis System (CAS), managed by PHE
- HDI can access both datasets

### Synthetic data: The Simulacrum
- Syncthetic version of patient and tunor data in COSD
- 1.4M patients, 7 tables
- Publicly released on HDI website

### Synthesis methods
- Use case: patient cohort identification and analysis
- Aims: Preserve characteristics relevant for use case
    - Capture strong correlations
    - Realistic ordering of tunor and treatment events
    - Same structure as real data
    - Enable privacy evaluation according to PHE data release guidelines
- Raw data -> Correlation analysis of variable pairs -> probailistic graph -> data generation
- Data validated before release
- Pairs with correlations above a predetermined threshold included in graph. Direction of links set from highest degree nodes to lower degree nodes (not a causality graph).
- Synthetic data generated column by column by randomly sampling based on conditional probabilities in graph.
- Where unique rows exist, merge across cancer type
- PHE data release follows ISB1523: Anonymisation Standard for Publishing Health and Social Care Data. Simulacrum satisfies this as they don't sample from small populations. Standard often uses k-anonymity.
- Work with IQVIA (lifesciences data science consultancy, pharma clients)
- IQVIA explore synthetic data and develop code for use cases for external clients. Then pass code to PHE, who run on real data. Make release of results after applyong statistical disclosure control. Partnership increases impact while letting HDI focus on synthetic data generation.
- Also provide Simulacrum downloads from website (300 registered downloads wince 2018)
- Number of releases of synthetic data based on same patients needs to be planned with care to protect patient privacy.
- Want to support seuqntial events (looking at simple Markov models to more realistic models)
- Transparent and understandable models key to confident release
- HDI are open to research collaboration
- HDI to summer internships to foster young talent


## Talk 6: How can we ensure patient privacy
Allan Tucker, Head of Intelligent Data Analytics Group, Department of Computer Science, Brunel University

- Practical lessons from generating synthetic healthcare data
- care.data was a failure
- Real diffculty with making gold standard ground truth data freely available to research organisations like universities

### Data Privacy concepts
- K-anonymisation: removing or generalising data
    - But what is acceptanle K
    - Not good on high dimensions
- Differential privacy: rmeoving an individual has no effect on analysis
  - Repeated requests for aggregate data can enable identification of individuals
  - Impact of rare cases (elderly, rare disease, personalised medicine)

### Generative Adversarial Networks (GANs)
- Large interest in GANs
- Deep learning approach to learn precise distributions and relationships in a dataset
- Nervous about inferring a model from data without high transparency. Deep learning methods are not transparent. Also had experts in the data available.
- Black box models risky in terms of introducing unknown biases and in encoding biases from e.g. data collection (most research is a secondary use of data collected for other purposes) and societal biases.
- Hard to confirm model captures expected dependencies and captures known relationships (and no unexpected relationships) woth black box models. Easier to inspect in graphical models, includin gidentifying spurious relationships that we think  are due to bias or model artefact.

### Probabilistic Graphical Networks
- Flexible conditional data generation
- Can query model for impact on subset of characteristics or different scenarios.
- Dynamic / state-based networks for time-series (including hideen markov models)
- Inferred from CPRD subset of cardiovascular risk fields and relationships
- Don't always capture same richness of relationships / distributions as deep learnign methods, but can address in part with inclusion of latent variables in graphical models.

### Fidelity tests
- Correlations between variables
- Univariate distributions 
- Joint distributions (2nd and 3rd order)
- Compared predictive performance of ML models trained with synthetic and ground truth data (e.g. ROC curves and Precision-Recall plots for classifiers)

### Privacy tests
- Explore effect of ground truth sample size and number of varables on clones (identical data points) and outliers vs inliers
- Repeated resampling from synthetic models
- Risk of clones decreases with ground truth size
- Risk of outliers decreses, but always small
- Number of outliers stable around 10-70
- Simulated attack to match to real patients
    - Gave partial fields from real dataset
    - Check whether real record can be matche dto very similar records in synthetic dataset based on these attributes
    - On rare occasion links were made, the remaining unshared fields of the true record were not sufficiently similar to count as a match.
- Development fo privacy metrics still a field in its infancy

### Datasets
- Cardiovascular dataset
- Covid-19 dataset
- Extended generation into time-seris for MIMIC-like dataset
