# Entity Framework

1. Create new .NET api project
2. In the `Web.config` file, include the following under the `<appSettings>` tags:
```C#
<connectionStrings>
    <add name="DotNetCoreConsole" connectionString="Server=(local); Database=DotNetCoreConsole; Trusted_Connection=True;" providerName="System.Data.SqlClient" />
</connectionStrings>
```
