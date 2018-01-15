# DevOpsLab

This lab will step through the key elements in setting up a DevOps pipeline for Azure using the DevOps tools for Azure - Visual Studio Team Services (VSTS).

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
2. Use the [VSTS Demo Generator](http://almvm.azurewebsites.net/labs/vsts/VSTSDemoGenerator/) to create a VSTS project using the **My Health Clinic** template. Call the project **My Health Clinic** or something similar.
3. Create a new Dashboard in VSTS:
- In your VSTS project, select **Dashboard** and then **New**:
<img src="images/1.png" width="624"/>

- Name the new Dashboard: Lab Progress:
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
4. Add a Code Tile to your **Lab Progress** dashboard:
- Add the Code Tile:
<img src="images/6.png" width="624"/>
- Configure it and make sure that the branch is **master**
<img src="images/7.png" width="624"/>
- Save the changes, close the widget gallery and save the dashboard by clicking on the blue edit button in the bottom right hand corner.

# Lab 2: Continuous Integration

Continuous Integration is a key DevOps practice to build, test and create the software to later deploy.

1. Follow the [Continuous Integration Lab](http://almvm.azurewebsites.net/labs/vsts/continuousintegration/).
2. Add a **Build History** widget to the **Lab Progress** dashboard by:
- Searching for and adding the build history widget:
<img src="images/8.png" width="624"/>
- Ensuring that it is configured to the build definition created in the preceding steps:
<img src="images/9.png" width="624"/>
- Save the changes, close the widget gallery and save the dashboard by clicking on the blue edit button in the bottom right hand corner.

# Lab 3: Create an Azure Web App

[Create an Azure web app](https://github.com/markharrisonuk/Lab_APIM/blob/master/README.md)

# Lab 4: Continuous Deployment

[Continuous Deployment](http://almvm.azurewebsites.net/labs/vsts/continuousdeployment/)

# Lab 5: Automated Testing with Selenium

[Automated Testing with Selenium](http://almvm.azurewebsites.net/labs/vsts/selenium/)

# Lab 6: Monitoring with Application Insights

[Monitoring with Application Insights](http://almvm.azurewebsites.net/labs/vsts/monitor/)
