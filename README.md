# MLOps tools

This repository contains code and descriptions of various MLOps tools that we regularly use at Aigency. 
Feel free to copy files from this repository to build your own environment.

## Introduction

After using Azure ML for a long time we've come to the conclusion at Aigency that there are better ways to build a machine-learning project environment.
We've run into quite a few limitations and issues with the tooling that Microsoft currently provides. This is why we gathered our own collection of tools.

### Goals

At Aigency we try to achieve a number of goals, which we've split up in two groups. First, we have the following functional goals:

1. Store, version, and describe datasets used in our projects
2. Store, version, describe, and deploy models used in our projects
3. Manage and execute pipelines used to process data and train models

We also have a number of quality goals:

1. Great developer experience, you should be able to debug and test locally before deploying pipelines
2. Easy to set up and easy to maintain, we want to focus on business value not operations
3. Safe, our customers expect a safe environment, and we should be able to provide that
4. Just enough tooling. We need a flexible environment that's cost-effective.

### Constraints

Please be aware that while your tool may look awesome, we may not adopt it in the collection here.
We operate according to these constraints:

1. Use before build and avoid buy. We value openness, and community interaction.
2. Python-only, we know there are many other options, but this is what we use at Aigency.
3. Tools must integrate with commonly used GIT implementations and commonly used CI/CD tools.

### Scope

The scope of the tools in this repository is based on the concepts described in [Machine Learning Operations (MLOps): overview, definition, and architecture][1].
We've converted the concepts into the following scope definition:

![Scope of the tools](https://user-images.githubusercontent.com/1550763/210202639-873fc1fe-e154-4b30-8433-d5247f78aad0.png)

Since we're following the principle that the MLOps tools must reasonably integrate with the most common CI/CD tools and GIT implementations, we're going to
assume that you have a CI/CD tool and a GIT repo to store the source code for your ML solutions.

Another important thing to note: We included feature stores as a component, but we don't include things like S3 storage or Azure Blob Storage.
You'll have to provide an actual storage mechanism yourself.

## Getting started

As we mentioned at the beginning of this README. This is a collection of tools, so there's no single manual to deploy all the tools.
We've recorded documentation to explain how things work and how they fit together. Please check the individual sections in the 
docs to pick a tool and deploy it.

## Documentation

1. [Concepts](./docs/concepts.md)
3. [Building blocks](./docs/building-blocks/index.md)
4. [Runtime scenarios](./docs/runtime-scenarios/index.md)
5. [Crosscutting concerns](./docs/crosscutting-concepts.md)

[1]: https://arxiv.org/abs/2205.02302
