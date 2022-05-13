# Multivariate Anomaly Detection
Azure Multivariate Anomaly Detection service is used to detect anomaly across a set of network nodes. The dataset should be in the below format

        INDEX,NODE_ID,Time,MI_1,MI_2,MI_3,MI_4

Where MI_1, MI_2, MI_3, MI_4 are multi variate variable across which MVAD service is used to detect anomalies. 


## Anomaly Detection using one network node as training data set
mvad-networknodes.ipynb notebooks uses a given network node id as source data for training the MVAD service. This trained model is to infere anomaly in another network node. This can be used if there are isn't too much variation in data value ranges across the network nodes. 

![Anomaly Detection across different node with quite a bit of data variation](bokeh_plot_different_nodes.png)

## Anomaly Detection using one network node as both training and inference data set
mvad-networknodes-same-dataset.ipynb notebooks uses a given network node id as source data for training the MVAD service. This trained model is to infere anomaly in across the same node id used in the training but across a different sliding window. 

![Anomaly Detection across different node with quite a bit of data variation](bokeh_plot_same_node.png)


## Variation in data values across different node ids
![](data variation across nodes.png)