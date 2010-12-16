How to run Open Eye from sources

1. Download

The source files can be downloaded from github located at the following url: git@github.com:patobe/openeye.git

2. Tools

The following tools are recommended for building Open Eye from the source files: Java JDK SE 6 (Java development toolkit), Ant (automates the software building process), Git (source code management), Eclipse (integrated development environment), JBoss Application Server 5.1 or 6.X.

3. Setup

Install Java JDK , Ant, Git, Eclipse and JBoss Application Server. Import the downloaded Eclipse project into Eclipse.

4. Build

Before building the project open the build.properties file and change the jboss.home value to match your setup. Select project/clean to build the distribution and deploy it to your JBoss Application Server.

5. Verify

Make sure that the openeye.ear and openeye-ds.xml is present in <jboss.home>/server/default/deploy (substitute jboss.home with the value specified in the build.properties file)

6. Run
Change to <jboss.home>/bin and type run.bat (Windows) or run.sh (Linux).

8. Login

Open your point your web browser to http://localhost:8080/openeye and enter username: admin and password: admin to login.


How to deploy process definitions

1. Download 

The process definitions can be downloaded from github located at the following url: git@github.com:patobe/openeye-processes.git.

1. Login

Open your point your web browser to http://localhost:8080/openeye and enter username: admin and password: admin to login.

2. Deploy

Change to the Definitions tab and click on the Create Deployment button. Select the openeye-process.bar from the download folder. Upload the process definition archive.

3. Verify

Change to the Tasks tab and click on the New button. Select a process from the drop-down list. A new task should now be visible in the Unassigned task list. Right click on the task and select Claim task from the drop-down list. The task should now be moved to the Assigned Tasks list. Select the task to view the associated task form. Fill in the data and click on the Complete button.



How to work with processes and tasks

Todo