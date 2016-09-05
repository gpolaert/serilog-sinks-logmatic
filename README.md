# Serilog.Sinks.Logmatic

[![NuGet Status](http://nugetstatus.com/serilog.sinks.logmatic.png)](http://nugetstatus.com/packages/serilog.sinks.logmatic) | [![Build status](https://ci.appveyor.com/api/projects/status/ntpaealecc1arba4?svg=true)](https://ci.appveyor.com/project/gpolaert/serilog-sinks-logmatic)


A Serilog sink that send events and logs staight away to [Logmatic.io](http://logmatic.io).
By default the sink will use a TCP connection over SSL.


**Package** - [Serilog.Sinks.Logmatic](http://nuget.org/packages/serilog.sinks.logmatic)
| **Platforms** - .NET 4.5


```csharp
var log = new LoggerConfiguration()
    .WriteTo.Logmatic("<API_KEY>")
    .CreateLogger();
```

You can override the default behavior by manually specifing the following properties.

```csharp
var log = new LoggerConfiguration()
    .WriteTo.Logmatic(
        "<API_KEY>",
        ip: "app.logmatic.io",
        port: 10515,
        useSSL: true
    )
    .CreateLogger();
```
