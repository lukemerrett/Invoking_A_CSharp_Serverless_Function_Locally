# Invoking A C# Serverless Function Locally

Sample repository showing how to invoke a Serverless function locally

## Prerequisites

* [NodeJS v12.14+](https://nodejs.org/en/)
* [DotNet Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core/3.1)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* Serverless installed as a global package - `npm update -g serverless`

## How This Repository Was Bootstrapped

Created a template C# application - `serverless create --template aws-csharp`

Everything is as the template generated, with the exception of the request object the handler expects, which I simplified slightly

## Running the Function Locally

1. Run the build script - `.\build.cmd`
2. Start the Docker service locally (Launch Docker Desktop)
3. Invoke locally - `serverless invoke local --function hello --path test_data.json`

This will download a base docker image then run your function inside the docker container, passing through the json in the `test_data.json` file at the root of this repository.

You should get output like the following:

```
START RequestId: b5f9a796-daa9-11d0-91de-216c1af48a19 Version: $LATEST
END RequestId: b5f9a796-daa9-11d0-91de-216c1af48a19
REPORT RequestId: b5f9a796-daa9-11d0-91de-216c1af48a19  Init Duration: 140.22 ms        Duration: 24.16 ms      Billed Duration: 100 ms Memory Size: 1024 MB    Max Memory Used: 39 MB

{"Message":"Go Serverless v1.0! Your function executed successfully!","Request":{"Value":"Bob"}}
```