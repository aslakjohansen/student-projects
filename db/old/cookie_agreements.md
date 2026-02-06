# Practical Cookie Agreement Analysis

**Tags:** cookies, gdpr, eprivacy regulation, web scraping, clustering

## Introduction

The practical implementation of cookie agreements leaves a lot to be desired. Often, the focus is on either misinforming the visitor or tiring them out, likely for the purpose of ensuring “consent” to wider collection privileges than the informed visitor would agree to. To inform the agreement dialogs more information is needed.

Due to the recent introduction of the General Data Protection Regulation (GDPR) regulative, websites have to inform their visitors of which kind of information they collect, how it is used, and allow the visitor to opt-out. Furthermore, does the website have to comply with the ePrivacy Regulation (Directive 2009/136), which among others enforces the current cookies laws. Websites accomplish this through a dialog which is shown to every new visitor. The different kinds of collected information (more or less referred to as cookies) can be organized in different ways; some more deceptive than others. The most popular formats seem to be:
1. A really long list, with an opt-out of all option.
2. A really long list, without an opt-out of all option.
3. Three categories covering required, functional and advertisement cookies, and allowing the visitor to opt out of any subset of the two latter.

## Problem

How are cookie agreements used today?

## Approach

Steps envisioned:
1. Find a list of the 1000+ sites most visited from Denmark (or Europe)
2. Scrape the cookie agreement form from each of these
3. Parse all collected cookie agreement forms
4. Perform statistical analysis on results to determine:
   1. What is the distribution of dialog formats?
   2. Which cookies are used most often?
   3. Which industries use which cookies?
   4. For which cookies are there categorization disagreements?
   5. Are there any patterns to categorization disagreements?
   6. Which classes of cookies can be detected?

## Related Work

Look up “privacy dark patterns”.

Other solutions than cookies:
- [https://amiunique.org](https://amiunique.org)

Laws:
- European Parliament and Council of the European Union. 2016. Regulations (EU)2016/679 of the European Parliament and of the Council - GDPR.Official Journal of the European UnionL119 (May 2016), 1–88.
- ePrivacy Regulation (Directive 2009/136)
