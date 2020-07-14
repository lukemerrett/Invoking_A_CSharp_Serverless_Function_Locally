# Invoking A C# Serverless Function Locally

Sample repository showing how to invoke a Serverless function locally

## Prerequisites

* [NodeJS v12.14+](https://nodejs.org/en/)
* [DotNet Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core/3.1)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* Serverless installed as a global package - `npm update -g serverless`
* Docker process running locally

## How This Repository Was Bootstrapped

1. Setup Serverless as a global package - `npm update -g serverless`
2. Created a template C# application - `serverless create --template aws-csharp`

## Running the Function Locally

1. Run the build script - `.\build.cmd`
2. Invoke locally - `serverless invoke local --function hello --data '{"Value": "Bob"}'`

## To Investigate

- [ ] How do you pass AWS credentials through to the docker container?