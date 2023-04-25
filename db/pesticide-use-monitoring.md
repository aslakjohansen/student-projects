# Pesticide Use Monitoring

**Tags:** NDVI, satellite data, multi-spectral imagery, 

## Introduction

In collaboration with the Danish Environmental Protection Agency (da: Miljøstyrelsen).

Multispectral data from satellites can be used to detect to calculate the photosynthetic activity (aka "greeness") of areas. When combined with GIS data defining the geographical areas of farmers plots, such plots can be mapped to greenness. Each pass these satellites generate a snapshot of that mapping at a single point in time. The history of passing shows how it evolves over time.

## Problem

Pesticides from the agricultural sector are finding their way into the ground water. While there are regulations in place to govern when and how much can be sprayed, the reality is that a only a small number of annual inspections are mandated. As a result, chances of getting caught are slim.

## Approach

By analyzing this evolution we can detect which plots have likely been exposed to excessive amounts of pesticides, and use this to guide the inspectors to the most likely violations. That will make the act of polluting our groundwater more risky.

Concretely:
- The project will analyze satellite imagery from July 1st to December 1st (both 2020) in order to detect events of plots withering.
- The project will focus on potatoes, where pesticides are being used to wither the plants to avoid fungal infection. This happens in the July-September period.
- In addition to temporal restrictions of then pesticides can be used, there are also geographical restrictions in terms distance to water courses and public areas.

## Related Work

- Miljøstyrelsen, Afd. P. og B. (2022, april 5). [Fagligt notat om resultater af screening for pesticidstoffer i grundvand 2021](https://mst.dk/media/243329/endelig_fagligt-notat-om-resultater-af-screening-for-pesticidstoffer-i-grundvand-2021.pdf).
- [Bekæmpelsesmiddelbekendtgørelsen nr 987 af 22/06/2022](https://www.retsinformation.dk/eli/lta/2022/987), BEK nr 987 af 22/06/2022 (2022).
- Miljø- og Fødevareministeriet. (2020, november 13). [Årsrapport 2019 for kontrol i Danmark i medfør af kontrolforordning 882/2004](https://www.foedevarestyrelsen.dk/SiteCollectionDocuments/Kontrolstyring/Diverse%20%C3%A5rsrapporter/%C3%85rsrapport%202019.pdf).
- Den Europæiske revisionsret. (2021). [Princippet om, at forureneren betaler: Inkonsekvent anvendelse på tværs af EU’s miljøpolitikker og foranstaltninger](https://data.europa.eu/doi/10.2865/612980). Særberetning, nr. 12, 2021.

## Additional

Governmental mapping of ground water by the Danish Environmental Protectil Agency (da: Miljøstyrelsen): Ground water with coding for drinking water interests (da: drikkevndsinteresser, OSD) and collection area (da: indvindingsopland, IOL) for water resources:
[<img src="https://github.com/aslakjohansen/student-projects/raw/master/db/figs/groud-water.png">](https://mst.dk/natur-vand/vand-i-hverdagen/grundvand/grundvandskortlaegning/)


Detected pesticides with indication of threshold value (da: grænseværdi, GV):
[<img src="https://github.com/aslakjohansen/student-projects/raw/master/db/figs/pesticide-level.png">](https://data.geus.dk/geusmap/?mapname=grundvand#baslay=baseMapDa&optlay=&extent=29341.797086927923,5632862.6489539575,1236008.4637535946,6924373.0656206235&layers=mc_grp_analyse&filter_0=dgu_nr%3D%26stofgruppe.num%3D50%26maengde.min%3D%26proeveaar.min%3D%26boringstype%3D%26boringsanvendelse.part%3Dvand%26kommune_navn.part%3D%26stof_tekst_hidden.part%3D%26indtag_bund_dybde.min%3D%26indtag_top_dybde.max%3D%26grumo_loop%3D)

