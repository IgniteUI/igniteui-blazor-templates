![Ignite UI for Blazor](https://raw.githubusercontent.com/IgniteUI/igniteui-blazor/master/images/general/Ignite-UI-for-Blazor.png)

# Ignite UI for Blazor Templates - from Infragistics

[![NuGet version](https://badge.fury.io/nu/IgniteUI.Blazor.Templates.svg)](https://www.nuget.org/packages/IgniteUI.Blazor.Templates)
[![Discord](https://img.shields.io/discord/836634487483269200?logo=discord&logoColor=ffffff)](https://discord.com/channels/836634487483269200/836636796229386241)

`dotnet new` templates for [Ignite UI for Blazor]. Scaffold a complete Blazor Web App wired up with Ignite UI, or drop a ready-to-edit page for any Ignite UI component into an existing project — from the .NET CLI or Visual Studio.

## Purpose

This repository hosts the code for the [IgniteUI.Blazor.Templates] NuGet package and is also intended for users to create feature requests, submit issues, and ask questions related to the templates.

It was split out of [igniteui-blazor](https://github.com/IgniteUI/igniteui-blazor), which remains the home of the Ignite UI for Blazor Lite components themselves.

## Overview

### Project template

| Template | Short name | Description |
| :------- | :--------: | :---------- |
| Ignite UI Blazor Web App | `igb-blazor` | Blazor Web App with Ignite UI registered, themed, and a navbar / nav drawer layout. Optional Weather page with [Grid Lite][Grid Lite] and [Blazor-ApexCharts]. |

| Parameter | Description | Values | Default |
| :-------- | :---------- | :----: | :-----: |
| `--Hosting` (`-H`) | Interactivity hosting model | `Server`, `Wasm`, `Auto` | `Server` |
| `--Theme` (`-T`) | Ignite UI design theme | `bootstrap`, `material`, `fluent`, `indigo` | `bootstrap` |
| `--Variant` (`-V`) | Light or dark color variant | `light`, `dark` | `light` |
| `--IncludeWeatherSample` | Include the Weather page (Grid Lite + chart demo) | `true`, `false` | `true` |
| `--SkipRestore` | Skip automatic NuGet restore on create | `true`, `false` | `false` |

Template strings are localized for `en`, `ja` and `ko`.

### Component item templates

Each item template scaffolds a single `.razor` page (plus a scoped `.css` file) demonstrating one component. In Visual Studio they appear under **Add → New Item → Ignite UI for Blazor**.

| Components          | Short name              |         Documentation          |
| :------------------ | :---------------------- | :----------------------------: |
| Accordion           | `igb-accordion`         |     [Docs][Accordion Docs]     |
| Avatar              | `igb-avatar`            |      [Docs][Avatar Docs]       |
| Badge               | `igb-badge`             |       [Docs][Badge Docs]       |
| Banner              | `igb-banner`            |      [Docs][Banner Docs]       |
| Breadcrumbs         | `igb-breadcrumbs`       |          Coming soon           |
| Button              | `igb-button`            |      [Docs][Button Docs]       |
| Button Group        | `igb-button-group`      |   [Docs][Button Group Docs]    |
| Calendar            | `igb-calendar`          |     [Docs][Calendar Docs]      |
| Card                | `igb-card`              |       [Docs][Card Docs]        |
| Carousel            | `igb-carousel`          |     [Docs][Carousel Docs]      |
| Checkbox            | `igb-checkbox`          |     [Docs][Checkbox Docs]      |
| Chip                | `igb-chip`              |       [Docs][Chip Docs]        |
| Circular Progress   | `igb-circular-progress` | [Docs][Circular Progress Docs] |
| Color Picker        | `igb-color-picker`      |          Coming soon           |
| Combo               | `igb-combo`             |       [Docs][Combo Docs]       |
| Date Picker         | `igb-date-picker`       |    [Docs][Date Picker Docs]    |
| Date Range Picker   | `igb-date-range-picker` |       [Docs][Date Range]       |
| Date Time Input     | `igb-date-time-input`   |  [Docs][Date Time Input Docs]  |
| Dialog              | `igb-dialog`            |      [Docs][Dialog Docs]       |
| Drop Down           | `igb-dropdown`          |     [Docs][Dropdown Docs]      |
| Expansion Panel     | `igb-expansion-panel`   |  [Docs][Expansion Panel Docs]  |
| Grid Lite           | `igbgrid`               |        [Docs][Grid Lite]       |
| Icon                | `igb-icon`              |       [Docs][Icon Docs]        |
| Icon Button         | `igb-icon-button`       |    [Docs][Icon Button Docs]    |
| Input               | `igb-input`             |       [Docs][Input Docs]       |
| Linear Progress     | `igb-linear-progress`   |  [Docs][Linear Progress Docs]  |
| List                | `igb-list`              |       [Docs][List Docs]        |
| Mask Input          | `igb-mask-input`        |   [Docs][Masked Input Docs]    |
| Navigation Bar      | `igb-navbar`            |  [Docs][Navigation Bar Docs]   |
| Navigation Drawer   | `igb-nav-drawer`        | [Docs][Navigation Drawer Docs] |
| QR Code             | `igb-qr-code`           |          Coming soon           |
| Radio Group         | `igb-radio-group`       |       [Docs][Radio Docs]       |
| Range Slider        | `igb-range-slider`      |      [Docs][Slider Docs]       |
| Rating              | `igb-rating`            |      [Docs][Rating Docs]       |
| Select              | `igb-select`            |      [Docs][Select Docs]       |
| Slider              | `igb-slider`            |      [Docs][Slider Docs]       |
| Snackbar            | `igb-snackbar`          |     [Docs][Snackbar Docs]      |
| Stepper             | `igb-stepper`           |      [Docs][Stepper Docs]      |
| Switch              | `igb-switch`            |      [Docs][Switch Docs]       |
| Tabs                | `igb-tabs`              |       [Docs][Tabs Docs]        |
| Textarea            | `igb-textarea`          |     [Docs][Textarea Docs]      |
| Tile Manager        | `igb-tile-manager`      |   [Docs][Tile Manager Docs]    |
| Toast               | `igb-toast`             |       [Docs][Toast Docs]       |
| Toggle Button       | `igb-toggle-button`     |   [Docs][Button Group Docs]    |
| Tooltip             | `igb-tooltip`           |      [Docs][Tooltip Docs]      |
| Tree                | `igb-tree`              |       [Docs][Tree Docs]        |
| ApexCharts Chart    | `apexchart`             |     [Docs][Blazor-ApexCharts]  |

## Usage

### Install the templates

```bash
dotnet new install IgniteUI.Blazor.Templates
```

### Create a project

```bash
dotnet new igb-blazor -n MyApp
```

Interactive WebAssembly hosting with the Material dark theme:

```bash
dotnet new igb-blazor -n MyApp --Hosting Wasm --Theme material --Variant dark
```

Server hosting with the Fluent theme, without the Weather sample page:

```bash
dotnet new igb-blazor -n MyApp --Theme fluent --IncludeWeatherSample false
```

### Add a component page

Item templates are run from inside an existing project folder; pass the file name with `-n`:

```bash
cd MyApp/MyApp/Components/Pages
dotnet new igb-button -n ButtonsDemo
```

For `Wasm` or `Auto` hosting, use `cd MyApp/MyApp.Client/Pages` instead. This drops `ButtonsDemo.razor` into the current directory. Run `dotnet new <short-name> -h` to see a template's options.

### Register Ignite UI for Blazor

Projects created from `igb-blazor` are already set up. To use the item templates in any other project, do this once:

1 - Install the [IgniteUI.Blazor.Lite] package:

```bash
dotnet add package IgniteUI.Blazor.Lite
```

2 - Open the **Program.cs** file and register the Ignite UI for Blazor Service:

```csharp
builder.Services.AddIgniteUIBlazor();
```

3 - Add the **IgniteUI.Blazor.Controls** namespace in the **_Imports.razor** file:

```csharp
@using IgniteUI.Blazor.Controls
```

4 - Add the Style Sheet in the **<head\>** element of the **Components/App.razor** file (Blazor Web App) or the **wwwroot/index.html** file (standalone Blazor WebAssembly):

```html
<head>
    <link href="_content/IgniteUI.Blazor/themes/light/bootstrap.css" rel="stylesheet" />
</head>
```

Don't mix `IgniteUI.Blazor.Lite` with the licensed `IgniteUI.Blazor` package.

Two item templates need additional packages: `igbgrid` requires `IgniteUI.Blazor.GridLite` and its theme stylesheet:

```bash
dotnet add package IgniteUI.Blazor.GridLite
```

```html
<link href="_content/IgniteUI.Blazor.GridLite/css/themes/light/bootstrap.css" rel="stylesheet" />
```

`apexchart` requires `Blazor-ApexCharts`:

```bash
dotnet add package Blazor-ApexCharts
```

Projects created with `--IncludeWeatherSample false` omit both packages. Add the package(s) needed by any `igbgrid` or `apexchart` item templates you use.

### Supported render modes

Ignite UI for Blazor components require an **interactive** render mode, so give scaffolded pages one of:

- **InteractiveServer**
- **InteractiveWebAssembly**
- **InteractiveAuto**

> **Note:** Render modes apply only to Blazor Web Apps (.NET 8+). Standalone Blazor WebAssembly and Blazor Server apps are interactive by default.

### Uninstall

```bash
dotnet new uninstall IgniteUI.Blazor.Templates
```

## Building and Running Locally

**Prerequisites:** [.NET SDK](https://dotnet.microsoft.com/download) 10.0 (see `global.json`). Generated projects target `net10.0`.

The template pack lives in `IgniteUI.Blazor.Templates/`: the project template under `templates/project/igb-blazor` and one folder per item template under `templates/item`. All commands below run from the repo root.

```bash
# 1. Pack the templates
dotnet pack IgniteUI.Blazor.Templates -c Release -o ./bin/packed

# 2. Install the packed nupkg (uninstall any previous copy first)
dotnet new uninstall IgniteUI.Blazor.Templates
dotnet new install ./bin/packed/IgniteUI.Blazor.Templates.<version>.nupkg
```

For faster iteration on the project template, skip packing and install straight from the source folder:

```bash
dotnet new install ./IgniteUI.Blazor.Templates/templates/project/igb-blazor
```

Then generate and run a project:

```bash
mkdir -p ./_smoketest && cd ./_smoketest
dotnet new igb-blazor -n MyTestApp --Hosting Server
cd MyTestApp
dotnet run --project MyTestApp/MyTestApp.csproj
```

For `Wasm` / `Auto` hosting the CLI also generates `MyTestApp.sln` with a host and a `.Client` project; build the solution and run the host with `dotnet run --project MyTestApp/MyTestApp.csproj`.

### Testing all templates

`IgniteUI.Blazor.Templates/test-templates.ps1` (PowerShell) and `test-templates.sh` (bash) install the whole pack from source, scaffold an `igb-blazor` Server app under `./tmp`, generate every item template into it and link each page from the nav drawer, so a single `dotnet run` exercises everything:

```bash
cd IgniteUI.Blazor.Templates
./test-templates.sh      # or ./test-templates.ps1
```

See the [package README](IgniteUI.Blazor.Templates/README.md#smoke-testing-the-templates) for the script options.

### Troubleshooting

- **`dotnet new` doesn't list `igb-blazor`** — run `dotnet new uninstall` (no args) to confirm `IgniteUI.Blazor.Templates` (or the folder path) shows up; reinstall if not.
- **Changes don't show up after reinstalling a nupkg** — bump `<Version>` in `IgniteUI.Blazor.Templates.csproj` so `dotnet new install` doesn't reuse a cached copy.
- **Two installs of the same template identity** — the warning at install time is harmless; the most recent install wins. Uninstall whichever you don't want.

## License

[MIT](LICENSE)

[Ignite UI for Blazor]: https://www.infragistics.com/products/ignite-ui-blazor
[IgniteUI.Blazor.Templates]: https://www.nuget.org/packages/IgniteUI.Blazor.Templates
[IgniteUI.Blazor.Lite]: https://www.nuget.org/packages/IgniteUI.Blazor.Lite
[Blazor-ApexCharts]: https://github.com/apexcharts/Blazor-ApexCharts
[Grid Lite]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/grid-lite/overview
[Switch Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/switch
[Radio Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/radio
[Navigation Drawer Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/menus/navigation-drawer
[Navigation Bar Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/menus/navbar
[List Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/grids/list
[Input Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/input
[Icon Button Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/icon-button
[Icon Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/icon
[Checkbox Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/checkbox
[Card Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/card
[Calendar Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/scheduling/calendar
[Button Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/button
[Badge Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/badge
[Avatar Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/avatar
[Slider Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/slider
[Rating Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/rating
[Toast Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/notifications/toast
[Snackbar Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/notifications/snackbar
[Chip Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/chip
[Circular Progress Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/circular-progress
[Linear Progress Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/linear-progress
[Dropdown Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/dropdown
[Tree Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/grids/tree
[Expansion Panel Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/expansion-panel
[Masked Input Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/mask-input
[Accordion Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/accordion
[Tabs Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/tabs
[Date Time Input Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/date-time-input
[Dialog Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/notifications/dialog
[Select Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/select
[Stepper Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/stepper
[Combo Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/combo/overview
[Textarea Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/text-area
[Button Group Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/button-group
[Banner Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/notifications/banner
[Date Picker Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/scheduling/date-picker
[Date Range]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/scheduling/date-range-picker
[Carousel Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/carousel
[Tile Manager Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/layouts/tile-manager
[Tooltip Docs]: https://www.infragistics.com/products/ignite-ui-blazor/blazor/components/inputs/tooltip
