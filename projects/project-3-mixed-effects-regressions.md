---
layout: project
type: project
image: images/30_schools_map_sq.jpg
title: Mixed-effects regressions comparing sanitation, hookworm infection, and child health
permalink: projects/mixed_effects_regressions
# All dates must be YYYY-MM-DD format!
date: 2017-10-09
labels:
  - R
  - lme4
  - mixed-effects
summary: Research into the relationships between environmental risk factors, parasite infection, and anaemia, stunting and wasting.
---

<h2>Hookworm</h2>

Hookworms are parasitic roundworms that live in the intenstine and feed on blood. 

<b>Transmission</b>

Infection occurs when hookworm larvae in the soil come into contact with, then burrow through, the bare skin. The worms living in the intestines lay eggs that leave the body in the faeces - open defecation puts these eggs into the soil, where they develop into larvae, which can later infect people coming into contact with the soil. 

However, open defecation alone will not increase the risk of infection if larvae die before they can infect a person, for example because:

 <ul>
  <li>Soil conditions are not conducive to larval develop (for example if it's too dry)</li>
  <li>People never come into direct contact with the soil</li>
</ul> 

<b>Health effects</b>

Hookworms feed on blood - this can cause anaemia, which in turn can lead to developmental problems such as: 

<ul>
  <li>Stunting (low height-for-age)</li>
  <li>Wasting (low weight-for-height)</li>
</ul> 

However, the relative importance of hookworm infection in causing these depends on the local prevalence of other factors, such as inadequate diet and other pathogens: for example, if no-one is has an adequate diet, then people will be anaemic regardless of their hookworm infection status.  

<h2>About this work</h2>

In this project, we sought to quantify the strengths of the realtionships outlined above. We used data collected from children in 30 schools in southern Ethiopia (this work forming part of a broader study investigating optimal delivery of school health programmes). Data were compared using mixed-effects logistic regressions, implemented in R's lme4 package: this allowed the models to account for the clustered nature of the data (children, in schools, in clusters of schools).

<p style="text-align:center;"><img src="/images/30_schools_map.png" alt="map" style="max-width: 100%;  margin-bottom: -1em;"></p><p style="text-align:left;"><font size="2">A map showing the locations of the 30 schools in southern Ethiopia.</font></p>

<b>Findings</b>

In mixed-effects models accounting for age, gender, school- and school-cluster level effects, we did not find any statistically significant associations between any of the relationships studied:

<ul>
  <li>Latrine absence at home and hookworm infection (adjusted odds ratio, OR = 1.28, 95% confidence interval, CI: 0.476–3.44)</li>
  <li>Evidence of open defecation at home, and hookworm infection (adjusted OR = 1.21, 95% CI: 0.468–3.12)</li>
  <li>Hookworm infection and anemia (adjusted OR = 1.24, 95% CI: 0.988–1.57)</li>
  <li>Hookworm infection and stunting (adjusted OR = 0.992, 95% CI: 0.789–1.25)</li>
  <li>Hookworm infection and wasting (adjusted OR = 0.969, 95% CI: 0.722–1.30)</li>
</ul> 

However, the relationship between hookworm infection and anaemia was borderline significant (<i>P</i> = 0.06).

You can read the [full open-access paper published by PLOS Neglected Tropical Diseases](https://journals.plos.org/plosntds/article?id=10.1371/journal.pntd.0005948).
