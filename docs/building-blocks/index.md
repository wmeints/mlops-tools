# Building blocks

This section maps concepts to building blocks. For each building block we provide a description of the functionalities
provided by the component and information on where to learn more about the component.

The building blocks in this section are based on the scope diagram that we've shown in the README of the repository.

![Scope of the building blocks](https://user-images.githubusercontent.com/1550763/210208513-c4fe4237-bf17-4fe1-adf4-9779c78670c1.png)

## Source control

As mentioned in the [Concepts](./concepts.md) section, we don't deploy source control as part of the MLOps tools.
We support using any kind of GIT implementation. Here are a few examples:

- [Github](https://github.com)
- [Azure DevOps](https://dev.azure.com)
- [Gitlab](https://about.gitlab.com/)

## CI/CD tool

CI/CD tooling is also out of scope for the MLOps tooling. All building blocks have a commandline interface 
or provide other ways to be controlled from the CI/CD tooling. The source control tools described in the previous
section all provide excellent CI/CD capabilities.

## Workflow orchestration

We use [Prefect][1] for workflow orchestration. It provides the following features:

- Scheduling of workflows
- Automatic retries of failing workflow tasks
- Logging of workflow steps
- Notifications of succeeded or failed workflows
- Observability of workflow execution

## Model training infrastructure

We train various types of models:

- Deep learning models using [Pytorch][2] and [Pytorch lightning][6]
- Machine learning models using [Scikit-learn][3]
- Explainable and interpretable models using [InterpretML][4]

To train these models, we use [Ray][5]. Ray Provides an important piece of
infrastructure to scale training models beyond a single node.

Ray also provides infrastructure to tune the hyperparameters of models
using [Ray Tune][7].

## Feature stores

## Model registry

## Monitoring components

## Metadata stores

## Model serving

[1]: https://docs.prefect.io/
[2]: https://pytorch.org/
[3]: https://scikit-learn.org/
[4]: https://interpret.ml/
[5]: https://docs.ray.io/
[6]: https://www.pytorchlightning.ai/
[7]: https://docs.ray.io/en/latest/tune/index.html