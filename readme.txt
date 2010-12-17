Open Eye is a web based Business Process Management and Business Intelligence platform licensed under the GPL v3.

The main objective of Open Eye is to provide a high-end BPM and BI solution including reporting and portfolio management, for any companies at a minimal cost of acquisition and ownership.

The Open Eye platform reuses Open Source components to deliver an integrated off-the-shelf BPM and BI platform.

Components
- Process modeling (Signavio's Activiti Modeler)
- Process design, development and testing (Eclipse and Activiti Eclipse Plugin)
- Process runtime engine (Activiti)
- Process monitoring, reporting and analytics (Birt)
- Rich web interface for process management, process execution and process monitoring (Richfaces)
- Framework for component and service integration (Seam)

Content
- Process templates based on best practices and industry standards
- Report templates based on best practices and industry standards

Here follows instructions on how to setup, build and run Open Eye from the source code. 

1. How to run Open Eye from sources

1.1 Download

The source files can be downloaded from github located at the following url: git@github.com:patobe/openeye.git

1.2 Tools

The following tools are recommended for building Open Eye from the source files: Java JDK SE 6 (Java development toolkit), Ant (automates the software building process), Git (source code management), Eclipse (integrated development environment), JBoss Application Server 5.1 or 6.X, MySQL Community Server 5.5.X and MySQL Connector/J.

1.3 Setup

Install Java JDK , Ant, Git, Eclipse and JBoss Application Server. Import the downloaded Eclipse project into Eclipse. Open the build.properties file and change the jboss.home value to match your setup. Install MySQL, create a new schema and name it openeye. Create a new user and name it openeye, leave the password blank or update the openeye-ds.xml with the new password. Login to mysql with the new user named openeye and run the import-dev.sql script to create the tables. Copy the MySQL connector to <jboss.hom>/server/default/lib. 

1.4 Build

Select project/clean to build the distribution and deploy it to your JBoss Application Server.

1.5 Verify

Make sure that the openeye.ear and openeye-ds.xml is present in <jboss.home>/server/default/deploy (substitute jboss.home with the value specified in the build.properties file)

1.6 Run
Change to <jboss.home>/bin and type run.bat (Windows) or run.sh (Linux).

1.8 Login

Open your point your web browser to http://localhost:8080/openeye and enter username: admin and password: admin to login.


2. How to deploy process definitions

2.1 Download 

The process definitions can be downloaded from github located at the following url: git@github.com:patobe/openeye-processes.git.

2.2 Login

Open your point your web browser to http://localhost:8080/openeye and enter username: admin and password: admin to login.

2.3 Deploy

Change to the Definitions tab and click on the Create Deployment button. Select the openeye-process.bar from the download folder. Upload the process definition archive.

2.4 Verify

Change to the Tasks tab and click on the New button. Select a process from the drop-down list. A new task should now be visible in the Unassigned task list. Right click on the task and select Claim task from the drop-down list. The task should now be moved to the Assigned Tasks list. Select the task to view the associated task form. Fill in the data and click on the Complete button.


3. How to work with processes and tasks

3.1 Todo
