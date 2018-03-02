Did you see how simple the csproj files for .NET core or .NET standard projects are?

Below an example from an .NET core WebAPI project:

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">
  <PropertyGroup>
    <TargetFramework>netcoreapp2.0</TargetFramework>
  </PropertyGroup>
  
  <ItemGroup> 
    <Folder Include="wwwroot\" />
  </ItemGroup>

  <ItemGroup>
    <PackageReference Include="AutoMapper" Version="6.2.2" />
    <PackageReference Include="AutoMapper.Extensions.Microsoft.DependencyInjection" Version="3.2.0" />
    <PackageReference Include="MediatR" Version="4.0.1" />
    <PackageReference Include="MediatR.Extensions.Microsoft.DependencyInjection" Version="4.0.0" />
    <PackageReference Include="Microsoft.AspNetCore.All" Version="2.0.5" />
    <PackageReference Include="Microsoft.EntityFrameworkCore" Version="2.0.1" />
  </ItemGroup>

</Project>
```

Microsoft decieded to remove all references to the files included in the project from the csproj file. Which makes creatubg and updating project files much easier than using the original csproj format.  

An empty project looks like this:

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">
  <PropertyGroup>
    <TargetFramework>netcoreapp2.0</TargetFramework>
  </PropertyGroup>
</Project>
```

Simple, isn't it?


