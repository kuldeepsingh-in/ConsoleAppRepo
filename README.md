# ConsoleAppRepo

# Data in Azure

## Storage Account
- LRS – 3 copies of your data, created synchronously, all in one data centre
- ZRS – 3 copies created synchronously, across three data centres (all in the same region). Slightly slower write latency due to multiple sites.
- GRS – 3 copies in the local data centre, and another 3 asynchronously copies in the paired data region.You can only access the remote copies when Microsoft initiates a failover. << Action: Check this as the is a roadmap to allow clients to initiate failover.We do this because we will try to understand the problem and restore the current primary to avoid data loss.
- GZRS – same as Zone redundant, but we also replicated to a secondary region. Data in the secondary regions is stored using LRS
- RA-GRS – Same as GRS, but you get read-access to the copies in the paired region.
- RA-GZRS – Same as GZRS, but you get read-access to the copies in the paired region.

## Storage Account - Disk
- The only reason to use unmanaged disks is if you need to control the storage encryption keys yourself.

## Databases
- MySQL, Postgre, Maria

## Data Lake
- Data Lakes are a massive data store 
- dump data in its native format, CSV images reports
- separate the storage and analysis elements
- to query the data we’ll spin up a compute cluster
- hirerchical namespace

## Data warehouse
- massive facility of parrlel sql servers
- Just like Azure Data Lake we separate the storage and compute
- So, you can scale the compute layer independently of the storage… 
- and the compute layer can even be paused to run at minimal cost.

## Demo: Data
- Azure Storage
- Azure SQL
- Azure Cosmos DB

# Azure Networking
