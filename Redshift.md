Data sources can be internal (company department) and external data.

# Traditional data warehouse (on- premise)
Bottom tier (collect and cleanse)
Middle tier (OLAP, convert)
Top tier (front end client - query, analystics, data mining)

- difficult to set up and manage
- difficult to scale up / down
- performance issues
- spiralling costs (hardware, security, estate)

# Amazon redshift: Cloud based warehouse
parallel
column-oriented
data lake

cluster: runs an amazon redshift engine and contains 1/more databases
a group of nodes = cluster
leader and compute nodes
leader nodes: receives quries from client applications, develops a query execution plan, aggregates the compute from nodes and sends it back to the client
compute nodes: execute the query plan
node slices: compute nodes are divided into slices. Slices work in parallet
client application works with leader node using SQL

# Two types of nodes available: 
Dense storage nodes (DS): storage optimised
Dense compute (DC): compute optimised
When choosing need to consider
1. Data quantity
2. Complexity of queries
3. Downstream systems

# Why use Amazon Redshift
1. Easy to set up, deploy and manage (just one click)
2. Scales quickly (resize cluster size, increase number of compute nodes)
3. Better and faster performance (columnar storage, parallel processing for high throughput)
4. Cost effective
5. Allows to query from data lake (storage repository, storing data in various raw formats)
6. Data is secure (back up in S3, encryption)

## Columnar data storage
- Data in one column is stored in one block (cf row storage, where one row is stored in one block)
- Better data compression
- Few input output

## Parallel processing
- Compute nodes + compute slices work in parallel

[link here]<https://docs.aws.amazon.com/redshift/latest/gsg/concepts-diagrams.html>

