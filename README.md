# starbucks_excercise for Udacity DSND

## Introduction

This exercise is apparently given as a take home for potential candidates at Starbucks (to be a barista?). The challenge is to take examples of people fitting seven features, and look at their response rates to a particular promotion.

Starting from initial data with a negative value proposition based on its costs, the job is to turn this into a profitable promotion via targeting more responsive consumers.

## Data

All data provide by Starbucks and is simulated, as not to violate any privacy considerations.

## Method

I fist look at features, and see two look numerical, and the others are potentially categorical, so standard scaling and one hot encoding are applied respectively.

After that KMeans is fit with differing numbers of clusters up to 8 on the transformed features, and the change in purchase rate or irr is calculated for individual clusters.

The fit is analyzed to find the highest response rate for any particular cluster, also considering the size of the cluster predicted.

Clustering is applied to unseen data, and only people in the best irr cluster are shown the promotion.

This eventually moves from an nrr of ~-2000, up to ~+185, which is as good as the code suggests was done by the authors.
