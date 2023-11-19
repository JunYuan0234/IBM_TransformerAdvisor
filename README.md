# IBM Cloud Transformation Advisor

This documentation will delve into the advantages, practical applications, and business value of IBM Cloud Transformation Advisor (TA). It aims to elaborate on and showcase the capabilities of TA, illustrating its potential benefits through detailed exploration of use cases and demonstrations.

- IBM Cloud Transformation Advisor (TA) is a vital application modernization tool within IBM WebSphere Hybrid Edition (WSHE).
- It enables rapid evaluation of on-premises Java EE applications for seamless cloud deployment.

- Key capabilities include identifying Java EE programming models in the app and determining app complexity through content and structure inventory.

- TA highlights Java EE programming model and WebSphere API differences across various WebSphere profile types.

- It identifies potential Java EE specification implementation differences that may impact the application.

- Additionally, TA recommends the optimal IBM WebSphere Application Server edition, offering advice, best practices, and potential solutions.

- The tool streamlines the application migration process to the cloud, minimizing errors and risks.

- TA significantly reduces time to market, making it a valuable asset for organizations seeking a smooth transition.

This documentation includes the following **steps**:

- Step 1: Establish a Transformation Advisor Workspace and Collection.

- Step 2: Download the Data Collector to gather necessary information.

- Step 3: Upload the results obtained from running the Data Collector.

- Step 4: Dive into the analysis phase to review and understand the recommendations provided.

- Step 5: Migration Demonstration

## Step 1 : Establish a Transformation Advisor Workspace and Collection.

In this demo journey, the objective is to leverage Transformation Advisor for a meticulous assessment of migration effort. The focal point is the transition of Customer Order Services application from the conventional WebSphere V 8.5.5 to a modern, cloud-ready runtime with minimal adjustments to the existing code. To initiate the utilization of Transformation Advisor (TA), the initial step involves the creation of a Workspace and Collection.

Think of a Workspace as a dedicated zone that encapsulates the migration recommendations provided by Transformation Advisor, tailored to each application server environment. The flexibility here lies in the ability to name and structure these Workspaces in alignment with personal preferences—whether it's based on business applications, geographical locations, or specific teams. On the TA homepage, I navigate to the 'Create new' button to establish a fresh Workspace explicitly named "CustomerOrderServices" for the purpose of this demo.

Furthermore, within each Workspace, there is the option to further compartmentalize the process by creating collections, allowing for a more targeted and nuanced approach to assessment and planning. Similar to Workspaces, these collections can be named and organized according to our discretion. In this demonstration, a Collection named "WAS855_AppSrv01" is formed, serving as the focus group for a more detailed and streamlined evaluation and planning process.

![Initial landing Page](/Image/1.jpeg)

1. The image above shows the initial landing page of the Transformation Advisor on OpenShift container platform. You can choose your login option and in this demo, htpasswd is used for login.

![Initial landing Page](/Image/2.png)

2. Fill in the tab with login credential of username and password to login into IBM Transformer Advisor.

![Initial landing Page](/Image/3.png)

3. Successfully authenticating login credential will leads to the IBM Transformation Advisor home page. Clicking on the create new button will allows the user to create a new workspace in IBM Transformation Advisor.

![Initial landing Page](/Image/4.png)

4. Enter a Workspace name as *CustomerOrderService* and click Next.

![Initial landing Page](/Image/5.png)

5. Enter a Collection name as *WAS855_AppSrv01* and click Create.

![Initial landing Page](/Image/6.png)

6. Once the workshop is created, the IBM Transformation Advisor will be ready to use as shown on the image above.

Within the TA collection page, you'll find two key tools: the Data Collector utility and the Data Uploader utility. The Data Collector utility, accessible from the Transformation Advisor web page, serves the purpose of retrieving application data from the Java application server operating in the client's environment. This Java utility can be effortlessly downloaded and executed against our Java application server, facilitating the comprehensive collection of all pertinent application data.

Upon running the utility, there are two options for managing the collected data. If Transformation Advisor (TA) is within the same network as the application server, the utility can seamlessly send the data directly back to TA. Alternatively, the utility also stores the collected data in a zip file, providing the convenience of uploading this file to a remote TA using the Data Uploader utility. This dual functionality ensures flexibility and accessibility in handling the collected application data based on the specific network configuration and requirements.

## STEP 2 : Download the Data Collector to gather necessary information.

Once the Workspace and Collection setup is complete, The page presented with the choice of either downloading the Data Collector utility or uploading an existing data file. In this demonstration, I'll walk through the process of using the Data Collector utility. To start, navigate to the download page where various versions of the utility are available, tailored to different application server operating systems such as WebSphere, WebLogic, and Tomcat.

Upon selecting the appropriate version, download the utility and save it locally on my workstation. This action results in a file named something like "transformationadvisor-Linux_CustomerOrderServices_WAS855_AppSrv01.tgz," which is stored in the local download directory. Following this, copy the command for extracting the Data Collector tar file from the Transformation Advisor download page.

Executing this command in the terminal window, located in the "Downloads" directory, leads to the successful extraction of the Data Collector. The extracted files are now stored in the "Downloads" directory. Using the 'cd' command, navigate to the directory, preparing anad stand-by for the subsequent step of running the Data Collector tool.

![Initial landing Page](/Image/7.png)

1. After landing on the TA Home Page, clicking on the blue "Download" button will lead to the page shown on the image above.

![Initial landing Page](/Image/8.png)

2. By clicking on the drop down box, a few selection of operating system will be display for selection depending on the operating system the device currently running for the relavent data collector to be installed. In this demo, Linux will be choosen as the operating system are running on Linux.

![Initial landing Page](/Image/9.png)

3. Then, clicking on the Download button below will trigger the system to download the file to the local system.

![Initial landing Page](/Image/10.png)

4. A system pop up will be displayed, select Save File option then click ok will starts the download process.

![Initial landing Page](/Image/11.png)

5. Click on the copy icon as shown above on the image.
 
![Initial landing Page](/Image/12.png)

6. After the download process is successfully completed, open your local terminal if Linux or MacOS / Command Prompt if Windows and direct to the location of the downloaded file located. Then, paste the code copied on the previous steps to the terminal and press enter for it to run.

![Initial landing Page](/Image/13.png)

7. The above images shows the successful extraction of the Transformer Advisor Data Collector utility to the Downloads Directory. 

![Initial landing Page](/Image/14.png)

8. With the successful installation of the Data Collector, it is ready to execute it against my application server. The Transformation Advisor Data Collector Download page offers comprehensive guidance on running the tool. Notably, the Data Collector is versatile, capable of gathering data from various application server runtimes such as WebSphere, WebLogic, JBoss, Tomcat, and MQ. Additionally, the Transformation Advisor Data Collector provides the flexibility to narrow the scope of analysis at different levels, including application and configuration, application only, or ear/war files.

## STEP 3: Upload the results obtained from running the Data Collector.

Transformation Advisor undergoes regular updates, incorporating insights gathered from the field. Simultaneously, Liberty continues to enhance its capabilities, further simplifying the migration process. Consequently, it is advisable to consistently utilize the latest Transformation Advisor collector when initiating a new collection. It's important to note that the execution of the collector may entail a certain duration to generate the required zip file.

Therefore in this demonstration, a pre-created Data Collector zip file is used to upload to IBM Transformation Advisor by utilising the Transformation Advisor Upload utility feature to upload the file.After a few moment of uploading waiting time, the upload of the data collector results will be successfully completed. Once the Data Collector Results are uploaded to Transformation Advisor, a set of recommendations will be generated and displayed on the Recommendations page.

![Initial landing Page](/Image/15.png)

1. Navigate back to the WAS855_AppSrv01 directory as shown on the image above.

![Initial landing Page](/Image/16.png)

2. Then, click on the grey button which shows upload on it to upload data collector zip file.

![Initial landing Page](/Image/17.png)

3. Click on the "Drop or add file" to upload the file from local directory.

![Initial landing Page](/Image/18.png)

4. After located and added the zip file, click on the upload button to upload the file to Transformation Advisor.

![Initial landing Page](/Image/19.png)

5. After successfully uploading the Data Collector Results to Transformation Advisor, a series of recommendations will be generated and displayed on the Recommendations page, as shown on the image above.

On the Recommendations page, the identified migration source environment is presented in the Profile section, while the target environment is specified in the Migration Target section. The data collector tool recognizes the source environment as our WebSphere Application Server Traditional runtime with a WAS 8.5.5.20 AppSrv01 profile. The target environment is configured for Liberty Runtimes, serving as the default target environment.

The Recommendations page further provides a comprehensive summary analysis of all applications in the AppSrv01 environment slated for migration to a Liberty environment. Each application's details include its Name, Migration Target, Complexity, Issues, and the Estimated development cost in days.

For instance, considering the modresorts application's transition to a Liberty runtime, the complexity level is categorized as Simple, indicating that no modifications to the application code are required for migration. Consequently, the estimated development effort is zero days.

Notably, the recommendation page showcases both Open Liberty and WebSphere Liberty as migration targets for the CustomerOrderServicesApp. A detailed explanation for this dual recommendation will be provided later in the presentation.

## STEP 4 : Dive into the analysis phase to review and understand the recommendations provided.

### Open Liberty

Now, let's direct our attention to the recommendations provided by Transformation Advisor specifically for the Customer Order Services application (CustomerOrderServicesApp.ear). According to Transformation Advisor's assessment, the projected effort required to migrate the Customer Order Services application from the traditional WebSphere V855 to Open Liberty (which accommodates JEE7, Java EE 8, and additional features) is estimated at 8 days of development time. To delve deeper into the analysis, let's examine the specific details pertaining to the Customer Order Services application.

![Initial landing Page](/Image/21.png)

1. At the recommendation page, click on the "CustomerOrderServicesApp.ear" with the migration target of Open Liberty.

![Initial landing Page](/Image/22.png)

2. Scroll down from the page to browse through "Complexity Rules". Initially, our focus is on reviewing the analysis outcomes within the Complexity Rules section. Notably, Transformation Advisor has identified that there might be a necessity for code modifications before the Customer Order Services application can successfully operate on Open Liberty.

![Initial landing Page](/Image/23.png)

3. Proceed to scroll down to access the detailed information in the Issues section. Additionally, open the sections for External Dependencies and Additional Information.

On to the Issues Details section, Transformation Advisor has identified a critical technology issue related to accessing Apache Wink APIs and multiple issues concerning JPA. In the External Dependencies section, it's noted that the application relies on accessing a database and Java EE security.

![Initial landing Page](/Image/24.png)

Towards the end of the details page, Transformation Advisor furnishes three reports containing additional analysis results, encompassing:

Technology Report: This report offers insights into which IBM platforms support the technologies utilized by the applications.

Inventory Report: Providing a high-level inventory of each application's content and structure, this report also highlights information on potential deployment challenges and performance considerations.

Analysis Report: This report outlines potential issues, their severity, and suggests possible solutions.

![Initial landing Page](/Image/n1.png)

4. The image above initiate the examination of Technology Report, which opens a new browser window displaying the Application Technology Evaluation Report. This report provides a comprehensive list of Java technologies utilized by the application, indicating whether these technologies are supported by specific runtimes, ranging from Open Liberty to WebSphere traditional for z/OS. The information presented in this report plays a crucial role in assessing the suitability of a particular WebSphere product for the analyzed application.

![Initial landing Page](/Image/n2.png)
![Initial landing Page](/Image/n3.png)
![Initial landing Page](/Image/n4.png)
![Initial landing Page](/Image/n5.png)
![Initial landing Page](/Image/n6.png)

5. Go back to the Transformation Advisor page, scroll to the bottom of the analysis pageand click on the Inventory Report link, then you will be able to scroll through the images similar as above. Then, we turn our attention to the Inventory Report, offering valuable insights into the application's structure, potential deployment issues, and additional details.

![Initial landing Page](/Image/25.png)

6. Go back to the Transformation Advisor page, scroll to the bottom of the analysis page and click on the Analysis Report link. Then, click on OK to open the report in a new tab.

![Initial landing Page](/Image/n7.png)
![Initial landing Page](/Image/image.png)
![Initial landing Page](/Image/26.png)

7.  Finally, let's explore the Analysis Report. This report showcases the outcomes of the migration rules executed by the Data Collector and the corresponding results.

Now, navigate to the Severe Rules section and review the details provided in the Show rule help section. Here, the Rule Help section offers recommended solutions for addressing the identified issues.

Within this section, various recommendations are outlined, including:

- The unavailability of Apache Wink Client APIs and org.codehaus.jackson packages: The suggestion is to utilize standard javax.ws.rs.client APIs where possible or package the API with the application, as the org.apache.wink.client packages are not accessible to JAX-RS applications using the WAS Java EE 7 JAX-RS 2.0 implementation. Similar adjustments are required for org.codehaus.jackson packages.
 
- Disabling the persistence unit second-level cache and migrating OpenJPA and WebSphere JPA configuration properties: Given that Open Liberty doesn't support JPA 2.0, which implements OpenJPA, the recommendation is to migrate to JPA 2.1, implementing EclipseLink JPA. This transition introduces several changes in the JPA configuration, which are detailed in the provided documentation.

### WebSphere Liberty

![Initial landing Page](/Image/19.png)

1. Go back to the Recommendation page as shown on the image above and click the CustomerOrderServicesApp.ear application name on the WebSphere Liberty row.

![Initial landing Page](/Image/27.png)

2. Let's focus on the Transformation Advisor recommendations specific to the Customer Order Services (CustomerOrderServicesApp.ear) application concerning WebSphere Liberty. According to Transformation Advisor's estimation, the effort required to migrate this application from traditional WebSphere V855 to WebSphere Liberty (which supports JEE6 partly, Java EE 7 and 8, and more) is estimate to take 0.5 days of development time. Now, let's examine the analysis details for the Customer Order Services application to understand why the migration efforts for WebSphere Liberty are less than those for Open Liberty. 

![Initial landing Page](/Image/Picture1.png)

3. Initially, we turn our attention to the Complexity Rules section. Here, Transformation Advisor has determined that code changes may be necessary for the application to run on WebSphere Liberty.

![Initial landing Page](/Image/Picture2.png)

4. However, upon moving to the Issues Details section, we observe that Transformation Advisor has only detected a critical technology issue related to accessing Apache Wink APIs. Unlike Open Liberty, there are no issues regarding JPA, as WebSphere Liberty supports JPA 2.0 and, Open JPA.

![Initial landing Page](/Image/28.png)
![Initial landing Page](/Image/29.png)

5. Go back to the Transformation Advisor page, scroll to the bottom of the analysis page and click on the Analysis Report link. Then click on OK on the pop up window.

While both WebSphere Liberty and Open Liberty share some similarities, the Technology Report differs between them. To gain more insights, we proceed to the Analysis Report. This report provides the outcomes of the migration rules executed by the Data Collector.

Scrolling down to the Severe Rules section within the Analysis Report, we review the Show Rule Help details. The Rule Help section offers recommended solutions for addressing the identified issue. In this section, there is only one recommendation listed:

The use of system-provided Apache Wink APIs requires configuration: To utilize system-provided third-party APIs in Liberty applications, configuration is necessary to include these APIs. In WebSphere Application Server traditional, these APIs are available without configuration. This change is configuration-only and can be implemented by using a classloader definition in the Liberty server.xml file.

## Step 5: Migration Demonstration

### Websphere Liberty

![Initial landing Page](/Image/30.png)

1. Go back to the Transformation Advisor page, scroll to the top and click on the button View migration plan. In addition to migration recommendations, Transformation Advisor offers assets to expedite deployment by providing a migration plan. This plan includes the generation of various assets such as the Liberty configuration file (server.xml) for deploying the application to Liberty, a pom file for building the application, a Docker file for containerizing the application, and an Application Custom Resource for deploying the application to Kubernetes.

![Initial landing Page](/Image/31.png)

2. Review the migration assets then click on the server.xml.

![Initial landing Page](/Image/32.png)
![Initial landing Page](/Image/33.png)

3. Let's begin with the Liberty configuration. Transformation Advisor leverages the analysis of the application EAR to generate a list of features required by the application. As the collector not only scrutinizes the application but also its configuration, it generates the Liberty configuration definition for the datasource. To enhance the portability of the application configuration, Transformation Advisor utilizes environment variables for many aspects of the configuration, injecting values retrieved from the current environment.

It's important to note that Transformation Advisor does not collect any passwords. Therefore, the variables for the datasource and keystore do not contain any credentials. This approach ensures security by avoiding the storage or transmission of sensitive information.

### Traditionla WAS

![Initial landing Page](/Image/34.png)

1. Go back to the Transformation Advisor overview page. Then, change the migration target to Compatible runtimes.

![Initial landing Page](/Image/35.png)

2. Click the CustomerOrderServicesApp.ear application name on the WebSphere traditional row.

![Initial landing Page](/Image/36.png)

3. The Inventory Report, Analysis Report and Technology Report are also available for Traditional WAS. For the CustomerOrderService application, migrating to WebSphere Liberty appears relatively straightforward. However, there may be reasons to consider sticking with WebSphere traditional and containerizing the application. Transformation Advisor offers valuable insights to evaluate the efforts required for migration to a WebSphere traditional v9 container. It provides a similar set of reports as it does for Liberty.

![Initial landing Page](/Image/37.png)
![Initial landing Page](/Image/38.png)
![Initial landing Page](/Image/39.png)

4. Scroll up to the top of the page and click on the button View migration plan. Additionally, Transformation Advisor goes a step further by providing assets specifically tailored for deploying the application into a WebSphere traditional v9 container. These assets include Python scripts to configure WebSphere traditional, deploy the application, a Dockerfile for deploying the application into WebSphere traditional within a container, and Pipeline resources. These resources are designed to streamline and facilitate the deployment process, offering a comprehensive set of tools for efficient migration and containerization within the WebSphere traditional environment.

## Summary

The demonstration illustrated the process of evaluating an existing Java application using IBM Cloud Transformation Advisor. The primary goal in our scenario of migrating from traditional WebSphere V855 to Liberty is to transition the Customer Order Services application to a cloud-ready new runtime with minimal code changes. Utilizing IBM Cloud Transformation Advisor, we conducted an in-depth analysis of the application's compatibility with traditional WebSphere. The outcome indicated that only minor modifications to three classes would be necessary. In addition to providing insights into the application, Transformation Advisor also furnished various deployment assets.

As demonstrated, Transformation Advisor proves instrumental in expediting the application migration to the cloud, minimizing errors and risks, and significantly reducing time to market. The tool streamlines the process and enhances the efficiency of migrating applications to new runtimes, contributing to a smoother transition to cloud environments.













