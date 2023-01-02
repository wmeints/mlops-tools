# Concepts

In this section we cover concepts that we apply in the MLOps tooling collection.
You can view these concepts as basic truths, a value, or a guide for behavior. 
We want to realize these concepts with tools to get the most value out of our machine-learning projects.

## CI/CD automation

CI/CD automation provides continuous integration, and continuous deployment. We use this to implement automated pipelines that lint, 
test, and deploy code. It provides feedback about the quality of the code used in the solution.

## Workflow orchestrations

Workflow orchestrations coordinate pipelines of tasks as directed-acyclic graphs for processing data and training models. 
We use workflows to automate steps to train and evaluate models and to prepare datasets.

## Reproducability

Reproducability is the ability to execute a workflow for the second time with the same configuration, code, and data and get the same results.
There are a number of reasons why we value reproducability:

1. It makes the product more trustworthy, because we know we can get the same results multiple times.
2. There are new regulations coming up that require traceable results. 
3. It increases quality of our work, we can more easily reproduce errors and fix them.

## Versioning of data, code, and models

Versioning ensures that each version of a model, dataset, and piece of code can be identified and restored at any time.
We like to track versions of data, code, and models together because it provides several benefits:

1. We can trace errors back from a user interaction to the model, to the code, and the data.
2. We can provide regulatory agencies with an audit trail of what was used to make a decision with our models.
3. We can restore the an environment to a specific version as needed.

## Collaboration

Machine-learning projects are never done by one person. We want to enable various disciplines
to easily work together towards an end result. This means that it must be easy for a non-technical person
to submit data for analysis and view evaluation results. But it must also be easy for a technical person
to work with the same data and generate results that can be viewed by everyone.

## Continuous training and evaluation

As machine-learning models age they drift from reality as we gather new data in production.
Continous training is the process of periodically retraining the model with updated/improved data
to ensure that the model doesn't drift too far from reality.

## Metadata tracking

As we process data and train models we need to gather metadata so we can use it later to gain insight
into what happened while we were building the model. We need several groups of metadata for this purpose:

- Training metadata: Hyper parameters, dataset version, and code version.
- Resource usage metadata: CPU, TPU, disk, and memory usage.
- Performance metadata: time it takes to run tasks and pipelines.
- Lineage metadata: How was the data obtained and processed.
- Feature metadata: Description of the data that we used for the model.
- Model metadata: Description of the model, how it should be used, limitations, etc.

## Monitoring

When building a model, we collect various pieces of metadata. It doesn't stop in our development environment.
In production we also gather metadata, but with a different goal: to gain insight into runtime behavior of the model.
We gather the following groups of metadata:

- Runtime performance: inferencing speed.
- Resource usage: CPU TPU, disk, and memory usage.
- Model performance and model drift.

## Feedback loops

We need several feedback loops to learn from the behavior of our model and users of the model.
We've found that the following feedbacks are useful for us:

- Code and build quality feedback: Information from CI/CD provides us insight in how safe, maintainable, and correct our code is.
- Training and model evaluation feedback: Information from workflow executions provide us insight in training behavior.
- Monitoring feedback: Information from the monitoring system provides insight in technical behavior in production.
- User feedback: Information from user feedback provides us insight in trust, safety, and usability.
