# Problem

Cannot publish application in .Net6 RC2 with workload installed. This worked in .Net 6 RC1.

## Steps
Install workload if you haven't already:

```
dotnet workload install wasm-tools
```

Publish project:

```
dotnet publish -c Release .\Web\
```

Output:
```
Microsoft (R) Build Engine version 17.0.0-preview-21501-01+bbcce1dff for .NET
Copyright (C) Microsoft Corporation. All rights reserved.

  Determining projects to restore...
  All projects are up-to-date for restore.
  You are using a preview version of .NET. See: https://aka.ms/dotnet-core-preview
  LazyBlazy -> C:\code\P4\LazyLoadProblem\LazyBlazy\bin\Release\net6.0\LazyBlazy.dll
  Web -> C:\code\P4\LazyLoadProblem\Web\bin\Release\net6.0\Web.dll
  Web (Blazor output) -> C:\code\P4\LazyLoadProblem\Web\bin\Release\net6.0\wwwroot
  Optimizing assemblies for size, which may change the behavior of the app. Be sure to test after publishing. See: https://aka.ms/dotnet-illink
  LazyBlazy -> C:\code\P4\LazyLoadProblem\LazyBlazy\bin\Release\net6.0\LazyBlazy.dll
  Web -> C:\code\P4\LazyLoadProblem\Web\bin\Release\net6.0\Web.dll
  Web (Blazor output) -> C:\code\P4\LazyLoadProblem\Web\bin\Release\net6.0\wwwroot
  Optimizing assemblies for size, which may change the behavior of the app. Be sure to test after publishing. See: https://aka.ms/dotnet-illink
C:\Program Files\dotnet\sdk\6.0.100-rc.2.21505.57\Sdks\Microsoft.NET.Sdk.BlazorWebAssembly\targets\Microsoft.NET.Sdk.BlazorWebAssembly.6_0.targets(524,5): error BLAZORSDK1001: Unable to find 'LazyBlazy.dll' to be lazy loaded later. Confirm that project or package references are included and the reference is used in the project. [C:\code\P4\LazyLoadProblem\Web\Web.csproj]
```