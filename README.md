# DotNetCodespaces
Repo for building .NET in Codespaces

## EP Build CLI with System.CommandLine

* [System.CommandLine](https://learn.microsoft.com/en-us/dotnet/standard/commandline/get-started-tutorial)

Create a new project that uses System.CommandLine
```bash
mkdir scl && cd scl
dotnet new console --framework net6.0
dotnet add package System.CommandLine --prerelease
```
Add in code for `Program.cs` and the run the help menu

```bash
dotnet build
cd bin/Debug/net6.0
#run 
./scl --help
```

You should see this:

```bash
{
  "runtimeOptions": {
    "tfm": "net6.0",
    "framework": {
      "name": "Microsoft.NETCore.App",
      "version": "6.0.0"
    }
  }
}

```

To run
```
./scl --file scl.runtimeconfig.json
```

To run using `dotnet command` cd to project root and run:

```bash
dotnet run -- --help ./scl
```

To publish the binary

```bash
dotnet publish -o publish
cd ./publish
./scl --help
```

To get version do the following:

```bash
./scl --version
```

#### Add subcommand

* [subcommand docs](https://learn.microsoft.com/en-us/dotnet/standard/commandline/get-started-tutorial#add-a-subcommand-and-options)

```bash
wget https://raw.githubusercontent.com/dotnet/samples/main/csharp/getting-started/console-teleprompter/sampleQuotes.txt
```

After build you can then do the following

```bash
./scl read --file sampleQuotes.txt --fgcolor Red
```



## Setup your environment

* Configure DevContainer
* Add NuGet see installPackageConsole Demo
* Build .NET console app inside of new environment
* One with package:  https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-using-the-dotnet-cli


