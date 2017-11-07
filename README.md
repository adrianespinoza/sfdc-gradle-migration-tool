**SFDC Gradle Migration Tool**
===================


Salesforce migration tool using **Gradle**<i class="icon-cog"></i>. This tool helps to migrate changes made in an salesforce environment to another, by configuring a couple of files and executing a simple gradle command.

----------


Project File Structure <i class="icon-folder-open"></i>
-------------

<i class="icon-folder-open"></i>sfdc-gradle-migration-tool
│   <i class="icon-file"></i>.gitignore  
│   <i class="icon-file"></i>gradlew
│   <i class="icon-file"></i>gradlew.bat
│   <i class="icon-file"></i>settings.gradle
│   <i class="icon-file"></i>README.md   
│
└───<i class="icon-folder-open"></i>gradle
│   │
│   └───<i class="icon-folder-open"></i>sfdc
│	 │ 	└───<i class="icon-folder-open"></i>config
│   │	│   │   <i class="icon-file"></i>build.gradle
│   │	│  	│
│	 │ 	│	└───<i class="icon-folder-open"></i>remove
│   │	│	│   │   <i class="icon-file"></i>destructiveChanges.xml
│   │	│	│   │   <i class="icon-file"></i>package.xml
│	 │	   │	│
│	 │ 	│	└───<i class="icon-folder-open"></i>unpackaged
│   │	│	    │   <i class="icon-file"></i>package.xml
│	 │	   │
│	 │ 	└───<i class="icon-folder-open"></i>output
│   │	│   └───<i class="icon-folder-open"></i>migration
│   │	│   
│   │   │   <i class="icon-file"></i>build.gradle
│   │   │   <i class="icon-file"></i>build.properties
│	│
│	└───<i class="icon-folder-open"></i>util
│   │   │   <i class="icon-file"></i>build.gradle
│   │   
│	└───<i class="icon-folder-open"></i>wrapper
│       │   <i class="icon-file"></i>gradle-wrapper.jar
│       │   <i class="icon-file"></i>gradle-wrapper.properties
│   
└───<i class="icon-folder-open"></i>lib
    │   <i class="icon-file"></i>ant-salesforce.jar



Prerequisites <i class="icon-cog"></i>
-------------
> - java v8.x.
> - Gradle v4.3


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

