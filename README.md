# WebContent.Packer

[![Nuget](https://img.shields.io/nuget/v/WebContent.Packer?style=flat-square)](https://www.nuget.org/packages/WebContent.Packer/#readme-body-tab)

Pack web contents into embedded resources, compatible with vite, webpack, rollup or any other, even vanilla js

Usage

```xml
<Project Sdk="Microsoft.NET.Sdk">
    <PropertyGroup>
        <Nullable>enable</Nullable>
        <UseWPF>true</UseWPF>
        <LangVersion>11.0</LangVersion>
    </PropertyGroup>

    <ItemGroup>
        <PackageReference Include="WebContent.Packer" Version="1.0.0" />
    </ItemGroup>

</Project>
```

That's it, default webcontent folder is `./Views`, `./View/dist/index.js` and `./View/dist/style.css` will compile as EmbeddedResource within dll.

You can change default folder via `ViewPackageRoot`, like this:

```xml
<Project Sdk="Microsoft.NET.Sdk">
    <PropertyGroup>
        <Nullable>enable</Nullable>
        <UseWPF>true</UseWPF>
        <LangVersion>11.0</LangVersion>
        <ViewPackageRoot>where/ever/you/are</ViewPackageRoot>
    </PropertyGroup>

    <ItemGroup>
        <PackageReference Include="WebContent.Packer" Version="1.0.0" />
    </ItemGroup>

</Project>
```

also there is option to change default npm client which is `pnpm`, like this `<DefaultNpmClient>yarn</DefaultNpmClient>`