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

<details><summary><b>Full Use Case Description (Click to expand/collapse)</b></summary>
<p>

A data provider organisation maintains authoritative data and publishes its data on the web for data consumers, and wishes to be notified via an API if data consumers believe there are records missing from a dataset.

One of its data consumers builds a search interface over the data, and wishes to enable users of that search interface to notify the organisation when a search they believe should succeed doesn't because corresponding data does not exist in the dataset.

On failing a search of the dataset, a user of the search interface is presented with a form used for notification. They fill in the necessary information and accept the terms of notification which states the data provider's purpose for collection and provides the data provider with a license to exploit the notification as per their conditions of use. Once happy, the search interface user clicks notify which calls the data provider's crowdsourcing API.
</p>
</details><br/>

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Requirements:** [Capture Categorical Identity](#capture-categorical-identity), [Capture Purpose For Collection](#capture-purpose-for-collection), [Establish License For Use](#establish-licence-for-use)

## 4.2 City Asset Management

**Contibuted by:** Joseph Abhayaratna, shared with [Smart Cities DWG Use Case 5](https://external.opengeospatial.org/twiki_public/SmartCitiesDWG/SmartCityUC5)

<details><summary><b>Full Use Case Description (Click to expand/collapse)</b></summary>
<p>
Leslie uses her favourite City App to search for the restaurant she agreed to meet her friend at. She drives with the City App open on her smartphone to take advantage of its traffic and incident alerting. On her way, she sees a pothole. She marks the pothole’s position using a button on the City App’s navigation screen that drops a pin and the time the feature was identified. When she stops her car, she uses the City App to fill in the remaining details regarding the pothole and submits a road incident report.

Tom, another driver, is also using the City App to take advantage of the its alerting features. He specifies in the City App that he is traveling to work. The City App notifies him that the shortest route has a damaged road surface, and asks whether he wishes to choose another route. Tom elects to take the shortest route. As he approaches the pothole that Leslie previously notified, Tom is asked for confirmation of the damaged road surface. He confirms it. Each user's identity is not revealed.

Stephen, a controller for road maintenance, is looking at the Common Operating Picture road maintenance view. He sees Leslie’s verified notification pop up on the map. The road is marked as high priority based on its historical throughput. As more and more verifications come through, the incident’s priority is increased and a road crew is dispatched at a time when the road is known to be under-utilized based on historical usage statistics. When the crew reaches the pothole, the status of the pothole incident is marked as “Work commenced”, and the City App sends notifications to approaching traffic to help them find an alternate route and allow the road crew to complete the job quickly. Once the road work is complete, the crew updates the status of the pothole, and road users are once again routed down the road.
</p>
</details><br/>

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Requirements:** [Capture Categorical Identity](#capture-categorical-identity), [Capture Currency Data and Time](#capture-currency-date-and-time), [Enable Ratings By Data Consumers](#enable-ratings-by-data-consumers), [Maintain Privacy](#maintain-privacy)

## 4.3 Utilizing Provenance

**Contibuted by:** Ivana Ivánová

**Extends:** [City Asset Management](#42-city-asset-management)

<details><summary><b>Full Use Case Description (Click to expand/collapse)</b></summary>
<p>
Over time, historical incidents are used to predict road maintenance needs so that roads can be preemptively maintained as required. However, this requires a reasonable amount ot trust to support related decision manking. The City App captures provenance information such as the device used to capture the GPS signal and its related accuracy, any other details about how the data was submitted that might affect its accuracy (e.g., speed Leslie was travelling when she dropped the pin). This information is then used by Stephen and the other road maintenance controllers, along with the number of corresponding notifications, to determine the trust applied to each notifier.
</p>
</details><br/>

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Requirements:** [Capture Creation Process](#capture-creation-process), [Capture Accuracy of Geographic Position](#capture-accuracy-of-the-geographic-position), [Machine Readable Provenance](#machine-readable-provenance)

# 5. Requirements

This chapter lists the requirements for the deliverables of the group, in alphabetical order.

## Capture Accuracy of the Geographic Position

To establish fitness for purpose of data, it is necessary for the supplier of the crowdsourced information to state the positional accuracy of the geographic information.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [Utilizing Provenance](#43-utilizing-provenance)

## Capture Categorical Identity

To establish trust in the supplier of crowdsourcing or volunteered geographic information, it is necessary to be able to identify all records supplied by them. This requirement should be considered in conjunction with requirement Maintain Privacy.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [Dataset Completeness Fulfilment](#41-dataset-completeness-fulfilment), [City Asset Management](#42-city-asset-management)

## Capture Currency Date and Time

To establish the currency of the data, it is necessary for the supplier of crowdsourced information to state the date and time that the data was captured.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [City Asset Management](#42-city-asset-management)

## Capture Purpose For Collection

To establish fitness for purpose of data that is part of an aggregated dataset, it is necessary for consumers of the aggregated dataset to be aware of the purpose for which each individual record was collected by the aggregator.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [Dataset Completeness Fulfilment](#41-dataset-completeness-fulfilment)

## Capture Purpose For Collection By Supplier

To establish fitness for purpose of data that is part of an aggregated dataset, it is necessary for consumers of the aggregated dataset to be aware of the purpose for which the original data was collected by its supplier.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** 

## Enable Ratings By Data Consumers

To help establish trust in crowdsourced data that is part of an aggregated dataset, it is necessary for consumers of the aggregated dataset to assess its fitness for similar purposes, and for others to access that assessment to allow it to factor into their own decision to use or not use that data.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [City Asset Management](#42-city-asset-management)

## Establish Licence For Use

To enable aggregators and data consumers to trust they have the right to exploit records within an aggregated dataset, the license for attributable for all records.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [Dataset Completeness Fulfilment](#41-dataset-completeness-fulfilment)

## Maintain Privacy

To enable suppliers of crowdsourcing and volunteered geographic information should have their personal identities protected to ensure their safety.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [City Asset Management](#42-city-asset-management)

## Machine Readable Provenance

To facilitate automated quality evaluation, provenance needs to be captured and published in a structured, machine-readable format, e.g. using W3C's PROV standard.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [Utilizing Provenance](#43-utilizing-provenance)

## Capture Creation Process

To improve the matching of crowdsourced data to use cases that are satisfied by its quality, it is necessary to understand how it was created and whether there may have been circumstances that affect its fitness for purpose.

**Related Deliverables:** [Best Practices](#2-best-practices)

**Related Use Cases:** [Utilizing Provenance](#43-utilizing-provenance)

# 6. Requirements by deliverable

For convenience, this chapter lists requirements grouped by deliverable

## 6.1 Best Practices

1. [Capture Accuracy of the Geographic Position](#capture-accuracy-of-the-geographic-position)

2. [Capture Categorical Identity](#capture-categorical-identity)

3. [Capture Currency Date and Time](#capture-currency-date-and-time)

4. [Capture Purpose For Collection](#capture-purpose-for-collection)

5. [Capture Purpose For Collection By Supplier](#capture-purpose-for-collection-by-supplier)

6. [Enable Ratings by Data Consumers](#enable-ratings-by-data-consumers)

7. [Establish Licence For Use](#establish-licence-for-use)

8. [Maintain Privacy](#maintain-privacy)

9. [Machine Readable Provenance](#machine-readable-provenance)

10. [Capture Creation Process](#capture-creation-process)

# Acknowledgements

