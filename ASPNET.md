## Stripe Payment Gateway:
- Creating WebHook Endpoint using below command:
```
curl https://api.stripe.com/v1/webhook_endpoints -u sk_live_51LQL9UKV5xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxT 
-d url="https://www.xyz.com/api/v1/paymentwebhook/stripwebhook" 
-d "enabled_events[]"="payment_intent.succeeded" 
-d "enabled_events[]"="payment_intent.payment_failed"

```
