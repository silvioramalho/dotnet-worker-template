# dotnet-worker-template

## Description

This project is an example of a console application in C# that uses `BackgroundService` to run background tasks. The application allows configuring the execution interval and the number of workers through the `appsettings.json` file.

## Configuration

Before running the project, make sure to configure the `appsettings.json` file as needed:

```json
{
  "WorkerIntervalActive": "10000", // Execution interval in milliseconds
  "WorkersNumber": "1", // Number of workers
  "ConnectionStrings": {
    "DBConnection": "localhost" // Database connection string (currently not used)
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  }
}
```

## How to Run

1. Clone the repository:  

```bash
git clone https://github.com/silvioramalho/dotnet-worker-template.git
cd dotnet-worker-template/src/WorkerTemplate/WorkerTemplate.ConsoleApp 
```

2. Restore dependencies:  

```bash
dotnet restore
```

3. Build the project:  

```bash
dotnet build
```

4. Run the application:  

```bash
dotnet run
```

## Project Structure

* Program.cs: Configures services and initializes the host.
* Worker.cs: Implements the BackgroundService that runs background tasks.
* WorkerParams.cs: Defines configuration parameters for the workers.
* appsettings.json: Application configuration file.

## Dependencies

* .NET 8.0 or higher
* Microsoft.Extensions.Hosting
* Microsoft.Extensions.Logging


## Contribution

Feel free to open issues and pull requests for improvements and fixes.  


## License

This project is licensed under the MIT License. See the LICENSE file for more details.