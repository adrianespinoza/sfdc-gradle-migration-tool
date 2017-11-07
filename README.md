**SFDC Gradle Migration Tool**
===================


Salesforce migration tool using **Gradle**<i class="icon-cog"></i>. This tool helps to migrate changes made in an salesforce environment to another, by configuring a couple of files and executing a simple gradle command.

----------

Prerequisites <i class="icon-cog"></i>
-------------
> - java v8.x.
> - Gradle v4.3

> **Note:**
> 
> - This project contains gradle wraper, if you do not need to install and configure gradle, you can directly execute the gradlew.bat from the main folder

Configuration and execution <i class="icon-cog"></i>
-------------

> **Migration:**

> - In the **build.properties** file located in **.../gradle/sfdc/** enter the credentials for source and target environments.
> - In the **package.xml** file located in **.../gradle/sfdc/config/unpackaged/** define the items that will be recovered form the source environment.
> - From the main folder open a cmd prompt and execute this command: **gradle migrate**.

#### Revert changes
Is there also an option to revert the change made in the target environment by executing a gradle command:
> **Undeploy:**

> - In the **build.properties** file located in **.../gradle/sfdc/** enter the credentials for source and target environments.
> - In the **destructiveChanges.xml** file located in **.../gradle/sfdc/config/remove/** define the items that will be removed form the target environment.
> - From the main folder open a command prompt and execute this command: **gradle undeploy**.