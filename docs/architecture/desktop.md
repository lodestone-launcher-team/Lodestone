# Desktop application

`src/Lodestone.Desktop` is a .NET 10 application using Avalonia 12. The current starter opens one window displaying the Avalonia welcome text.

`Program.cs` configures the desktop lifetime, platform detection and Inter font. `App.axaml` provides the Fluent theme; `App.axaml.cs` creates `MainWindow`. Debug builds include Avalonia developer tools.

The project references Lodestone.Core, Lodestone.Minecraft and Lodestone.Packages. Those libraries are currently empty; launcher and environment management behavior has not been implemented.

From the repository root, with the .NET SDK specified in `global.json` installed:

```sh
dotnet build
dotnet run --project src/Lodestone.Desktop
dotnet test
```

See [the architecture overview](overview.md) and [the Avalonia decision](../decisions/0003-use-avalonia.md).
