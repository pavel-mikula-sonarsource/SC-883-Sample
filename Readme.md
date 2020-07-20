# SonarScanner for MSBuild

[https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-msbuild/](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-msbuild/)

# .NET Framework or .NET Core with MSBuild example (Windows)

```
SonarScanner.MSBuild.exe begin /d:sonar.host.url="https://sonarcloud.io" /o:"pavel-mikula-test" /k:"SC-883-Sample-NetFramework" /d:sonar.login=tokentokentokentoken
MSBuild.exe SC-883-Sample-NetFramework.sln /t:Rebuild
SonarScanner.MSBuild.exe end /d:sonar.login=tokentokentokentoken
```

# .NET Core dotnet tool example (Windows, Linux, MacOS)

```
dotnet sonarscanner begin /d:sonar.host.url="https://sonarcloud.io" /o:"pavel-mikula-test" /k:"SC-883-Sample-NetFramework" /d:sonar.login=tokentokentokentoken
dotnet build SC-883-Sample-NetCore.sln
dotnet sonarscanner end /d:sonar.login=tokentokentokentoken
```