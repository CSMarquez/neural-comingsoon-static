# Neural Coming Soon — Azure Static Web Apps

Landing page converted to a standalone Blazor WebAssembly app targeting .NET 10.

This project is intended for Azure Static Web Apps. It does not require an ASP.NET Core server at runtime.

## Run locally

```bash
cd Neural.ComingSoon.StaticWebApp
dotnet restore
dotnet run
```

Open the URL shown by the terminal, usually:

```text
https://localhost:7182
```

## Publish locally

```bash
dotnet publish -c Release
```

For standalone Blazor WebAssembly static hosting, deploy the published `wwwroot` content from:

```text
bin/Release/net10.0/publish/wwwroot
```

Depending on SDK settings, the output can also appear under:

```text
bin/Release/net10.0/browser-wasm/publish/wwwroot
```

## Azure Static Web Apps settings

When creating the Static Web App in the Azure Portal with GitHub:

```text
Build preset: Blazor
App location: /
Api location: leave empty
Output location: wwwroot
```

Use the Free plan for this landing page.

## Files of interest

```text
wwwroot/index.html
wwwroot/app.css
wwwroot/assets/neural-logo.svg
Pages/Home.razor
staticwebapp.config.json
```

`staticwebapp.config.json` includes navigation fallback to `index.html`, which is required for client-side routing.
# neural-comingsoon-static
# neural-comingsoon-static
