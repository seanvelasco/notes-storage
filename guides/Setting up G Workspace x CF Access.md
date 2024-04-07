

1. Create a separate project in GCP for Cloudflare Access
2. Navigate to GCP > PROJECT > APIs & Services
3. Create OAuth consent screen under Oath consent screen
4. Create an OAuth 2.0 Client ID
5. Copy and paste Oath Client ID and Client secret to App ID and Client secret in Cloudflare Access. Fill out Google Workspace domain with your domain
6. Fill out Authorized JavaScript origins and Authorized redirect URIs in GCP
7. In GCP, enable Admin SDK API (https://console.cloud.google.com/apis/api/admin.googleapis.com)
8. In Google Admin, trust internal apps under API controls (https://admin.google.com/u/1/ac/owl)
9. Test the integration
























```
GSUITE ERROR: Failed to get google groups
{
  "error": {
    "code": 403,
    "message": "Admin SDK API has not been used in project 561359748979 before or it is disabled. Enable it by visiting https://console.developers.google.com/apis/api/admin.googleapis.com/overview?project=561359748979 then retry. If you enabled this API recently, wait a few minutes for the action to propagate to our systems and retry.",
    "errors": [
      {
        "message": "Admin SDK API has not been used in project 561359748979 before or it is disabled. Enable it by visiting https://console.developers.google.com/apis/api/admin.googleapis.com/overview?project=561359748979 then retry. If you enabled this API recently, wait a few minutes for the action to propagate to our systems and retry.",
        "domain": "usageLimits",
        "reason": "accessNotConfigured",
        "extendedHelp": "https://console.developers.google.com"
      }
    ],
    "status": "PERMISSION_DENIED",
    "details": [
      {
        "@type": "type.googleapis.com/google.rpc.Help",
        "links": [
          {
            "description": "Google developers console API activation",
            "url": "https://console.developers.google.com/apis/api/admin.googleapis.com/overview?project=561359748979"
          }
        ]
      },
      {
        "@type": "type.googleapis.com/google.rpc.ErrorInfo",
        "reason": "SERVICE_DISABLED",
        "domain": "googleapis.com",
        "metadata": {
          "service": "admin.googleapis.com",
          "consumer": "projects/561359748979"
        }
      }
    ]
  }
}
```