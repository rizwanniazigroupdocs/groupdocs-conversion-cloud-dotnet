# GroupDocs.Conversion Cloud SDK for .NET
This repository contains GroupDocs.Conversion Cloud SDK for .NET source code. This SDK allows you to work with GroupDocs.Conversion Cloud REST APIs in your .NET applications.

## How to use the SDK?
The complete source code is available in this repository folder, you can either directly use it in your project via NuGet package manager. For more details, please visit our [documentation website](https://docs.groupdocs.cloud/display/conversioncloud/Available+SDKs#AvailableSDKs-.NET).

## Dependencies
- .NET Framework 2.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json)
- [StyleCop.MSBuild](https://www.nuget.org/packages/StyleCop.MSBuild)

NOTE: The DLLs included in the package may not be up to date. We recommended using [NuGet](https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package Newtonsoft.Json
Install-Package StyleCop.MSBuild
``` 

## Getting Started

```csharp
using System;
using System.Diagnostics;
using GroupDocs.Conversion.Cloud.Sdk;
using GroupDocs.Conversion.Cloud.Sdk.Api;
using GroupDocs.Conversion.Cloud.Sdk.Model.Requests;

namespace Example
{
    public class Example
    {
        public void Main()
        {
            //TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud/ (free registration is required).
            var configuration = new Configuration
            {
                AppSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
                AppKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
            };

            var apiInstance = new ConversionApi(configuration);

            try
            {
                var request = new GetAllPossibleConversionsRequest();

                // Get supported file formats
                var response = ConversionApi.GetAllPossibleConversions(request);

                foreach (var entry in response.Conversions)
                {
                   Debug.Print(string.Format("{0}: {1}", entry.SourceFileType,
                        string.Join(",", entry.PossibleConversions));
                }
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ConversionApi.GetAllPossibleConversions: " + e.Message);
            }
        }
    }
}
```

## Licensing
All GroupDocs.Conversion for Cloud SDKs are licensed under [MIT License](LICENSE).

## Resources
+ [**Website**](https://www.groupdocs.cloud)
+ [**Product Home**](https://products.groupdocs.cloud/conversion/cloud)
+ [**Documentation**](https://docs.groupdocs.cloud/display/conversioncloud/Home)
+ [**Free Support Forum**](https://forum.groupdocs.cloud/c/conversion)
+ [**Blog**](https://blog.groupdocs.cloud/category/groupdocs-conversions-cloud-product-family/)

## Contact Us
Your feedback is very important to us. Please feel free to contact us using our [Support Forums](https://forum.groupdocs.cloud/c/conversion).