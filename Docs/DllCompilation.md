## DLL Compilation
In order to make the build process copy all referenced dll files from NuGet packages from the cache folder into the build output, set this property inside a `<PropertyGroup>` in the csproj file:
```xml
<CopyLocalLockFileAssemblies>true</CopyLocalLockFileAssemblies>
```
Source: https://stackoverflow.com/questions/45464271/include-nuget-dependencies-in-my-build-output
