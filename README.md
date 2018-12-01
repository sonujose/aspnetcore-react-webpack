# React, .NET Core, Webpack 

This application bootstraps react.js from asp.net core mvc app using webpack. Make sure node and npm installed in your machine.

Check npm and node version. Make sure both are updated

Update npm run - `npm i npm@latest -g`

If any of the node packages are not loaded please load package explicitly - `npm install`. 

The npm modules are build during the dotnet build - see the csproj file (All the webpack magic happens there).

To Run the app - trigger `dotnet run`

```cmd
dotnet restore
dotnet build
dotnet run
```

## Analyze your webpack modules

This app consists of 2 webpack modules 

- webpack.config.js - Application level files are modularized here
- webpack-config.vendor.js - Vendor dependencies are build here eg: react modules 

Run

```cmd
webpack --profile --json >> stats.json
```

Open http://webpack.github.io/analyse/#modules or you can use any webpack visualizer

Upload stats.json file from your repository