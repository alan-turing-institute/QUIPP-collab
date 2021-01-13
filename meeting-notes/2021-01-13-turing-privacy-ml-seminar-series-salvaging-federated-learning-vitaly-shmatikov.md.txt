
# Salvaging Federated Learning
Vitaly Shmatikov
13 January 2021

## Introduction
- Federated learning has significant issues
- Became a thing when presented by Google at an event in 2019
- Avoid centrally collecting data
  - Illegal with some data
  - Some data too sensitive (e.g. message contents)
- Do learning on the end user device (e.g. mobile phones)

## Why do federated learning?
- Altrusim
- Federated learning gives better results than users doing local independent learning

## Who?
- Non-IID: every user has different data
- Unbalanced: some users have more data
- Massively distributed: millions of users
- Limited communications: user devices frequently offline or slow connections
- Privacy: train model without looking at users private data. Key consideration driving developments in federated learning.

## How?

- In each iteration central serve / aggregator distributes current federated model to participating federated nodes.
- Each local node trains a batch and send model updates to central server
- Central server aggregates local updates
- Over many batches, users' data is gradually incorporated into combined federated model.

## Data leakage issues
- Naive federated learning leaks information about users' data, even if only model weights / parameters are exchanges, especially for models with large numbers of parameters.
- e.g. gradients in deep learning models can leak information about training data.
- Model updates can allow successful membership inference or derivation of sensitive properties of the data that are not necessarily related to the learning objective (e.g. presence of people in dataset at time points, gender, race, authorship of text)
- Use clever techniques to provably prevent aggregator to inspect individual models (secure aggregation techniques)
- Improves privacy, but significantly reduces utility

## Backdoors / Model poisoning issues
- No protections for users deliberately crafting data to train model to misbehave maliciously for certain inputs.
- As local nodes directly submit model updates, poisoning is easier to do more directly than crafting malicious training data.
- As federated learning is expects non-IID and unbalanced datasets, it's hard to say what an "odd" update looks like (tail users look anomalous).
- Secure aggregation prevents direct inspection of updates to do anomaly detection.
- Robust aggregation discards contributions of tail users, but risks biasing model and making is less useful for users in the tails.

## Differential privacy
- Has effect of discarding tail users as it is designed to be insensitive to inclusion or exclusion of particular users.
- Challenging to deploy in real-world use cases.
- Hard to determine meaningful epsilon (privacy parameter) for particular use cases.
- Loses accuracy, especially for tail users.
- Exacerbates unfairness, especially for tail users
- Suppresses novel data as it is different

## Why would a user participate in FL?
- All privacy and integrity protection measures in federated learning suppress accuracy for tail users.
- Addition of such controls makes federated learning **less** accurate for many users than a purely locally trained model (i.e. each user only using their own data).
- Example analysis of Reddit posts:
  - Vanilla aggregation: FL is worse than local training for 9% of users
  - DP aggregation: FL is worse than local training for 21% of users
  - Robust median aggregation: FL is worse than local training for 52% of users
- Users who do better locally:
  - Have lots of data 
  - Have atypical data
- It's commonly said you can only pick 2 of 3 of Privacy, Accuracy Robustness. Vitaly suggests it's really 1 of 3 for tail users.

## Local adaptation
- Start with the federated model, which may possibly / likely be inaccurate for the local user
- Train many versions of this further using local data to adapt the model to local user while still leverage the data from other participants available via the federated model.
- Techniques:
  - Fine-tuning: Adapt global parameters for new local data
  - Multi-task learning: train model to support two tasks. Risks "forgetting" federated learning.
  - Knowledge distillation: teach local model to perform similarly to global model (effectively transfer learning).
- For all three above techniques, individual locally adapted models give improved accuracy for all users vs only a privacy preserving federated model and for many more users (even tail users) also better accuracy than local only learning. Biggest improvement for tail users.

## Takeaways
- Conjecture: The influence of outliers must be bounded to achieve privacy and robustness. This will result in models that are inaccurate for tail users. A bold claim, not a theory.
- Conjecture: Cannot balance privacy, robustness and accuracy in a single federate model.
- If the above is true then a solution is lots of models rather than a single model.
- Locally adapted individual models seem to work well. Several promising techniques.
- Preprint at https://arxiv.org/abs/2002.04758. A little stale (last update Feb 2020).



