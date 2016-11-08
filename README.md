---
services: Cloud-Services
platforms: .Net
author: msonecode
---

# Host Multiple Websites within One Azure WebRole using VisualStudio 2015

##Introduction
An example of how to host multiple websites within one Azure webrole using Visual Studio 2015. This is a supplement and implement of Azure official video: [Multiple Websites in a Web Role](https://channel9.msdn.com/Shows/Cloud+Cover/Cloud-Cover-Episode-37-Multiple-Websites-in-a-Web-Role).  Because that post is dated 2011, maybe updates for the past years allows for a more friendly and better approach. This post will give you the latest version of implementation.
<br/>
Video guide,<br/>
https://channel9.msdn.com/Shows/Cloud+Cover/Cloud-Cover-Episode-37-Multiple-Websites-in-a-Web-Role
<br/>
Text guide,<br/>
http://www.wadewegner.com/2011/02/running-multiple-websites-in-a-windows-azure-web-role/

## Prerequisites

***1. Azure Account***
<br/>
You need an Azure account. You can [open a free Azure account](https://azure.microsoft.com/pricing/free-trial/?WT.mc_id=A261C142F) or [Activate Visual Studio subscriber benefits](https://azure.microsoft.com/pricing/member-offers/msdn-benefits-details/?WT.mc_id=A261C142F).

***2. Visual Studio 2015***
<br/>
https://www.visualstudio.com/downloads/

***3. ASP.NET MVC 5***
<br/>
The tutorial assumes you have worked with ASP.NET MVC and Visual Studio. If you need an introduction, see [Getting Started with ASP.NET MVC 5](http://www.asp.net/mvc/overview/getting-started/introduction/getting-started).

***4. Azure SDK***
<br/>
The tutorial is written for Visual Studio 2015 with the [Azure SDK for .NET 2.9](https://azure.microsoft.com/en-us/documentation/articles/dotnet-sdk/) or later.
[Download the latest Azure SDK for Visual Studio 2015](http://go.microsoft.com/fwlink/?linkid=518003). The SDK installs Visual Studio 2015 if you don't already have it.

## Run the sample
1.	Please first download my test VS solution MultipleWebSite.zip for your reference.
2.	After you downloaded, please unzip it and open the main “MultiWebsitesOneWebRole” solution as Administrator.
Switch to ServiceDefinition.csdef file, replace the highlight parts as your actual path.
<img src="https://github.com/zhangdingsong/AzureMultipleWebsitesOneWebrole/blob/master/2.jpg">
3.	Add below info into your host file.
<img src="https://github.com/zhangdingsong/AzureMultipleWebsitesOneWebrole/blob/master/3.jpg">
4.	Ping to check if the dns name can be used.
<img src="https://github.com/zhangdingsong/AzureMultipleWebsitesOneWebrole/blob/master/4.jpg">
5.	Run the solution, and visit three websites.
<img src="https://github.com/zhangdingsong/AzureMultipleWebsitesOneWebrole/blob/master/1.jpg">

Reference:
Below are some useful links, you will need them before your real action.

[Some notes that you might need to know when you start to deploy your websites]
How to setting up CNAMEs for your domain:
http://blog.smarx.com/posts/custom-domain-names-in-windows-azure

Tips for Publishing Multiple Sites in a Web Role:
https://michaelcollier.wordpress.com/2013/01/14/multiple-sites-in-a-web-role/
https://kellyhpdx.wordpress.com/2012/04/11/deploying-multiple-web-applications-to-a-single-azure-instance-and-applying-web-config-transforms-correctly/
https://www.intertech.com/Blog/windows-azure-multiple-web-sites/
https://blog.bareweb.eu/2011/01/11/azure-running-multiple-web-sites-in-a-single-webrole/
http://www.structuretoobig.com/post/2012/01/17/One-Azure-Web-Role-Multiple-Websites.aspx
http://weblogs.asp.net/gunnarpeipman/deploying-independent-web-applications-to-windows-azure-using-single-web-role
http://stackoverflow.com/questions/21796881/multiple-sites-within-one-azure-webrole

How to configure the Azure Cloud Service Project to compile all the associated webs within a single web role:
http://stackoverflow.com/questions/15536819/azure-web-role-multiple-websites-dont-compile-when-debugger-is-run-in-visual

