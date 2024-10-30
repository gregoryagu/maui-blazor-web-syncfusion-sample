This is a very simple sample which illustrates how to integrate Syncfusion Blazor controls into a ".NET Maui Blazor Hybrid and Web App" The reasons I created this sample:

The Syncfusion Extension which can upgrade a Blazor app to use Syncfusion controls does not work on a Blazor Hybrid and Web App"
There is currently no guidance from Syncfusion on how to do this, as this particular type of project is new in .net 9.
Why you would want to do this: You want to create an app using Syncfusion Blazor Controls. This is a Web App, along with a .net Maui Hybrid app (which runs on Windows, Mobile etc, but NOT the Web which is why the Web app is a seperate app.)

Note that Syncfusion has a different set of controls for .net Maui, but those are xaml controls, not web controls.

Code Highlights: There are only a few actual lines of code needed to make this work.

In both the Hybrid app, and the Blazor app, add the following to program.cs

builder.Services.AddSyncfusionBlazor();

In both the Hybrid app, and the Blazor app, add the following references:

PackageReference Include="Syncfusion.Blazor" Version="27.1.57" PackageReference Include="Syncfusion.Blazor.Themes" Version="27.1.57"

In the Blazor Project, also add your licence key to program.cs

Syncfusion.Licensing.SyncfusionLicenseProvider.RegisterLicense("YourKeyHere");//27.x.x
