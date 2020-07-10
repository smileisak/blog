---
title: "Kopf (Kubernetes Operator Pythonic Framework) UseCase"
date: 2020-07-09T14:33:34+02:00
author:
  name: Ismail KABOUBI
  image: /assets/images/avatar.png
hero: /assets/images/discoveries/kopf/k8s-python.jpg
categories: 
- kopf
- discoveries
draft: true
weight: 2
---

## Introduction

During my last experience while helping one of my clients to its journey to cloud, I've worked on deploying a multi-tenant Kubernetes clusters to host more than 200 application. We've chosen to go with GKE a managed Kubernetes upon Google Cloud Platform.

The cluster has been created using [Terraform]() scripts. In this article I'll focus only on what happened once we have the cluster provisioned.

For each application that will be hosted in the cluster, we need to create:

* Inside the Kubernetes cluster:
  * One or multiple namespaces.
  * Resource Quotas.
  * Network Policies.
  * RBAC resources.
  * Secrets (for Google Service Account Keys, Docker Trust Registry access, ...)
  * ...

* Provision Docker Trust Registry Org, Repo, Team, and User.

As SRE, one of the main principles is to [eliminate Toil](https://landing.google.com/sre/sre-book/chapters/eliminating-toil/).

> If a human operator needs to touch your system during normal operations, you have a bug. The definition of normal changes as your systems grow. (Carla Geisser, Google SRE)

So, I've decided to automate the actions needed to "provision" an application environment within a multi-tenant Kubernetes cluster.

First I listed the possible solutions to satisfy this need:

1. Use a Shell script within a Gitlab Runner that takes application needs as input and run to create the environment.
1. Script a Python solution (since I'm comfortable with this language) to perform those actions.
1. Use Terraform to automate those actions.

The problem of the 2 first solutions is that the state is not guaranteed, which means that if someone use this script there is no way to figure out with which input the script have been launched.

Regarding the terraform solution, at that time the [Kubernetes Provider](https://www.terraform.io/docs/providers/kubernetes/index.html) does not support the entire Kubernetes resources.

## Declarative Approach VS Imperative Approach

Comming soon

