# Abstract

This document describes use cases that demand crowdsourcing and volunteered geographic information. It underpins the collaborative work of the Non-Authoritative Data for Decisions (NAD) Ad Hoc group of the OGC.

# Status of this Document

This document is a draft of a discussion paper, to be used as input to the development of best practices for handling crowdsourcing and volunteered geographic information.

# 1. Introduction

The mission of the NAD Ad Hoc group is to clarify and to formalize best practices relating to crowdsourcing and volunteered geographic information. In particular:

to determine what metadata must be captured in order to make this data fit for decision making; and
to determine what interfaces, if any, would support the transmission of this data.

This document describes the results of the first steps of working towards these goals. Members of the group and other stakeholders have come up with a number of use cases that describe how crowdsourcing and volunteered geographic information could work. From these use cases, a number of requirements for further work are derived. In this document, use cases, requirements and their relationships are described. Requirements and use cases are also related to the deliverables of the group.

The requirements described in this document will be the basis for development of the other four deliverables of the group.

# 2. Deliverables

The following deliverables will constitute the output of this group.

##### 1. Use Cases and Requirements: 

A document setting out the range of problems that the group is trying to solve (this document).

##### 2. Best Practices: 

This will include:

1. advice on metadata that needs to be collected to support the use of crowdsourcing and volunteered geographic information for decision making;
2. advice on how to combine the data and its metadata to facilitate delivery;
3. advice on, or possibly definitions of, RESTful APIs used for receiving crowdsourcing and volunteered geographic information.

# 3. Methodology

In order to find out the requirements for the deliverables of the group, use cases will be collected. For the purpose of the group, a use case is a story that describes challenges with respect to crowdsourcing and volunteered geographic information for existing or envisaged information systems. It does not need to adhere to certain standardized format. Use cases are primarily used as a source of requirements, but a use case could be revisited near the time the work of the group will reach completion, to demonstrate that it is now possible to make the use case work.

The group will derive requirements from the collected use cases. A requirement is something that needs to be achieved by one or more deliverables and is phrased as a specification of functionality. Requirements can lead to one or more tests that can prove whether the requirement is met.

Care will be taken to only derive requirements that are considered to be in scope for the further work of the group. The scope of the group may be determined by a charter in future. To help keeping the requirements in scope, the following questions were applied:

Is the requirement specifically about crowdsourcing or volunteered geographic information?
Has a use case a description that can lead to a testable requirement?

# 4. Use Cases

## 4.1 Dataset Completeness Fulfilment

**Contributed by:** Joseph Abhayaratna

**Full Use Case Description:**

A data provider organisation maintains authoritative data and publishes its data on the web for data consumers, and wishes to be notified via an API if data consumers believe there are records missing from a dataset.

One of its data consumers builds a search interface over the data, and wishes to enable users of that search interface to notify the organisation when a search they believe should succeed doesn't because corresponding data does not exist in the dataset.

On failing a search of the dataset, a user of the search interface is presented with a form used for notification. They fill in the necessary information, and click notify which calls the data provider's crowdsourcing API.

**Related Deliverables:** Best Practices.

**Related Requirements:** 

# 5. Requirements

This chapter lists the requirements for the deliverables of the group, in alphabetical order.

## Capture Accuracy of the Geographic Position

To establish fitness for purpose of data, it is necessary for the supplier of the crowdsourced information to state the positional accuracy of the geographic information.

**Related Deliverables:** Best Practices.

**Related Use Cases:** Dataset Completeness Fulfilment.

## Capture Categorical Identity

To establish trust in the supplier of crowdsourcing or volunteered geographic information, it is necessary to be able to identify all records supplied by them. This requirement should be considered in conjunction with requirement Maintain Privacy.

**Related Deliverables:** Best Practices.

**Related Use Cases:** Dataset Completeness Fulfilment.

## Capture Currency Date and Time

To establish the currency of the data, it is necessary for the supplier of crowdsourced information to state the date and time that the data was captured.

**Related Deliverables:** Best Practices.

**Related Use Cases:** Dataset Completeness Fulfilment.

## Capture Purpose For Collection

To establish fitness for purpose of data that is part of an aggregated dataset, it is necessary for consumers of the aggregated dataset to be aware of the purpose for which each individual record was collected by the aggregator.

**Related Deliverables:** Best Practices.

**Related Use Cases:** Dataset Completeness Fulfilment.

## Capture Purpose For Collection By Supplier

To establish fitness for purpose of data that is part of an aggregated dataset, it is necessary for consumers of the aggregated dataset to be aware of the purpose for which the original data was collected by its supplier.

**Related Deliverables:** Best Practices.

**Related Use Cases:** Dataset Completeness Fulfilment.

## Enable Ratings by Data Consumers

To help establish trust in crowdsourced data that is part of an aggregated dataset, it is necessary for consumers of the aggregated dataset to assess its fitness for similar purposes, and for others to access that assessment to allow it to factor into their own decision to use or not use that data.

**Related Deliverables:** Best Practices.

**Related Use Cases:** .

## Establish Licence For Use

To enable aggregators and data consumers to trust they have the right to exploit records within an aggregated dataset, the license for attributable for all records.

**Related Deliverables:** Best Practices.

**Related Use Cases:** .

## Maintain Privacy

To enable suppliers of crowdsourcing and volunteered geographic information should have their personal identities protected to ensure their safety.

**Related Deliverables:** Best Practices.

**Related Use Cases:** Dataset Completeness Fulfilment.

# 6. Requirements by deliverable

For convenience, this chapter lists requirements grouped by deliverable

## 6.1 Best Practices

1. Capture Accuracy of the Geographic Position

2. Capture Categorical Identity

3. Capture Currency Date and Time

4. Capture Purpose For Collection

5. Capture Purpose For Collection By Supplier

6. Enable Ratings by Data Consumers

7. Establish Licence For Use

8. Maintain Privacy

# Acknowledgements

