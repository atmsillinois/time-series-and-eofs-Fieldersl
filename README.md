Assignment objective: 
Learn about basic time series analysis concepts.
Understand how to analyze spatiotemporal time series.
Gain experience using Empirical Orthogonal Functions for dimensionality reduction and understanding spatiotemporal co-variation of geophysical quantities.

Assignment overview:
Use the land sea mask from the Thredds catalog and create a dataset that contains the monthly means of Sea Surface Temperature anomalies and total column water vapor from Jan 1979-Dec 2023 over the Pacific Basin (65°N to 65°S, 120°E to 60°W). 
While I personally did not go onto use it due to persistent errors with my data, I encourage anyone using this reference to explore the use of
of the mask.
Compute anomalies by deseasonalizing the data (remove the mean monthly anomaly from the annual mean from each point), detrend, and standardize the SST anomalies. With the modified subset of the SST data, you will perform an EOF analysis (with cosine latitude weighting) on the SST anomalies and plot a map of the first 5 EOFs.
Then, you will plot the percent variance of the first 10 EOFs from the same SST anomaly dataset.
You will then reconstruct the SST field using the first 5 EOFs and plot a map of the Pearson's correlation coefficient ([xarray.corr](https://docs.xarray.dev/en/stable/generated/xarray.corr.html)) of the reconstructed monthly time series and the "observed" SST time series.
Finally, you will compute a map of the Pearson's correlation coefficient between SST EOF1 and monthly mean detrended, deseasonalized, and standardized monthly mean column water vapor anomalies (don't mask these over land for the plot).

