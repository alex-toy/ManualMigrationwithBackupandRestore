Manual Migration with Backup and Restore
=
In this project, we will be creating a local environment with a schema and some data in a database. Afterward, we will create a back up of the database that we will later use to restore in Azure.

## Local Database Environment
1. Log in to PGadmin portal and create a database: Name: bookreviewdb
2. Add a Table with the following definitions:
    - Table Name: review
    - Columns:
    - id: integer, primary key, identity with auto increment, not null
    - name: text, not null
    - email: text, not null
    - job_position: text, not null
    - company: text, not null
    - review: text, not null
3. Manually add 3 reviews to the database via the admin portal


## Azure Environment
1. Create an Azure resource group
2. Create an Azure Postgres Database Service:
    - Server Type: Single Server Postgres
    - Server Version: select the latest
    - Compute and Storage: Basic, with 1 vcore, and 5GB of storage
3. Allow access to all IP Address range
4. Restore the recently created backup from reviewdb to the Azure Postgres database
Cleanup and delete resources : Be sure to cleanup and delete resources to avoid recurring charges