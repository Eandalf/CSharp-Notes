# Background

This document will go through the background of C#.

## `C#`

C# (pronounced "See Sharp") is a modern, object-oriented, and type-safe programming language. C# has its roots in the C family of languages and will be immediately familiar to C, C++, Java, and JavaScript programmers. [1]

C# is an object-oriented, component-oriented programming language. C# provides language constructs to directly support these concepts, making C# a natural language in which to create and use software components. Since its origin, C# has added features to support new workloads and emerging software design practices. [1]

Features [1]

- Garbage collection
- Exception handling
- Lambda expressions
- Query syntax
- Asynchronous operations
- Pattern matching
- Unified type system
  - All C# types, including primitive types such as `int` and `double`, inherit from a single root `object` type. All types share a set of common operations. Values of any type can be stored, transported, and operated upon in a consistent manner. [1]
- User-defined reference types and value types
- Dynamic allocation of objects and in-line storage of lightweight structures

## .NET

- .NET is a free, open-source development platform for building many kinds of apps. [2]
- Programming languages: .NET supports three programming languages [2]
  - C#
  - F#
  - Visual Basic
- IDEs [2]
  - Visual Studio
  - Visual Studio Code
  - Visual Studio for Mac
  - GitHub Codespaces
- SDK and runtimes [2]
  - The .NET SDK is a set of libraries and tools for developing and running .NET applications.
- Terminology [2]
  - .NET Framework
    - A development platform for creating Windows apps.
  - .NET Core and .NET 5
    - A cross-platform, open-source successor to .NET Framework.
    - This new implementation of .NET was named .NET Core until it reached version 3.1. The next version after .NET Core 3.1 is .NET 5.0, which is currently in preview. Version number 4 was skipped to avoid confusion between this implementation of .NET and .NET Framework 4.8. The name "Core" was dropped to make clear that this is now the main implementation of .NET.
    - Unlike the .NET Framework, .NET Core is not considered a Windows component. Therefore, updates come as NuGet packages, not through Windows Update. [3]
  - .NET Standard
    - .NET Standard is an API specification that lets you develop class libraries for multiple implementations of .NET.
    - .NET Standard is a specification for implementing the BCL. Since a .NET implementation is required to follow this standard, application developers will not have to worry about different versions of the BCL for each managed framework implementation. [3]
      - Each implementation of the managed framework has its own set of Base Class Libraries. The Base Class Library (BCL) contains classes such as exception handling, strings, XML, I/O, networking, and collections.
    - The relationship between .NET Standard and a .NET implementation is the same as between the HTML specification and a browser. The second is an implementation of the first. [3]
    - Each .NET version has an associated version of the .NET Standard. [3]
- Analogy
  - C# (.NET languages) <-> Java
  - MSIL, Microsoft Intermediate Language <-> Java bytecode
  - CLR, Common Language Runtime <-> JVM

## MSBuild

A build engine for building a project.

Project file (.csproj) [2]

- For a console app:

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>net5.0</TargetFramework>
  </PropertyGroup>
</Project>
```

- For a web app:

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">
  <PropertyGroup>
    <TargetFramework>net5.0</TargetFramework>
  </PropertyGroup>
</Project>
```

## NuGet

NuGet is an open-source package manager designed for .NET.

To include a NuGet package: `dotnet add package PackageName`

- For example, `dotnet add package NUnit --version 3.12.0`

## References

[1] [A tour of the C# language](https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/)

[2] [Introduction to .NET](https://docs.microsoft.com/en-us/dotnet/core/introduction)

[3] [.NET Core and .NET Standard: What Is the Difference?](https://www.infoq.com/news/2017/10/dotnet-core-standard-difference/)

## Read More

- [Introducing .NET Standard](https://devblogs.microsoft.com/dotnet/introducing-net-standard/)
- [Microsoft Says .NET 5 Replaces .NET Standard (Except for ...)](https://visualstudiomagazine.com/articles/2020/09/16/net-standard-future.aspx)
- [.NET Glossary](https://docs.microsoft.com/en-us/dotnet/standard/glossary)
