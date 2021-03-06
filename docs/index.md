---
title: "edi3 Inter Customs Ledger 0.1.0 Specification"
specID: "icl/1"
status: "![raw](http://rfc.unprotocols.org/spec:2/COSS/raw.svg)"
editors: "[Chris Gough](https://github.com/monkeypants)"
contributors: "[Richard Spellman](https://github.com/arpentnoir)"
---

## Abstract
This document proposes the use of a permissioned Inter Customs Ledger to facilitate the transfer of regulatory documents between customs agencies. 

## Status

This document is currently focussed toward providing enough background content to inform discussions on elaborating the design of an Inter Customs Ledger. 


## Glossary

Phrase | Definition
------------ | -------------
| Authorised Body| In this document, the term Authorised Body is used to denote an organisation which has authority to issue some Document. e.g. A Chamber of Commerce which issues Certificate of Origin under some FTA, a CITES Management Authority which issues CITES Permits, etc.|
| Document | When capitalised in this document, this term refers to any document which gives authorisation for an importer or exporter to take some action (or be granted some further authority) with respect to an international shipment of goods. e.g. a Certificate of Origin, a Phytosanitary Certificate, an Export Declaration, etc| 
| Node | A device on the Inter Customs Ledger network which has full visibility of the entire ledger and contriibutes to the integrity of the ledger by implementing a Consensus Algorithm |

## Introduction
International trade clearance procedures require a number of documents to be presented to satisfy the requirements of a variety of agreements. For example, in order for an importer to gain preferential tariff treatment under a Free Trade Agreement, the importer must present a valid Certificate of Origin (issued to the exporter) which states that the goods being imported qualify as originating in the country which is party to the agreement. These processes are managed largely by the transfer of paper documents which are subject to loss, alteration and forgery. 

An Inter Customs Ledger is proposed as an apporach to the transfer of shipment related documents between customs agencies which is immediate, permanent and irrefutable.

This document uses Certificates of Origin as the guiding use case for the initial specification, however it is intended that the Inter Customs Ledger should be generic and allow for the transfer of any shipment related documentation between authorised agencies. 


#### Background
There have been a number of recent projects which use blockchain to implement a system which allows the validation of Certifiate of Origin issued under some Free Trade Agreement. Singapore and Kenya have both worked with industry parter vCargo Cloud to implement blockchain Certificate of Origin solutions. The first Certificate of Origin for a shipment from the UK was issued by {who?} in {month?} 2018 and in {when?} the United States were looking into the use of blockchain to validate Certificates of Origin for shipments made under {old agreements?}. These projects have highlighted the necessity for digital, blockchain based solutions to exist alongside paper based processes in the short term, requiring the continued existance of some mechanism for validating the authenticity of a paper certificate. 

Before the prevalence of distributed ledger technology, the common approach to providing for assurance as to the validity of a Document was largely achieved with the idea of a hub. there are a number of implementations of this approach which may be instructive: ICC Certificate of Origin verification website, EPIX, ePhyto thing, etc... 

The link below provides a number of resources which attempt to give an overview of the landscape of blockchain based projects related to both Certificates of Origin and International trade in general

[Survey of Blockchain Based Approaches to Managing International Trade Documentation](precedents.md)


## Licence

All material published on edi3.org including all parts of this specification are the intellectual property of the UN as per the [UN/CEFACT IPR Policy](https://www.unece.org/fileadmin/DAM/cefact/cf_plenary/plenary12/ECE_TRADE_C_CEFACT_2010_20_Rev2E_UpdatedIPRpolicy.pdf).

This Specification is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version. See http://www.gnu.org/licenses.
 
## Change Process

 This document is governed by the [2/COSS](http://rfc.unprotocols.org/spec:2/COSS/) (COSS).

## Language

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" 
in this document are to be interpreted as described in RFC 2119.

# High Level Requirements
> FIXME 
seperate the list below into sections? (Ledger, Network, Transaction) 

1. Any Customs Authority SHOULD be able to participate in the ICL by running a Node
2. Participating in the network by running a Node SHOULD NOT grant access to the content of a document
3. A message on the Inter Customs Ledger MAY provide a mechanism for discovering the full content of the document to which it relates
4. The Inter Customs Ledger MUST provide a mechanism for preventing an importer or exporter from re-using a document which is intended to have a single use
5. The Inter Customs Ledger MUST provide some mechanism for asserting the validity of a document presented by an importer or exporter 
6. The Inter Customs Ledger MUST provide some mechanism for invalidating a Document
7. The Inter Customs Ledger MUST provide some mechanism for specifying who can perform certain actions with respect to a Document

