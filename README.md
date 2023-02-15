# Tutorial: Get started with ASP.NET Core

This tutorial shows how to create and run an ASP.NET Core web app using the .NET Core CLI.

You'll learn how to:

* Create a web app project
* Trust the development certificate.
* Run the app.
* Edit a Razor page.
 
At the end, you'll have a working web app running on your local machine.

##  Prerequisites
[.NET 6.0 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)

##  Create a web app project

Open a command shell, and enter the following command:

```Command shell
.NET CLI
dotnet new webapp -o aspnetcoreapp
```

The preceding command:
* Create a web app project.
* The -o aspnetcoreapp parameter creates a directory named aspnetcoreapp with
the source files for the app.

## Trust the development certificate.

```Command shell
.NET CLI
dotnet dev-certs https --trust
```

Select Yes if you agree to trust the development certificate.

## Run the app

```Command shell
.NET CLI
cd aspnetcoreapp
dotnet watch run
```

After the command shell indicates that the app has started, browse to
https://localhost:{port} , where {port} is the random port used.


## Edit a Razor page

Open Pages/Index.cshtml and modify and save the page with the following highlighted
markup:

```CSHTML
@page
@model IndexModel
@{
 ViewData["Title"] = "Home page";
}
<div class="text-center">
 <h1 class="display-4">Welcome</h1>
 <p>Hello, world! The time on the server is @DateTime.Now</p>
</div>
```

Browse to https://localhost:{port} , refresh the page, and verify the changes are
displayed.
