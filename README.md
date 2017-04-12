[![Build Status](https://travis-ci.org/QubizSolutions/sample-dnca2s.svg?branch=master)](https://travis-ci.org/QubizSolutions/sample-dnca2s)
# sample-dnca2s

## Purpose
The purpose of this sample has several important parts:
  * It shows the Token Based Authentication using OWIN middleware pipeline with ASP.NET Core Web Api.
  * It provides the perfect playground to experience new technologies

## Setup
Below is a list of `Windows 10` steps to help setup each application. Please let us know if these are different on `Mac` or `Linux` and we'll update accordingly.

### Api
- navigate to `/src/Api`
- open cmd
- run `dotnet restore` - restores the NuGet packages(everything is NuGet based now)
- run `dotnet build` - builds the solution(new cli command for building .net core apps)
- run `dotnet run` - runs the application under `http://localhost:7000`(url is also displayed in the cmd)

### Web
- navigate to `/src/Web`
- open cmd
- run `dotnet restore` - restores the NuGet packages(everything is NuGet based now)
- run `dotnet build` - builds the solution(new cli command for building .net core apps)
- run `dotnet run` - runs the application under `http://localhost:7001`(url is also displayed in the cmd)

### Entity Framework Core
- navigate to `/src/Api`
- duplicate and rename `connectionstrings.sample.json` into `connectionstrings.json`
- add your connection string inside the `DefaultConnection` tag

## Technical details
We are going to use different tools and technologies. The system will be split into two:
  * Api: a RESTFUL Api providing the data(we are going to secure this)
  * Web: the Client of the Api which is going to present the information to the viewer(mainly build with Angular 2)

You can have a look at the **OAuth 2** standard that we'll be using [here](https://tools.ietf.org/html/rfc6749). We'll be using the **Resource Owner Password Credentials Grant** which is explained [here](http://tools.ietf.org/html/rfc6749#section-4.3).

Source code of the **OWIN middleware** aka ***Katana Project*** can be found on [codeplex](https://katanaproject.codeplex.com/SourceControl/latest#README).

### Technology stack
 * ASP.NET Core Web Api
 * ASP.NET Core MVC
 * OWIN, OAuth 2
 * HTML, CSS, Javascript
 * Angular 2
 * MsSql Server
 * Entity Framework Core
 * Bootstrap

## Goals
Below is a narrow list of goals for certain areas

### Development:
 * Experience .net core
 * Experience .net core with mysql(we want to move towards free-ware)
 * Experience .net core integration with OWIN
 * Experience .net core integration with Angular 2/4

### Deployment:
 * Experience .net core on linux & windows => Deploy on both Windows & Linux machines
 * Experience .net core in Docker => Host Docker in both Windows & Linux. Deploy to Docker.

### Features:
 * Multi-tenant application
 * Google OAuth Authentication(using OWIN)
 * Resource management(any kind of resource, since in REST everything is a resource)
 * Role management(Admin and User should sufice)
