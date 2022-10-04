## Stripe Payment Gateway:
- Creating WebHook Endpoint using below command:
```
curl https://api.stripe.com/v1/webhook_endpoints -u sk_live_51LQL9UKV5xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxT 
-d url="https://www.xyz.com/api/v1/paymentwebhook/stripwebhook" 
-d "enabled_events[]"="payment_intent.succeeded" 
-d "enabled_events[]"="payment_intent.payment_failed"

```

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
