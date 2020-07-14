# Invoking A C# Serverless Function Locally

Sample repository showing how to invoke a Serverless function locally

## Prerequisites

* [NodeJS v12.14+](https://nodejs.org/en/)
* [DotNet Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core/3.1)
* Serverless installed as a global package - `npm update -g serverless`

## How This Repository Was Bootstrapped

1. Setup Serverless as a global package - `npm update -g serverless`
2. Created a template C# application - `serverless create --template aws-csharp`
3. Restored the C# dependencies - `dotnet restore`
4. Build the project to check it worked correctly - `dotnet build`
