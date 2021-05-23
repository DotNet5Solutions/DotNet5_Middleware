# DotNet5_Middleware
ASP.NET Core Middleware

ASP.NET Core has new concept called **Middleware **. A middleware is nothring bua conponenet(class) which is executed on every request in ASP.NET Core application. In the classic ASP.NET, HttpHandlers and HttpModules were part of request pipeline. Middleware is similar to HttpHandlers and HttpModules where both needs to be configures and excuted in each request.

Typically, there will be multiple middleware in ASP.NET Core web application. It can be either framework provided middleware, added via NuGet or your own custom middleware. We can se the order of middleware execution in the request pipeline. Each middleware adds or modifies http request and optionally passes control to the next middleware component.

![File](Images/file.png)

Middleware build the request pipeline. The following figure illustrates the ASP.NET Core request processing.
![File2](Images/file2.png)


How To Add Custom Middleware in ASP.NET Core Application

Add -> New Item -> middleware ->MyMiddleware.cs

![Add Middleware](Images/AddMiddleware.png)

Now we have to update the code as follows
![Middleware Class](Images/MiddlewareClass.png)

Before running the project lets add a NuGet package manager as follows:
![Add Nuget](Images/AddNuget.png)

Make the changes in MyMiddleware class as follows:
![Modified Class](Images/ModifiedClass.png)

Update Startup.cs class as follows to register custom middleware
![Startup Class](Images/StartupClass.png)

Run the project and see the log in Debut windows
![Output Window](Images/OutputWindow.png)

Middleware implemented successfully!!!