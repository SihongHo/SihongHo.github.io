---
title: "Learn to use Notion"
layout: post
date: 2021-05-01 22:10
tag: Notion
image:
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "Learn how to use notion"
category: project
author: Sihong
externalLink: false
# <!-- https://www.notion.so/Getting-Started-ba9ba90d9838455a9829c38fdc5cd756 -->
---

# CSE 5830: Project Progression Report

**Sihong He, Bingjun Li**

## Project’s objectives

Our objective of the project has been stayed the same as when we started this project. We aim to find the relationship between gene and severity of COVID-19 patients using single-cell sequencing data via graph Markov neural network model.

## Activities your team have carried out

1. We did a more **extensive literature review** regarding proper model based on the kind of data we have and our problem setup. The final model we selected is the **graph Markov neural networks model (GMNN)**, which combines the **dependency among object labels** via conditional random field and **effective object representations** for classification through end-to-end training.
2. We had several **discussion sessions** that how to incorporate the GMNN model to our problem settings. The final procedure is to train a **graph auto-encoder (GAE) to extract the low-dimensional representation** from the genes and the corresponding gene regulation networks. Then use the **bottleneck layer** in the GAE as **node features** for each sample node in the GMNN model, patients' **severity of illness** as node label and the **connection graph** among sample node by their characteristics (age, gender, sample type, and pre-existing conditions).
3. We conducted several **test runs** with the GMNN model demo data.

## Tasks your team have completed and Contribution

1. **Data Management**: since the whole dataset is too large (almost 70GB), we build a pipeline to split the dataset to about 4,000 small data sets. (*Sihong He*)
2. **Data Cleaning**: for each sample, we construct its feature vector. (*Sihong He*)
3. **Converting** Original data from **Single cell to pseudo Bulk cell**.
    1. **Aggregation** of the all cells reading within each sample. (*Sihong He*)
    2. **Normalize** the resulted sample data to proper unit. (*Bingjun Li*)
4. **Data Exploration**: collected some data characteristics. (*Sihong He*)
5. **Preliminary Coding**: explore the GMNN (Graph Markov Neural Networks) codes.  (*Sihong He*)
6. **Data Format**: transfer original data to required format. (*Sihong He*)
7. **Reproducing GMNN**: reproduce GMNN on 3 standard dataset. (*Sihong He*, *Bingjun Li*)
8. **Modeling**: discuss how to apply GMNN model to our problem. (*Bingjun Li*, *Sihong He*)
9. **Determine and clean** the effective sample characteristics. (*Bingjun Li*)
10. **Construct the connection graph** among samples using their patients' characteristics. (*Bingjun Li*)
11. **Construct** the **gene interaction network** with database from BioGrid. (*Bingjun Li*)

## Preliminary results your team have obtained so far

1. Pseudo bulk-cell expression data for each sample for GAE.
2. Adjacency matrix for GAE.
3. Connection graph among samples for GMNN.

## Changes from the proposed work

We don't have changes from the proposed work.

## Unexpected challenges

- Data set is so large that we can not open it via the traditional method.
- The required data format is confusing that takes a lot time to read extra codes and papers.