# Up and running with Azure Functions and Docker

This is a simple project to get an Azure function running inside a Docker container.
You may want to check my [Medium](https://medium.com/@nsoria/up-and-running-with-azure-functions-docker-containters-4e0db076b6a6) This Readme file will have only the main information.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* [Node.js](https://nodejs.org/en/download/) - Version 8.5 or higher
* [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-windows?view=azure-cli-latest)
* [.NET Core SDK 2.1](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.200-windows-x64-installer)
* [Azure Functions Core Tools v2](https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local#v2)
* [Docker](https://store.docker.com/editions/community/docker-ce-desktop-windows)
* Coffee and good music

Disclaimer: I used Windows 10 Pro for this demostration, but can be replicated on Ubuntu 16.04 or higher. Steps may differ.

## Running the tests

Step 1: Initialize an Azure function.
This tutorial was done choosing node.js

  Initialize Azure Docker function.
  func init . --docker

Step 2: Create a new function
This tutorial was done choosing HTTP trigger template.

  Create a new function
  func new

Step 3: Build and run the container!
  Build a docker container
  docker build -t azurefuntiondemo .

  Run docker container
  docker run -p 8080:80 azurefunctiondemo

Step 4: Check your progress!
Check link http://localhost:8080 to validate your function is up and running.

## Authors

* **Nicolás Soria** - [PurpleBooth](https://github.com/nsoria1)
