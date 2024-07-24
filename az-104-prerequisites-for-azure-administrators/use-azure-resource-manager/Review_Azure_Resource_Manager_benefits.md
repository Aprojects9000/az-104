# Review Azure Resource Manager benefits

    Note: Each of these MD files is a copy of the related Microsoft Learn page. It is not copy pasted, instead it is copied word for word, altered here and there, and expanded on to help me better learn the information. 

The infrastructure for your application is typically made up of many components e.g., a virtual machine, storage account, and virtual network. Maybe a web app, database, database server, and third-party services. These components are not separate entities, instead they are related and interdependent parts of a single entity. You want to deploy, manage, and monitor them as a group. 

Azure Resource Manager enables you to work with the resources in your solution as a group. You can deploy, update, or delete all the resources for your solution in a single, coordinated operation. You use a template for deployment and that template can work for different environments such as testing, staging, and production. Azure Resource Manager provides security, auditing, and tagging features to help you manage your resources after deployment.

**Consistent management layer**

Azure Resource Manager provides a consistent management layer to perform tasks through Azure PowerShell, Azure CLI, Azure portal, REST API, and client SDKs. Choose the tools and APIs that work best for you.

The following image shows how all the tools interact with the same Azure Resource Manager API. The API passes requests to the Azure Resource Manager service, which authenticates and authorises the requests. Azure Resource Manager then routes the requests to the appropriate resource providers.  
![image1](images/1.png)

**Benefits**

Azure Resource Manager provides several benefits:

-   You can deploy, manage, and monitor all the resources for your solution as a group, rather than handling all these resources individually.
-   You can repeatedly deploy your solution throughout the development lifecycle and have confidence your resources are deployed in a consistent state.
-   You can manage your infrastructure through declarative templates rather than scripts. 
-   You can define the dependencies between resources so they're deployed in the correct order.
-   You can apply access control to all services in your resource group because Role-Based Access Control (RBAC) is natively integrated into the management platform.
-   You can apply tags to resources to logically organise all the resources in your subscription.
-   You can clarify your organisation's billing by viewing costs for a group of resources sharing the same tag.
  
**Guidance**

The following suggestions help you take full advantage of the Azure Resource Manager when working with your solutions.

-   Define and deploy your infrastructure through the declarative syntax in Azure Resource Manager templates, rather than through imperative commands.
-   Define all deployment and configuration steps in the template. You should have no manual steps for setting up your solution.
-   Run imperative commands to manage your resources, such as to start or stop an app or machine.
-   Arrange resources with the same lifecycle in a resource group. Use tags for all other organising of resources.

## Key-terms

**Azure PowerShell:** A command shell designed for managing and administering Azure resources from the command line. PowerShell itself is also the scripting language for the majority of Windows operating systems. In comparison, you have Bash being a Unix shell and scripting language for most Linux operating systems.

**Azure Command-Line Interface (CLI):** A set of commands used to create and manage Azure resources. Similar in a way to PowerShell, but their functionality is different. CLI can be seen as a simplified and limited version of PowerShell.

**Azure portal:** A web-based, unified console with which you can create and manage all your Azure resources. It can do what PowerShell can, but by using a graphical user interface.  

**Application Programming Interface (API):** A set of definitions and protocols for building and integrating application software. It is a way of interacting with a computer or system to retrieve information or perform a function. You can think of an API as a mediator between the users or clients and the resources or web services they want to get. 

**Representational State Transfer (REST):** REST is a set of architectural constraints, not a protocol or a standard. Through it (a RESTful API), a representation of the state of a resource can be transferred from the resource to the requester or endpoint. REST is a set of guidelines that can be implemented as needed.

**REST API:** An application programming interface (API or web API) that conforms to the constraints of REST architectural style and allows for interaction with RESTful web services. 

**Software Development Kit (SDK):** Also known as a devkit, an SDK is a set of software-building tools for a specific platform, including the building blocks, debuggers and, often, a framework or group of code libraries such as a set of routines specific to an operating system (OS).
Often, at least one API is also included in the SDK because without the API, applications can't relay information and work together. The difference between an SDK and an API is that an SDK is the complete kit. They go beyond facilitation (though they include it) to provide everything for building new software for a specific platform or programming language. 

**Client SDKs:** A client-side SDK is designed to be used in applications that your users run directly on their own devices, such as mobile, desktop and web applications. They are optimised to be used by a single user and low-bandwidth consumption. Examples: JavaScript Library, Angular, and React SDKs.

**Microsoft Azure Solutions:** Microsoft Azure Solutions refers to a suite of cloud computing services offered by Microsoft through its Azure platform. These solutions encompass a wide range of services, including infrastructure as a service (IaaS), platform as a service (PaaS), and software as a service (SaaS). Azure provides businesses with tools for building, deploying, and managing applications and services through Microsoft's global network of data centers.
Azure Solutions cover various domains such as computing, storage, networking, databases, analytics, artificial intelligence (AI), Internet of Things (IoT), security, and more.

**Azure Infrastructure:** Azure infrastructure encompasses essential compute, storage, and networking resources that lets you bypass the cost and complexity of buying and managing physical servers and datacenter infrastructure. It does this through IaaS (Infrastructure as a Service).

**ARM templates:** Azure Resource Manager (ARM) templates, declarative by design, is an infrastructure as code (IaC) solution. In code, you define the infrastructure that needs to be deployed. This code can then be used repeatedly as much as is necessary. The template uses declarative syntax, which lets you state what you intend to deploy without having to write the sequence of programming commands to create it. 
A new language ['Bicep'](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview?tabs=bicep) has been created that offers the same capabilities as ARM templates but with a syntax that's easier to use. 

**Scripts:** In computer programming, a script is a program or sequence of instructions that is interpreted or carried out by another program rather than by the computer processor (as a compiled program is). In general, script languages are easier and faster to code in than the more structured and compiled languages such as C and C++. However, a script takes longer to run than a compiled program since each instruction is being handled by another program first (requiring additional instructions) rather than directly by the basic instruction processor.

**Azure Role-Based Access Control (RBAC):** Azure role-based access control (Azure RBAC) helps you manage who has access to Azure resources, what they can do with those resources, and what areas they have access to. It is an authorisation system built on Azure Resource Manager that provides fine-grained access management to Azure resources. 

**Azure Tags:** Azure tags are metadata elements that you apply to your Azure resources. They're key-value pairs that help you identify resources based on settings that are relevant to your organisation. If you want to track the deployment environment for your resources, add a key named ```Environment```. To identify the resources deployed to production, give them a value of ```Production```. The full key-value pair is ```Environment = Production```.

**Azure Resources:** Azure resources are manageable items that are available through Azure. Virtual machines, storage accounts, web apps, databases, and virtual networks are examples of resources. Resource groups, subscriptions, management groups, and tags are also examples of resources

**Azure Subscription:** An Azure subscription is an agreement with Microsoft to use one or more Microsoft cloud platforms or services, for which charges accrue based on either a per-user license fee or on cloud-based resource consumption

**Declarative syntax:** Used in declarative programming. It is syntax that writes your code in such a way that it describes what you want to do, and not how you want it to do. It is left up to the compiler to figure out the how. 

**Imperative commands:** Used in imperative programming. They are commands that you use to write your code in such a way that it describes how to do what you want the code to do, and not what you want it to do.


### Used sources
[1. What is Azure PowerShell?](https://learn.microsoft.com/en-us/powershell/azure/get-started-azureps?view=azps-12.1.0)

[2. What is Azure CLI?](https://learn.microsoft.com/en-us/cli/azure/)

[3. Azure PowerShell vs CLI](https://www.msp360.com/resources/blog/azure-cli-vs-powershell/)

[4. What is Azure portal?](https://learn.microsoft.com/en-us/azure/azure-portal/azure-portal-overview)

[5. What is an API, REST, and a REST API?](https://www.redhat.com/en/topics/api/what-is-a-rest-api)

[6. What is an SDK?](https://www.ibm.com/think/topics/api-vs-sdk)

[7. What is a Client SDK?](https://docs.unlaunch.io/docs/sdks/client-vs-server-side-sdks#:~:text=Client%2Dside%20SDKs%20are%20designed,%2C%20Angular%2C%20and%20React%20SDKs.)

[8. What are Microsoft Azure Solutions?](https://www.savictech.com/azure-solution.php#:~:text=Azure%20Solutions%20cover%20various%20domains,%29%2C%20security%2C%20and%20more.)

[9. What is Azure Infrastructure, or infrastructure as a service (IaaS)?](https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-iaas)

[10. What are ARM (Azure Resource Manager) templates?](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/overview)

[11. What is a script?](https://www.techtarget.com/whatis/definition/script#:~:text=1%29%20In%20computer%20programming%2C%20a,as%20a%20compiled%20program%20is%29.)

[12. What is Azure role based access control (RBAC)?](https://learn.microsoft.com/en-us/azure/role-based-access-control/overview)

[13. What are Azure tags?](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/tag-resources)

[14. What are Azure resources? (first term under terminology)](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview)

[15. What is an Azure Subscription?](https://learn.microsoft.com/en-us/microsoft-365/enterprise/subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings?view=o365-worldwide)

[16. What is declarative syntax?](https://stackoverflow.com/questions/129628/what-is-declarative-programming)

[17. What is an imperative command?](https://en.wikipedia.org/wiki/Imperative_programming)


