---
layout: project
type: project
image: images/national_mapping.jpg
title: "Ethiopian national survey: comparing school water, sanitation and hygiene with parasitic infection"
permalink: projects/national_mapping_ethiopia
# All dates must be YYYY-MM-DD format!
date: 2016-03-08
labels:
  - R
  - Kendall's &tau;
  - GIS
summary: Comparing parasite infection rates with school water, sanitation and hygiene provision in a national survey across Ethiopia.
---

Ethiopia recently conducted a national mapping of schistosomiasis and the soil-transmitted helminthiases (parasitic diseases). In this mapping, schools were purposively selected from each woreda (district) included in the survey: a set was randomly selected, then those thought to be in the areas of greatest risk for schistosomiasis were selected from that random selection.

In each of the included schools, the levels of infection with the various parasites was assessed. The school water, sanitation, and hygiene (WASH) facilities and practices were also through a set of questions to the school director (headteacher) and a guided inspection of the school facilities.

<p style="text-align:center;"><img src="/images/national_mapping_non_sq.png" alt="maps" style="max-width: 100%;  margin-bottom: -1em;"></p><p style="text-align:left;"><font size="2">These maps show the locations in Ethiopia of the schools with at least one infection detected, of the various parasites.</font></p>

The WASH data were transformed into scores, for: 

<ul>
  <li><b>Water</b>: roughly estimating the frequency of water collection from rivers and lakes for school</li>
  <li><b>Sanitation</b>: roughly the ratio of latrines to students, with each latrine weighted according to its condition</li>
  <li><b>Hygiene</b>: roughly the ratio of latrines to students, with each latrine weighted according to its facilities for handwashing</li>
</ul> 

These scores were then compared with the arithmetic mean intensity of infection (concentrations of parasite eggs in the urine and the faeces, proxies for the numbers of worms in the infections). These comparisons were carried out using Kendall's <i>&tau;</i>, a non-parametric statistic that compares ranks between the independent and dependent variables, and therefore doesn't need the variables to have any particular distributions.

Schools with more frequent water collection had statistically significantly (<i>P</i> < 0.05) higher-intensity intestinal schistosomiasis infections. Schools with better sanitation had significantly with lower roundworm, and those with better hygiene significantly lower hookworm burdens. Statistically significant associations were not found for the other WASH-parasite combinations studied. WASH improvements might affect the  various parasites differently, due to differences in the biology.

You can read the [full open-access paper published by PLOS Neglected Tropical Diseases](https://journals.plos.org/plosntds/article?id=10.1371/journal.pntd.0004515).



