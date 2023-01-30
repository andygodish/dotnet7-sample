There's an over-arching solutions file (.sln) that appears to encompass both the project (dotnet new classlib) and test project (dotnet new xunit). From the root directory containing the `.sln` file, run a `dotnet sln add <.csproj>` command to add a project to the solutions file.

On a related note, projects can be added as dependencies to other projects with the following command:

```
dotnet add <proj1.csproj> reference <proj2.csproj>
```

This will result in proj2 being added as an ItemGroup in the .csproj file of proj1.

```
  <ItemGroup>
    <ProjectReference Include="..\PrimeService\PrimeService.csproj" />
  </ItemGroup>
```
