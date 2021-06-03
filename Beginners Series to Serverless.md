# Beginners Series to Serverless

## Additional Info

- Youtube playlist: <https://www.youtube.com/playlist?list=PLlrxD0HtieHjU-gOB3ifnFaqikI2kGxUW>

## Table of Contents

01. What is Serverless and why is it so popular now?
02. Core principles of Serverless
03. Use cases of Serverless
04. Create your first Serverless Function using VS Code
05. Walkthrough the directory structure
06. Add Changes to The Generated Function
07. Debug Your Serverless Application
08. Install Node Modules in your Azure Functions application
09. How to set up Azure in VS Code for Deployment
10. Publishing your Serverless Function to Azure
11. Redeploying to Azure after making changes
12. Triggers and Bindings Explained
13. CRON Jobs and Timers with Serverless
14. Connect and read data from MongoDB using Serverless
15. File Uploads with Serverless
16. Using Serverless as API for Static Web Apps

## 01. What is Serverless and why is it so popular now

Serverless - Build application without thinking about servers. (Not thinking about things like runtime, web framework, CPU power, memory, etc).

Serverless examples: FaaS - Functions as a Service

```js
// my_functions_app -> HelloWorld -> index.js

module.exports = async function (context, req) {
    context.res = {
        body: "Hello, World"
    }
}
```

Why Serverless is so popular?

- cheap - only pay for what you use
- easy - much easier to do setup and deploy. Put your code in the cloud and it "just works"
- practical - good for all sorts of applications from microservices to API to one-off business needs

## 02. Core principles of Serverless

Pay as you Go | Event-Driven | Stateless
:--- | :--- | :---
You only pay for what you use | Stand-alone service that communicates with each other and with other applications via events | Your service only runs when they are responding to an event.
how many times + compute resource while running. NEVER pay if a function is not running. | HTTP request, timer, record  added to DB, file  uploaded |  No long-running processes

## 03. Use cases of Serverless

GOOD:

- Serverless is  GOOD for processes that experience low or "burst-able" demand.
- Serverless is GOOD for processes that need to be triggered by other events in our systems.
- Serverless is BAD for operations with predictable, high traffic

APIs:

- traditional WEB APIs that do CRUD operations on a database
- baked into a lot of static web app solutions like Azure Static Web Apps

Image processing:

- Upload an image to Azure Blob Storage
- create a thumbnail for that image

Bots:

- Chatbots
- Auto-reply bots
- Service bots

## 04. Create your first Serverless Function using VS Code

1) Install Azure Functions
2) Create New Project -> Select Sub-directyory -> Python -> HTTP trigger -> `<provide a function name>` -> Anonymous
3) func start
4) <http://localhost:7071/api/products-get?name=your_name>

