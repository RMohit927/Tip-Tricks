## Stripe Payment Gateway:
- Creating WebHook Endpoint using below command:
```
curl https://api.stripe.com/v1/webhook_endpoints -u sk_live_51LQL9UKV5xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxT 
-d url="https://www.xyz.com/api/v1/paymentwebhook/stripwebhook" 
-d "enabled_events[]"="payment_intent.succeeded" 
-d "enabled_events[]"="payment_intent.payment_failed"

```

## Azure Key Vault Connection to ASP.NET core:
Helpful Nuget Package:
----------------------
1. Azure.Identity
2. Azure.Security.KeyVault.Secrets
3. Microsoft.Extensions.Configuration.AzureKeyVault
4. Azure.Extensions.AspNetCore.Configuration.Secrets

Console App: 
-----------
1. https://www.c-sharpcorner.com/blogs/fetching-secrets-from-key-vault-in-net-console-app
2. https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-net?tabs=azure-cli

App:
----
1. https://learn.microsoft.com/en-us/aspnet/core/security/key-vault-configuration?view=aspnetcore-5.0
2. ![image](https://user-images.githubusercontent.com/86957308/194701466-e18accfe-526c-4b9e-89b1-4bed481a661d.png)
3. https://www.youtube.com/watch?v=RTq72C10x88
4. https://github.com/a-patel/azure-key-vault-labs

## Pdf Password Protected Check:
```
1. Using ITextSharp:
--------------------

using iTextSharp.text.pdf;
using System;

namespace IsPdf_Password_Protected
{
    internal class Program
    {
        static void Main(string[] args)
        {
			string fileName = "C:\\Users\\radad\\Downloads\\Accredited Mail.pdf";
            Console.WriteLine(IsPasswordProtectedByITextSparp(fileName));
        }
        public static bool IsPasswordProtectedByITextSparp(string pdfFullname)
        {
            try
            {
                var pdfReader = new PdfReader(pdfFullname);
                return false;
            }
            catch (Exception e)
            {
                return true;
            }
        }
    }
}

2. Using Spire Pdf:
-------------------

using Spire.Pdf;
using System;

namespace IsPdf_Password_Protected
{
    internal class Program
    {
        static void Main(string[] args)
        {
			string fileName = "C:\\Users\\radad\\Downloads\\Accredited Mail.pdf";
            Console.WriteLine(IsPasswordProtectedBySpirePdf(fileName));
        }
        public static bool IsPasswordProtectedBySpirePdf(string pdfFullname)
        {
            return PdfDocument.IsPasswordProtected(pdfFullname);
        }
    }
}

```


