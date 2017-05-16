#BikeSharing360

During our Visual Studio 2017 Launch event this year, Scott Hanselman presented our Docker Tooling experiences. 

This year, we built the technology stack for a fictional company named BikeSharing360, which allows users to rent bikes from one location to another.

BikeSharing360 is a fictitious example of a smart bike sharing system with 10,000 bikes distributed in 650 stations located throughout New York City and Seattle. Their vision is to provide a modern and personalized experience to riders and to run their business with intelligence.

In this demo scenario, we built several apps for both the enterprise and the consumer (bike riders). You can find all other BikeSharing360 repos in the following locations:

* [Mobile Apps](https://github.com/Microsoft/BikeSharing360_MobileApps)
* [Backend Services](https://github.com/Microsoft/BikeSharing360_BackendServices)
* [Websites](https://github.com/Microsoft/BikeSharing360_Websites)
* [Single Container Apps](https://github.com/Microsoft/BikeSharing360_SingleContainer)
* [Multi Container Apps](https://github.com/Microsoft/BikeSharing360_MultiContainer)
* [Cognitive Services Kiosk App](https://github.com/Microsoft/BikeSharing360_CognitiveServicesKioskApp)
* [Azure Bot App](https://github.com/Microsoft/BikeSharing360_BotApps)

# Bikesharing360 Single Container App
In this repo you will find the Single Container demo where Scott opened an existing project, added docker support and published it to Azure App service, running Linux Docker containers.

## Demo Prerequisites
The Single Container demo encompasses taking an existing ASP.NET Core Web App and deploying it to Azure App Services for Linux, using container deployments. To run this demo you'll need:

* An Azure Subscription (see below)
* [Visual Studio 2017 RC](https://www.visualstudio.com/vs/visual-studio-2017-rc/) Choose the **".NET Core & Docker (Preview)"** Workload
* [Docker for Windows](https://www.docker.com/products/docker#/windows) Used to run Docker Containers Locally, including the Linux containers used in this demo.

The creation and publishing to an Azure App Service will be done as part of the demo.   

## How to sign up for Microsoft Azure

To run this demo, you'll need an Azure account. You can:

- Open an Azure account for free [Azure subscription](https://azure.com). You get credits that can be used to try out paid Azure services. Even after the credits are used up, you can keep the account and use free Azure services and features, such as the Web Apps feature in Azure App Service.
- [Activate Visual Studio subscriber benefits](https://www.visualstudio.com/products/visual-studio-dev-essentials-vs). Your Visual Studio subscription gives you credits every month that you can use for paid Azure services.
- Not a Visual Studio subscriber? Get a $25 monthly Azure credit by joining [Visual Studio Dev Essentials](https://www.visualstudio.com/products/visual-studio-dev-essentials-vs).

## Demo Steps

### Open and run the project within a container, making live changes
1. Clone the before docker branch and open this repo locally using Visual Studio 2017
2. Right Click the project and choose **Add** -> **Docker Support**
3. F5 - or click the |> Start Debugging, with Docker as the target
4. Open Views\Home\Index.cshtml
5. Add some text, such as "Come see what we've got" to the end of "...throughout New York City and Seattle." 
6. Save Index.cshtml
7. Refresh the page in the browser
8. Voila, you've now run a .NET Core app in a Linux container and made a change without having to rebuild or re-run the container image.

### Publish to Azure App Services 

1.	Right Click on the project and choose **Publish**
2.	Create a new profile
3.	Choose [Azure App Service Linux (Preview)]
4.	Choose an Azure Subscription you have create rights within
5.	Create a new Resource Group
6.	Name the resource group Marketing_WestUS
7.	Create a new App Service Plan
8.	Set the Location to **West US**. 
9.	*Optionally choose S2 for faster deployments*
10.	 Create a new Azure Container Registry
11.	 Set a DNS Prefix
12.	 Set the Location to **West US**. 
13.	 Click [Create]. This will take a bit of time as the new resource group, registry and Azure App Services are created
14.	 Click [Publish]
15.	 VS will now build the project, push the image the Azure Container Registry and configure Azure App Service to pull the image. Once complete, the browser will launch with your container running in Azure App Service 


## Blogs posts

Here's links to blog posts related to this project:

- Xamarin Blog: [Microsoft Connect(); 2016 Recap](https://blog.xamarin.com/microsoft-connect-2016-recap/)
- The Visual Studio Blog: [Announcing the new Visual Studio for Mac](https://blogs.msdn.microsoft.com/visualstudio/2016/11/16/visual-studio-for-mac/)
- The Visual Studio Blog: [Introducing Visual Studio Mobile Center (Preview)](https://blogs.msdn.microsoft.com/visualstudio/2016/11/16/visual-studio-mobile-center/)
- The Visual Studio Blog: [Visual Studio 2017 Release Candidate](https://blogs.msdn.microsoft.com/visualstudio/2016/11/16/visual-studio-2017-rc/)

## Copyright and license
* Code and documentation copyright 2016 Microsoft Corp. Code released under the [MIT license](https://opensource.org/licenses/MIT).

## Code of Conduct 
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

