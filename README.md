# QR Code Website

A web application built using ASP.NET MVC 4 and Entity Framework with MySQL database integration, designed for managing and generating QR codes, handling media/file uploads, and routing proxy URLs.

## Features

- **QR Code Generation & Management**: Generate and manage QR codes dynamically using `MessagingToolkit.QRCode`.
- **Proxy QR Routing**: Create proxy URLs to redirect generated QR codes dynamically to target URLs or hosted content.
- **File & Media Uploads**: Admin interface for uploading videos and documents (`vupload`, `vurl`).
- **Admin Dashboard**: Interactive dashboard with file management and link configuration tiles.
- **Responsive UI**: Integrated with Bootstrap 3.3.7, FontAwesome, Owl Carousel, and jQuery.

## Tech Stack

- **Framework**: ASP.NET MVC 4 (.NET Framework 4.5)
- **ORM**: Entity Framework 6 (with MySQL Provider)
- **Database**: MySQL (`MySql.Data.MySqlClient`)
- **QR Generator Library**: `MessagingToolkit.QRCode` (v1.3.0)
- **Frontend**: Razor CSHTML views, Bootstrap 3.3.7, jQuery 3.1.1, Font Awesome 4.6.1, Owl Carousel

## Project Structure

```
├── Content/            # CSS stylesheets (Bootstrap, jQuery UI, Custom styles)
├── Scripts/            # JavaScript libraries (jQuery, Bootstrap, Moment.js, WOW.js)
├── Views/              # ASP.NET MVC Razor view files (Home, Admin, Shared layouts)
├── css/                # Additional CSS assets and FontAwesome stylesheets
├── fonts/              # Font files (FontAwesome, Glyphicons)
├── images/             # Static image assets and logo files
├── owl-carousel/       # Owl Carousel library assets
├── views qr code/      # QR code specific Razor view components
├── Web.config          # ASP.NET application configuration & connection strings
└── packages.config     # NuGet package dependencies
```

## Getting Started

### Prerequisites

- [Visual Studio 2017 or higher](https://visualstudio.microsoft.com/) with **ASP.NET and web development** workload installed.
- **.NET Framework 4.5** Developer Pack.
- **MySQL Server** instance (local or hosted).

### Database Configuration

1. Locate `Web.config` in the root directory.
2. Update the MySQL connection string under `<connectionStrings>` according to your MySQL server settings:

```xml
<connectionStrings>
  <add name="con" connectionString="server=YOUR_SERVER;User Id=YOUR_USER;password=YOUR_PASSWORD;database=YOUR_DB;Persist Security Info=True;SslMode=none" providerName="MySql.Data.MySqlClient" />
  <add name="vectorEntities" connectionString="metadata=res://*/Models.vector.csdl|res://*/Models.vector.ssdl|res://*/Models.vector.msl;provider=MySql.Data.MySqlClient;provider connection string=&quot;server=YOUR_SERVER;user id=YOUR_USER;password=YOUR_PASSWORD;persistsecurityinfo=True;database=YOUR_DB&quot;" providerName="System.Data.EntityClient" />
</connectionStrings>
```

### Installation & Execution

1. Open the repository/solution in Visual Studio.
2. Restore NuGet packages:
   - Right-click the solution in Solution Explorer and select **Restore NuGet Packages**, or run NuGet package restore via Package Manager Console.
3. Build the solution (`Ctrl + Shift + B`).
4. Run the application (`F5` or `Ctrl + F5`) using IIS Express or your configured local web server.

## License

This project is licensed under the standard repository license terms.
