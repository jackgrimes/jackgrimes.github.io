---
layout: project
type: project
image: images/face_rec_investigation_sq.png
title: Face recognition distances investigation
permalink: projects/face_recognition
# All dates must be YYYY-MM-DD format!
date: 2019-08-23
labels:
  - Python
  - face_recognition
  - matplotlib
  - pandas
summary: I investigated the distances returned by face_recogntion for the same and for different faces, to inform the optimal choice of cut-off.
---

<a href="https://pypi.org/project/face_recognition/">face_recognition</a> is a Python package containing pre-trained deep neural networks for that can be used to recognise and compare faces (provide a score reflecting their similarity). It uses a convolutional neural network to convert an image of a face to a set of 128 'encodings': numbers that are similar for different images of the same face, but different for images of different faces. The Euclidean distance between two sets of encodings can be interpreted as a facial 'distance': a measure of how different the faces are. Face recognition works by comparing these face distances with a cutoff: below the cutoff, the faces are taken as being the same, and above, they are taken as being different. By varying the cutoff you can vary the precision and recall - with a lower cutoff, you are less likely to identify pairs of images as being of the same face, but you can have higher confidence where you do so. Conversely, with a higher cutoff, you are more likely to identify pairs of images as being of the same face, but you can have less confidence where you do so. You can read more about this at <a href="https://medium.com/@ageitgey/machine-learning-is-fun-part-4-modern-face-recognition-with-deep-learning-c3cffc121d78">this blog post by the author of the package</a>.

I compared the 81,875,206 pairs in 12,797 images (of 5,467 people), keeping track of whether they distance, and whether the images were of the same, or different, faces. The resulting distribution of face distances, for pairs of images of the same, and different, faces, is shown below:

<p style="text-align:center;"><img src="/images/face_rec_investigation.png" alt="graph" style="max-width: 100%;"></p>

By collecting the face distances for all those combinations, comparing them with various cutoffs, and summing the correct and incorrect classifications at each of those cutoffs, I generated the following table of precision and recall at various face distance cutoffs:

<table>
  <tr>
    <th>cutoff</th>
    <th>precision</th>
    <th>recall</th>
  </tr>
  <tr>
    <td>0.00</td>
    <td>1.00</td>
    <td>0.00</td>
  </tr>
  <tr>
    <td>0.30</td>
    <td>1.00</td>
    <td>0.02</td>
  </tr>
  <tr>
    <td>0.40</td>
    <td>1.00</td>
    <td>0.29</td>
  </tr>
  <tr>
    <td>0.45</td>
    <td>0.98</td>
    <td>0.59</td>
  </tr>
  <tr>
    <td>0.50</td>
    <td>0.91</td>
    <td>0.84</td>
  </tr>
  <tr>
    <td>0.55</td>
    <td>0.71</td>
    <td>0.96</td>
  </tr>
    <tr>
    <td>0.60</td>
    <td>0.34</td>
    <td>0.99</td>
  </tr>
  <tr>
    <td>0.90</td>
    <td>0.00</td>
    <td>1.00</td>
  </tr>
  <tr>
    <td>1.00</td>
    <td>0.00</td>
    <td>1.00</td>
  </tr>
    <tr>
    <td>1.50</td>
    <td>0.00</td>
    <td>1.00</td>
  </tr>
</table>

The code is available at [GitHub](https://github.com/jackgrimes/face_distance_investigation).



