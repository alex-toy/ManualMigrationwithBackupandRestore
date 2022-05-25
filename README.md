Manual Migration with Backup and Restore
=
In this project, we will be creating a local environment with a schema and some data in a database. Afterward, we will create a back up of the database that we will later use to restore in Azure.

Local Database Environment
Install and configure the Postgres database locally:
If you have not already installed Postgres, you can find install instructions here
Log in to PGadmin portal and create a database:
Name: bookreviewdb
Add a Table with the following definitions:
Table Name: review
Columns:
id: integer, primary key, identity with auto increment, not null
name: text, not null
email: text, not null
job_position: text, not null
company: text, not null
review: text, not null
Manually add 3 reviews to the database via the admin portal:

Review 1:

name: Enoch Josh
email: enoch@josh.com
job_position: Medical Chief Officer
company: Mouelet Medical Center
review: I recommend this book to all my medical students because lessons, stories, advice from this artistic work applies both in engineering as well as in the medical field.
Review 2:

name: Lily Michele
email: lily@michele.com
job_position: Chief Data Scientist
company: TOKO LLC
review: I wish I had a role model like her to outline my goals and dreams in order to avoid the common mistakes of a young and enthusiastic engineer. Buy, read, and offer a copy to someone younger than you!
Review 3:

name: Laidry Arian
email: laidry@arian.com
job_position: CEO
company: MabsInsvestment
review: This a classic GPS for this generation; it outlines what to do, what not to do, when to do it, how to do it, and why taking the risk is the greatest legacy you can ever give yourself.
Create a backup of the reviewdb database and save it locally

Azure Environment
Create an Azure resource group
Create an Azure Postgres Database Service:
Server Type: Single Server Postgres
Server Version: select the latest
Compute and Storage: Basic, with 1 vcore, and 5GB of storage
Allow access to all IP Address range
Restore the recently created backup from reviewdb to the Azure Postgres database
Cleanup and delete resources
Be sure to cleanup and delete resources to avoid recurring charges