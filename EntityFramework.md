# Entity Framework

1. Create new .NET api project
2. In the `Web.config` file, include the following under the `<appSettings>` tags:
```C#
<connectionStrings>
    <add name="DotNetCoreConsole" connectionString="Server=(local); Database=DotNetCoreConsole; Trusted_Connection=True;" providerName="System.Data.SqlClient" />
</connectionStrings>
```
3. In the `Models` folder, create a class, which will be a table in your DB. Add some "columns" to it (aka fields).
4. In the `Models` folder, create a class called `AppDbContext` and put the following inside the namespace:
```C#
public class AppDbContext : DbContext
    {
        public AppDbContext() : base("EntityFrameworkHonda") { }

        public virtual DbSet<Civic> Civics { get; set; }
    }
```
