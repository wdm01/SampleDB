# 🕮 Azure Bootcamp Overview & Goals
⮩ Gain an understanding of the full Azure DevOps lifecycle
>- Agile Planning
>- Version Control
>- Continuous Integration
>- Continuous Deployment
>- Infrastructure as Code

⮩ We want to do this with as few external dependencies as possible <br>
⮩ Discuss some of the challenges specific to Data Engineering projects  <br>
⮩ Talk about alternates to Azure DevOps that we might encounter  <br>


<br><br><br>


# 🗐 Setup

## Azure DevOps Subscription
In order to create a subscription, you need an azure account. If you don't currently have one, you will need to sign up at [portal.azure.com](portal.azure.com). If you have a Visual Studio Professional or higher subscription level, you may be able to take advantage of free subbscription credits.

- Navigate to [Dev Ops Organizations](https://aex.dev.azure.com/me?mkt=en-US).  
- Find the `Create new organization` button and create a new one. <br>
*If you are already an admin of an Organization and wish to use that, feel free to do so.*
- Create a new project
Under **Advanced**: <br> Choose **Git** as the version control and **Agile** as the template.
 *(naming doesn't matter for this walk-through)*

<br> 


## Azure Resource Manager Service Connection
- Go to your project `Setting` > `Service Connections` > `New Service Connection`
- Choose the following properties:
	- **Connection Type:** Azure Resource Manager
	- **Authentication Method:** Service Principal (automatic)
	- **Scope Level:** Subscription
	- **Resource Group:** (leave this blank)
	- **Service Connection Name:** servCon1
	- **Security:** Grant access to all pipelines


<br> 



## Initialize Source Control Repository
- This [github repo](https://github.com/wdm01/SampleDB) contains all of the files needed for this walkthrough.
- Go to `Repos` > `Files` 
Under **"Import a repository"** choose `Import` and paste the following: <br> https://github.com/wdm01/SampleDB.git in the flyout panel

<br>
We will eventually need the following variables mapped in our pipeline:

>**adminUser** = bootcamp123 <br>
**serverName** = myServerNameHere <br>
**adminPass** = TempPa$$wordOrWhateverYouWantHere <br>
**azureResourceManagerConnection** = servCon1 <br>
**subscriptionId** = [found here](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) <br>
**resourceGroupName** = whatever-you-want-rg <br>
	
<br><br><br>

# 🗐 Agile Planning 
> The purpose of this  section is to get us aquainted with how we manage project requirement within Azure DevOps. Along the way we will be creating work items that will be leveraged in later sections.
- Setting the Process Type
- Defining Sprints and Areas
- Setting Capacity
- Determining a Story Point strategy
- Creating Backlog items
- Creating Task items
- Understanding Columns & States
- Swimlanes, Tags and Column Splitting for added organization
- Leveraging the Burndown Chart

<br><br><br>

# 🗐 Version Control
- Repository Hosting
- git vs TFVC
- Utilizing Branches
- Setting Branch Policies
- Creating Pull Requests


<br><br><br>

# 🗐 Continuous Integration
- Pipelines (classic vs YAML)
- Advantages of using YAML Pipelines
- Designing your pipeline (multi-build, multi-stage, etc.)
- Utilizing Artifacts
- Defining pipeline variables


<br><br><br>

# 🗐 Continuous Deployment
- Running your pipeline manually
- Triggering our pipeline via a trigger
- Conditional Stages

<br><br><br>

# 🗐 Infrastructure as Code
- Utilize ARM templates
- Alternatives to ARM (Chef, Puppet, Terraform, etc.)
- Desired State Configuration (DSC) & Idempotence in deployments
