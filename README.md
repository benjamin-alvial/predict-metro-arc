# Metro Arc Prediction
In this project, machine learning models are used to predict the arc traveled by a metro train, based on its acceleration signal. The data has been personally gathered with a mobile device fixed to an inside front ledge of the train using Phyphox to measure acceleration. The app's output acceleration signals are four: x, y, z, and absolute acceleration.

Line 6 from the Santiago Metro has been chosen because it has an automated operation and because of its most notable curvature. Both of these aspects are assumed to generate more predictable and distinct movements which would be easier to classify. Line 6 is composed of 10 stations. Considering the southbound route (to Cerrillos) and northbound route (to Los Leones), there are 18 possible arcs to which acceleration signals can be classified.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/4/49/L%C3%ADnea_6_-_Metro_de_Santiago.svg" width=50% height=50% align="center">
</p>

## Hypothesis
It is expected that arcs with more distinct curvatures have better classification performance. For example, the two arcs (north and southbound) that connect Estadio Nacional with Ñuñoa have a very sharp curvature, which is expected to be represented in its acceleration signal. Similarly, the arcs that connect Cerrillos with Lo Valledor should have a similar performance. It must be noted that the duration of the signal could make this problem trivial, as fixed distances traveled with programmed velocities could induce very similar times for different runs of the same arcs. Therefore, initially, features that include the time variable are not considered, although the variable will be measured to verify if times are indeed approximately constant for a given arc.
<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/e/ee/Linea_6_Metro_de_Santiago_mapa.png" width=50% height=50% align="center">
</p>
