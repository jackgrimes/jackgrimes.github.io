---
layout: project
type: project
image: images/journeys_sq.png
title: Journey Plotter
permalink: projects/journey_plotter
# All dates must be YYYY-MM-DD format!
date: 2019-07-18
labels:
  - Python
  - Geopandas
summary: Using geopandas to plot cycling journeys over time. Different formats can produce videos that use colours to show different speeds or journeys at different times.
---

This is a project that plots cycling journeys over time, to produce videos of the journeys building up over time, as well as final plots of all the journeys (either by year, or over all time). It takes data from [Runkeeper](https://runkeeper.com/), and uses [Ffmpeg](https://ffmpeg.org/) to produce the videos.

These are some of the types of video it can make:

<p><b>Overall</b>
<br>Journeys build up over time. Colours indicate speed: between red for stationary, and yellow for 18 mph and above. Black points are the start and finish of journeys.
<video width="100%"  poster="../journey_plotter_files/overall_thick.png" controls>
  <source src="../journey_plotter_files/overall_thick.mp4" type="video/mp4">
  <!--to get video to work in chrome, need to run ffmpeg
  ffmpeg -i input.mp4 -vcodec h264 output.mp4
  -->
</video></p>

<p><b>Overall, bubbling off</b>
<br>Journeys gradually expand and disappear. Colours indicate speed: between red for stationary, and yellow for 18 mph and above. Black points are the start and finish of journeys.
<video width="100%"  poster="../journey_plotter_files/overall_bubbling_off.png" controls>
  <source src="../journey_plotter_files/overall_bubbling_off.mp4" type="video/mp4">
  <!--to get video to work in chrome, need to run ffmpeg
  ffmpeg -i input.mp4 -vcodec h264 output.mp4
  -->
</video></p>

<p><b>Overall, shrinking</b>
<br>Journeys gradually shrink into place. Colours indicate speed: between red for stationary, and yellow for 18 mph and above. Black points are the start and finish of journeys.
<video width="100%"  poster="../journey_plotter_files/overall_shrinking.png" controls>
  <source src="../journey_plotter_files/overall_shrinking.mp4" type="video/mp4">
  <!--to get video to work in chrome, need to run ffmpeg
  ffmpeg -i input.mp4 -vcodec h264 output.mp4
  -->
</video></p>

<p><b>Running recents</b>
<br>Journeys disappear 99 new journeys have been plotted (so no more than 100 journeys present at any time). Colours indicate speed: between red for stationary, and yellow for 18 mph and above. Black points are the start and finish of journeys.
<video width="100%"  poster="../journey_plotter_files/running_recents.png" controls>
  <source src="../journey_plotter_files/running_recents.mp4" type="video/mp4">
  <!--to get video to work in chrome, need to run ffmpeg
  ffmpeg -i input.mp4 -vcodec h264 output.mp4
  -->
</video></p>

<p><b>End points, bubbling off</b>
<br>Only the start (in green) and finish (in blue) of each journey is plotted. These gradually expand and disappear.
<video width="100%"  poster="../journey_plotter_files/end_points_bubbling.png" controls>
  <source src="../journey_plotter_files/end_points_bubbling.mp4" type="video/mp4">
  <!--to get video to work in chrome, need to run ffmpeg
  ffmpeg -i input.mp4 -vcodec h264 output.mp4
  -->
</video></p>

<p><b>End points, shrinking into place</b>
<br>Only the start (in green) and finish (in blue) of each journey is plotted. These gradually shrink into place.
<video width="100%"  poster="../journey_plotter_files/end_points_shrinking.png" controls>
  <source src="../journey_plotter_files/end_points_shrinking.mp4" type="video/mp4">
  <!--to get video to work in chrome, need to run ffmpeg
  ffmpeg -i input.mp4 -vcodec h264 output.mp4
  -->
</video></p>

<p><b>Dark</b>
<br>Journey points are plotted in white on a black background.
<video width="100%"  poster="../journey_plotter_files/dark.png" controls>
  <source src="../journey_plotter_files/dark.mp4" type="video/mp4">
  <!--to get video to work in chrome, need to run ffmpeg
  ffmpeg -i input.mp4 -vcodec h264 output.mp4
  -->
</video></p>

<p><b>Dark, colours changing in time</b>
<br>Journey points are plotted on a black background. They are plotted with colours that vary over time.
<video width="100%"  poster="../journey_plotter_files/dark_colours_by_time.png" controls>
  <source src="../journey_plotter_files/dark_colours_by_time.mp4" type="video/mp4">
  <!--to get video to work in chrome, need to run ffmpeg
  ffmpeg -i input.mp4 -vcodec h264 output.mp4
  -->
</video></p>
 
Source: <a href="https://github.com/jackgrimes/journey_plotter"><i class="large github icon"></i>jackgrimes/journey_plotter</a>