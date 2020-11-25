# 2020-02-06 Whittaker Lab meeting
- **Author: @LouiseABowler**
- **Ed Palmer - CC-HIC dataset (UCL)**

My notes from the meeting:

- Ed is involved in the collection of a large dataset from patients in intensive care
  - Camila: This is the same one that we're applying for access to
  - 250,000,000 data points
  - Data held in the UCL safe haven
- Statistical disclosure control
  - This approach is used for less sensitive, aggregated data
  - Types of columns:
    - Direct identifiers, e.g. name
    - Key variables (not unique, but could be a key in combination), e.g. age and time of admission
    - Sensitive variables e.g. HIV status
    - Non-sensitive e.g. heart rate
  - Typical approach is to remove directly identifying variables, and to "soften" keys (k-anonymity)
  - See also L-diversity for measure of how identifiable the data could be
  - However, so much public data is available that key variable paradigm aren't necessarily valid
- Samples of this data (I think 1/1000) are released
  - Some context is lost
  - Lose linkages between records, so no readmissions data etc.
- Types of synth
  - Things we've looked into: MICE, GANs etc.
  - Augmented synthesis: synthesise only the identifying variables
- Ed's SSI Fellowship:
  - Hold a "synth-a-thon" to bring together people who hold data, people who want synthetic data and people who have ideas about the synthesis process
  - Create new data resources
  - Set community standards
  - Synthesise and share more data (links to the Turing Way)

From follow-up discussion:
- A "refresh" of the UCL safe haven is happening at the moment. Ed would like to get involved in a trial of the new system; there's potential for us to link in there.
- Release of synthetic data models and potential for combining synthetic datasets derived from the same original dataset are hard problems for privacy.
- Data generator - is it safe to release?

And some more notes from others (mainly Kirstie!) in the lab's HackMD document:
* Definition of intensive care: keeping the organs alive while the body heals itself
  * iron lung --> manual ventilator (medical students) --> automated monitoring
  * Lots of data!
* > The NIHR Health Informatics Collaborative (HIC) brings together all NHS trusts with NIHR Biomedical Research Centres (BRCs) and their partner trust to make NHS clinical data more readily available to NHS trusts, researchers, industry and the wider NHS community.
  * from https://hic.nihr.ac.uk
  * doi: [10.1016/j.ijmedinf.2018.01.006](https://doi.org/10.1016/j.ijmedinf.2018.01.006)
* Can't release data and so therefore:
  * can't verify work that has been published
  * barrier of reusing the data for new analyses and greater innovation
* The big secret: anonymisation relies on subjective assessments
  * What is a key variable (erm....everything)
  * What is sensitive (one person's signal is another person's noise)
* Questions:
  * When you say "community standards" what do you mean by that?
    * A: Who gets to answer the question about "what is sensitive"? So community standards is trying to build consensus across a broad coalition of medical professionals and experts in privacy preserving analyses.
  * Could you have a fine grained consent?
    * A: It would be a bit tough... intensive care is exempt from legal requirements for consent as the patients are so unwell when that data is collected. Might be easier in other areas within the medical community. 
  * Are there GDPR restrictions?
    * A: Not really - it affected documentation, but not really the actions that are taken around the data.
