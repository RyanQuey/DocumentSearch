# CURRENT STATUS
Couldn't get it to work. Installed some stuff using nuget, but couldn't figure out how to get it to build, and this thing doesn't have much by way of docs...

I'm giving up - I don't have the skills to make this work in C#. But I do like the base idea, and though I can't figure out how he did this, will try a similar stack (Tika + ES) in my other project: https://github.com/RyanQuey/es-index-onedrive

# Setup
## Get ES up and running

From project root
```
docker-compose up -d
```

## C# project
- Open in VS Code
- Install 4.7.2 if don't have already
    https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net472-developer-pack-offline-installer

- install C# plugin based on omnisharp (use the official microsoft plugin)

### Setup ./DocumentSearch/ project
```
cd ./DocumentSearchCore/
```

- install nuget if don't have already

    ```
# download the file
https://www.nuget.org/downloads
# or somewhere on your path
mkdir -p C:\Users\queyr\.dotnet\tools\
# move nuget executable there
mv C:\Users\queyr\Downloads\nuget.exe C:\Users\queyr\.dotnet\tools\ 
```

- install Nuget packages from packages.config

    ```
    cd C:\Users\queyr\projects\DocumentSearch\DocumentSearch
    nuget.exe install .\packages.config
    ```

# Run it

## Index documents
Open ./DocumentSearch


# Project Notes
## Directory Organization
### ./DocumentSearch
Indexer. This is what writes to ES
- when running, .net core will find the .csproj file (which is the main file) and run it

### ./DocumentSearchCore

### ./DocumentSearchClient
Web client. For a GUI/UI. Reads from ES

