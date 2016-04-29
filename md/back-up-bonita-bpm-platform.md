# 2.6 Back up Bonita BPM Platform

Any basic one node (non-clustered) installation can be backed up to be restored later. 
In a [Bonita BPM cluster](/overview-of-bonita-bpm-in-a-cluster.md), you need to back up the nodes, the shared database, and the shared [Bonita home](/bonita-home.md).

## How to back up an installation

A cold backup (total shutdown) is recommended, to avoid losing data being processed during the backup process. Note: make sure your database server is backed up. 
(Please refer to the specific documentation for your database concerning the backup procedure).

1. Stop the application server
2. Save the BONITA\_HOME directory. 
3. Save the Application Server configuration files modified during Bonita setup.
4. Save the deployed web application (i.e. `bonita.war`) (for Tomcat `[TOMCAT_HOME]/webapps/bonita.war`), or you can redeploy all applications at startup. 
If you decide not to save the `webapps` directory, make sure that you have a copy of your Bonita application available.
5. Back up your database (Please refer to the specific documentation for your database concerning the backup procedure).
6. Start the application server.