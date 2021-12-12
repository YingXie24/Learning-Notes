#Amazon Redshift

## Traditional data warehouse (on- premise)
Bottom tier (collect and cleanse)
Middle tier (OLAP, convert)
Top tier (front end client - query, analystics, data mining)

- difficult to set up and manage
- difficult to scale up / down
- performance issues
- spiralling costs (hardware, security, estate)

## Amazon redshift: Cloud based warehouse
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

## Two types of nodes available: 
Dense storage nodes (DS): storage optimised
Dense compute (DC): compute optimised
When choosing need to consider
1. Data quantity
2. Complexity of queries
3. Downstream systems

## Why use Amazon Redshift
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

# Amazon S3
- S3 is for data storage (unlimited and flexible)
- Redshift is for data analytics (structured data)
- Redshift gives you fast querying capabiilites over structured data using familiar SQL-based clents and BI tools using standard ODBC/JDBC connections. 
- The relationship between Redshift and S3 is that data can be pumped into warehouse from S3

## Object and buckets in S3
- Objects contains data, name and metadata
- A bucket stores objects
- When an object is stored in a bucket, it gets assigned an id

## Storage class
- User will specify the type of storage class for each object uploaded
1. S3 Standard for frequent data access: Frequently (daily) accessed data. The default storage class. Used for big data analytics and applications
2. S3 Standard for infrequent data access. Suitable for backups.
3. Amazon Glacier: Used where data has to be archived and high performance is not required. Cheapest. 
4. One zone IA: Used where data is infrequently accessed and stored in a single region
5. Standard Reduced Redundancy storage: Where data is non critical and reproduced quickly 

## S3 features
### Lifecycle management
Amazon S3 applies set of rules to a group of objects
1. Transition actions: moves objects from one storage class to another storage class on a defined schedule, eg. Standard -> Infrequent access -> Glacier (to save cost)
2. Expiration actions: removes objects when a specified date/ time period is reached

### Bucket policy
An IAM which allows and denies user permission to your S3 bucket

### Data encryption
Client-side encryption: data encryption at rest 
Server-side encryption: data encryption in motion

### Versioning
Preserves, recovers and restores early versions of every object you store in the S3 bucket. Each version as a different version-id. You need to enable versioning!

### Cross-region replication
Copies every object in your buckets in different AWS regions

### Transfer acceleration
Transfers data very quickly from client (local pc) to bucket over large distances, eg Mumbai to Oregon


