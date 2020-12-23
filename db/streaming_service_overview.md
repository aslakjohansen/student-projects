# Streaming Service Overview

**Tags:** data analysis, web, http, html, graceful degradation, caching

## Introduction

Netflix offers access to a very large number of films. However, in my experience they never have any of the films that I want to watch. So the number of available films is not a good metric for comparing streaming services.

However, as films come and go on Netflix, it is really more interesting to see what the *likelyhood* of these films being available is.

As a consumer, I would like to give my money to the streaming service that best reflects my taste in both movies and shows. This business lacks transparency!

## Problem

How can we -- through transparency -- enable consumers to make informed choices regarding their streaming media service purchases?

## Approach

1. Choose a subset of services:
   - Netflix USA
   - Netflix DK
   - HBO
   - HBO Nordic
   - Amazon
   - Disney
   - ...
2. Find historical and current sources that are machine readable and can tell what is/was available. Deal with missing data by introducing a dimension of how trustworthy the foundation for the analysis is. This can be seen as a form of *graceful degradation*.
3. Create a web service that has a web interface. This service -- at its core -- takes a set of IMDB links (or similar) as input, and scores the different services.
4. The scoring takes the form of a table with services on one axis and films/shows on the other. Each combination is marked green if the medium was available all of the last two year and red if it was never available throughout this period. Gradients are used for anything in between. A percentage score summarizes each service.
5. Compare different ways of highlighting the uncertainty from point 2.
6. The user can then click on a service or a medium to fix this dimension and compare the other against time.

## Evaluation

Criterias should include (but not be limited to):
- How many requests are sent to external serices, or what bandwidth is consumed to external services.

## Related Work

- [Mobilabonnement Priser](https://mobilabonnementpriser.dk)
- [TelePrisGuide](https://teleprisguide.dk)

Sources:
- [Complete List of Movies on Netflix](https://www.whats-on-netflix.com/library/movies/)
