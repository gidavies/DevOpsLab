# DevOpsLab

This lab will step through the key elements in setting up a DevOps pipeline for Azure using the DevOps tools for Azure - Visual Studio Team Services (VSTS).

This lab is intended to provide a learning path through the [many existing VSTS labs](https://almvm.azurewebsites.net/), in order to focus on the core DevOps elements.

[What is DevOps?](https://www.visualstudio.com/learn/what-is-devops/)

[How Microsoft does DevOps](https://www.visualstudio.com/learn/devops-at-microsoft/)

# Overall flow

- Setup
- Working with Git
- Continuous Integration
- Create an Azure web app
- Continuous Deployment
- Automated Testing with Selenium
- Monitoring with Application Insights

# Preparing for the lab

For this lab you will require:

- A Visual Studio Team Services account (free)
- An Azure subscription (your own or a free trial)
- Visual Studio 2017 installed (optional)

1. Follow  [these instructions (overview section)](http://almvm.azurewebsites.net/labs/vsts/) to set the above up.
2. Use the [VSTS Demo Generator](http://almvm.azurewebsites.net/labs/vsts/VSTSDemoGenerator/) to create a VSTS project using the My Health Clinic template. Call the project My Health Clinic or something similar.

3. Optional: Create a new Dashboard in VSTS:
- In your VSTS project, select Dashboard and then New:
<img src="images/1.png" width="624"/>

- Name the new Dashboard Lab Progress:
<img src="images/2.png" width="624"/>

- Select the pencil icon in the bottom left, followed by the plus button:
<img src="images/3.png" width="624"/>

- Search for and select the Markdown widget:
<img src="images/4.png" width="624"/>

- Configure the Markdown widget and add the names of your team and any other summary info that might be useful:
<img src="images/5.png" width="624"/>

- Save the changes, close the widget gallery and save the dashboard by clicking on the blue edit button in the bottom right hand corner.


# Lab 1: Working with Git

[This lab](http://almvm.azurewebsites.net/labs/vsts/git/) will introduce you to using Git in VSTS for source control. 

1. Complete [Exercise 1: Cloning a Git repository](http://almvm.azurewebsites.net/labs/vsts/git/#exercise-1-cloning-an-existing-repository) to ensure that you have the project cloned to Visual Studio.
2. If you are new to Git then complete [Exercise 2: Save work with commits](http://almvm.azurewebsites.net/labs/vsts/git/#exercise-2-save-work-with-commits). 
3. Optionally complete:
- [Exercise 3: Review History](http://almvm.azurewebsites.net/labs/vsts/git/#exercise-3-review-history)
- [Exercise 4: Manage Branches from Visual Studio](http://almvm.azurewebsites.net/labs/vsts/git/#exercise-4-manage-branches-from-visual-studio)
- [Exercise 5: Manage branches from the Team Services Portal](http://almvm.azurewebsites.net/labs/vsts/git/#exercise-5-manage-branches-from-the-team-services-portal)
- [Exercise 6: Pull Requests](http://almvm.azurewebsites.net/labs/vsts/git/#exercise-6-pull-requests)
- [Exercise 7: Manage Repositories](http://almvm.azurewebsites.net/labs/vsts/git/#exercise-7-manage-repositories). 
4. Optional: Add a Code Tile to your Lab Progress dashboard:
- Add the Code Tile:
<img src="images/6.png" width="624"/>
- Configure the tile and make sure that the branch is master:
<img src="images/7.png" width="624"/>
- Save the changes, close the widget gallery and save the dashboard by clicking on the blue edit button in the bottom right hand corner.

# Lab 2: Continuous Integration

Continuous Integration is a key DevOps practice to build, test and create the software to later deploy.

1. Complete the [Continuous Integration Lab](http://almvm.azurewebsites.net/labs/vsts/continuousintegration/).
2. Optional: Add a Build History widget to the Lab Progress dashboard by:
- Searching for and adding the build history widget:
<img src="images/8.png" width="624"/>

- Ensuring that it is configured to the build definition created in the preceding steps:
<img src="images/9.png" width="624"/>

- Save the changes, close the widget gallery and save the dashboard by clicking on the blue edit button in the bottom right hand corner.

# Lab 3: Create an Azure Web App

[Azure Web Apps](https://docs.microsoft.com/en-gb/azure/app-service/app-service-web-overview) is an Azure service for hosting web applications. In this lab you'll create the Azure Web App into which you will later deploy the web application.

1. In a browser go to the Azure Portal at http://portal.azure.com.

2. Select Create a resource and enter web app into the search field:
<img src="images/WA-1.png" width="624"/>

3. Press enter and select Web App from the list:
<img src="images/WA-2.png" width="624"/>

4. Click Create:
<img src="images/WA-3.png" width="624"/>

5. Complete the highlighted fields as follows:
<img src="images/WA-4.png" width="800"/>

- App name: Choose a unique name that will be the URL for the web application such as Health plus your initials

- Subscription: If you have more than one subscription, ensure that you choose the correct one for this lab

- Resource Group: Create a new resource group for your web app

- OS: Leave this as the default of Windows.

- App Service Plan/Location: Click on this to create a new App Service Plan. Complete these fields:
    - App Service plan: Enter a name, such as HealthPlan
    - Location: Select an Azure region close to you
    - Pricing tier: Click on this, and select the F1 Free tier
6. Click OK to save the App Service Plan.

7. Click Create to save and create the Web App.

8. After a short time (perhaps 1-2 mins) you should see notification that the Web App has been successfully created. You may want to pin the web app to your Azure dashboard for easy location later on:
<img src="images/WA-5.png" width="624"/>

9. Confirm that your Web App is created by selecting Go to resource.

10. Click on the URL:
<img src="images/WA-6.png" width="624"/>

11. Your Web App should open in the browser and you will see something like this:
<img src="images/WA-7.png" width="624"/>

The exact page details will change over time but this now confirms that you have created a Web App in Azure. In the next lab we will deploy the web application into the newly created Web App.

12. Optional: Add an Embedded Webpage widget to the Lab Progress dashboard by:
- Searching for and adding the Embedded Webpage widget:
<img src="images/WA-8.png" width="624"/>

- Add the URL for your web app created in the preceding steps:
<img src="images/WA-9.png" width="624"/>

- Save the changes, close the widget gallery and save the dashboard by clicking on the blue edit button in the bottom right hand corner.

# Lab 4: Continuous Deployment

Continuous Deployment is another key practice within DevOps to enable to continuous delivery of value (in this example the web application) to end users.

1. Complete the [Continuous Deployment Lab](http://almvm.azurewebsites.net/labs/vsts/continuousdeployment/) following Exercises:

- Exercise 1 (all)

- Exercise 2 (all)

>Note: There is no need to complete Exercise 2 Steps 9 and 10 (replace the database connection string and ConnectionStrings variable plus Azure SQL database creation). The web application can create it's own local database.

- Exercise 3, Task 1 only.

2. Confirm that the continuous deployment pipeline is working:

- Make a code change in Visual Studio (such as adding a comment or a minor UI change),  committing and pushing the change.

- Check the Continuous Integration build gets triggered.

- Once complete the Continuous Deployment should be triggered to deploy the changes into Azure.

3. Optional: Add a Release Definition Overview widget to the Lab Progress dashboard by:
- Searching for and adding the Release Definition Overview widget:
<img src="images/CD-1.png" width="300"/>

- Set the Release Definition to the release created in the lab above:
<img src="images/CD-2.png" width="624"/>

- Save the changes, close the widget gallery and save the dashboard by clicking on the blue edit button in the bottom right hand corner.

# Lab 5: Automated Testing with Selenium

To Do

[Automated Testing with Selenium](http://almvm.azurewebsites.net/labs/vsts/selenium/)

# Lab 6: Monitoring with Application Insights

To Do

[Monitoring with Application Insights](http://almvm.azurewebsites.net/labs/vsts/monitor/)

Other labs (To Do)

ARM

# Other labs 

If you'd like to continue exploring DevOps with VSTS then related labs include:

[Node.js and Express continuous deployment with Visual Studio Team Services and Azure App Service](https://almvm.azurewebsites.net/labs/vsts/nodejs/express/)

[DevOps with Visual Studio Team Services for Java](https://almvm.azurewebsites.net/labs/java/)