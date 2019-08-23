---
layout: project
type: project
image: images/face_rec_investigation_sq.png
title: Face recognition distances investigation
permalink: projects/face_recognition
# All dates must be YYYY-MM-DD format!
date: 2019-08-15
labels:
  - Python
  - face_recognition
  - matplotlib
  - pandas
summary: I investigated the distances returned by face_recogntion for the same and for different faces, to inform the optimal choice of cut-off.
---

<a href="https://pypi.org/project/face_recognition/">face_recognition</a> is a Python package containing pre-trained deep neural networks for that can be used to recognise and compare faces (provide a score reflecting their similarity). It uses a convolutional neural network to convert an image of a face to a set of 128 'encodings': numbers that are similar for different images of the same face, but different for images of different faces. The Euclidean distance between two sets of encodings can be interpreted as a facial 'distance': a measure of how different the faces are. Face recognition works by comparing these face distances with a cutoff: below the cutoff, the faces are taken as being the same, and above, they are taken as being different. By varying the cutoff you can vary the precision and recall - with a lower cutoff, you are less likely to identify pairs of images as being of the same face, but you can have higher confidence where you do so. Conversely, with a higher cutoff, you are more likely to identify pairs of images as being of the same face, but you can have less confidence where you do so. You can read more about this at <a href="https://medium.com/@ageitgey/machine-learning-is-fun-part-4-modern-face-recognition-with-deep-learning-c3cffc121d78">this blog post by the author of the package</a>.

<a href="http://vis-www.cs.umass.edu/lfw/">Labeled Faces in the Wild</a> is a dataset of images of people, structured by the person shown in the image. I compared the 81,875,206 pairs in 12,797 images (of 5,749 people) from this dataset, keeping track of whether they distance, and whether the images were of the same, or different, faces. The resulting distribution of face distances, for pairs of images of the same, and different, faces, is shown below:

<p style="text-align:center;"><img src="/images/face_rec_investigation.png" alt="graph" style="max-width: 100%;"></p>

By collecting the face distances for all those combinations, comparing them with various cutoffs, and summing the correct and incorrect classifcations at each of those cutoffs, I generated the following table of precision and recall at various face distance cutoffs:

<table>
  <tr>
    <th>cutoff</th>
    <th>precision</th>
    <th>recall</th>
  </tr>
  <tr>
    <td>0.00</td>
    <td>0.00</td>
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
    <td>0.70</td>
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


While carrying out these comparisons, we can also investigate which people look the most different in different images. The top 10 pairs of images of the same people, but with the highest face distances, are shown below. The face distances are in the table below the images.

<p style="text-align:center;"><img src="/images/different_looking_same_people.jpg" alt="different_looking_faces" style="max-width: 30%;"></p>

<table>
  <tr>
    <th></th>
    <th>Name</th>
    <th>Face Distance</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Nicole Kidman</td>
    <td>0.90</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Michael Schumacher</td>
    <td>0.89</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Bill Simon</td>
    <td>0.81</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Recep Tayyip Erdogan</td>
    <td>0.78</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Debra Messing</td>
    <td>0.78</td>
  </tr>
  <tr>
    <td>6</td>
    <td>Cristina Fernandez</td>
    <td>0.76</td>
  </tr>
    <tr>
    <td>7</td>
    <td>Jennifer Lopez</td>
    <td>0.74</td>
  </tr>
  <tr>
    <td>8</td>
    <td>Janica Kostelic</td>
    <td>0.73</td>
  </tr>
  <tr>
    <td>9</td>
    <td>Lance Armstrong</td>
    <td>0.72</td>
  </tr>
    <tr>
    <td>10</td>
    <td>Anna Kournikova</td>
    <td>0.71</td>
  </tr>
</table>

Reasons for these high face distance scores seem to include things obscuring the faces, and photos not taken straight-on.

The code is available at [GitHub](https://github.com/jackgrimes/face_distance_investigation).



