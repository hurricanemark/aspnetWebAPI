# ASP.NET Core project Created Using dotnet CLI

This project was created using `dotnet` commandline and loaded into VSCode.  There may be a few extentions required such as SwaggerUI, C#, ASP.NET,...

## Creating a new ASP.NET Core project

From a powershell terminal, do the followings:

* Create a new folder and cd into it

* Verify dotnet templates available, there should be one for `webapi`

```javascript
dotnet new --list

dotnet new webapi -o myWeatherAPI

cd myWeatherAPI

dotnet dev-certs https --trust

code .
```

At this stage, the project should be loading into VSCode.

Open PS terminal and type:

```typescript
dotnet run

PS D:\DEVEL\C-SharpProjs\LINKEDIN_TRAINING_2023\.NET7API\hello\myHelloAPI> dotnet run --watch
Building...
info: Microsoft.Hosting.Lifetime[14]
      Now listening on: https://localhost:5059
info: Microsoft.Hosting.Lifetime[0]
      Application started. Press Ctrl+C to shut down.
info: Microsoft.Hosting.Lifetime[0]
      Hosting environment: Development
info: Microsoft.Hosting.Lifetime[0]
      Content root path: D:\DEVEL\C-SharpProjs\LINKEDIN_TRAINING_2023\.NET7API\hello\myHelloAPI
```

The IDE should build and launch the application via the project profiles tag for    `localhost:port` as specified in `Properties/launchSettings.json`

eg.
```json
    "http": {
      "commandName": "Project",
      "dotnetRunMessages": true,
      "launchBrowser": true,
      "launchUrl": "swagger",
      "applicationUrl": "https://localhost:5059",
      "environmentVariables": {
        "ASPNETCORE_ENVIRONMENT": "Development"
      }
    },
    "https": {
      "commandName": "Project",
      "dotnetRunMessages": true,
      "launchBrowser": true,
      "launchUrl": "swagger",
      "applicationUrl": "https://localhost:7214;http://localhost:5059",
      "environmentVariables": {
        "ASPNETCORE_ENVIRONMENT": "Development"
      }
    },
```

Open the browser to https//localhost:5059/weatherforecast/


## Output

```json
[
  {
    "date": "2023-08-02",
    "temperatureC": 26,
    "temperatureF": 78,
    "summary": "Chilly"
  },
  {
    "date": "2023-08-03",
    "temperatureC": 16,
    "temperatureF": 60,
    "summary": "Hot"
  },
  {
    "date": "2023-08-04",
    "temperatureC": -3,
    "temperatureF": 27,
    "summary": "Balmy"
  },
  {
    "date": "2023-08-05",
    "temperatureC": 10,
    "temperatureF": 49,
    "summary": "Bracing"
  },
  {
    "date": "2023-08-06",
    "temperatureC": -13,
    "temperatureF": 9,
    "summary": "Cool"
  }
]
```