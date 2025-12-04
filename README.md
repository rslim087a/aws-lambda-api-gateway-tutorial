# AWS Lambda API Gateway Tutorial

A serverless QR code generator built with AWS Lambda and API Gateway.

## What's Included

- `lambda_function.py` - QR code generation Lambda handler
- `requirements.txt` - Python dependencies (qrcode, pillow)
- `lambda_deployment.zip` - Ready-to-upload deployment package

## Test Event (for Lambda console)

```json
{
  "body": "{\"url\": \"https://www.youtube.com/@RayanSlim087\"}"
}
```

## cURL Command (after API deployment)

```bash
curl -X POST https://YOUR-API-ID.execute-api.us-east-1.amazonaws.com/prod/generate \
  -H "Content-Type: application/json" \
  -d '{"url": "https://www.youtube.com/@RayanSlim087"}'
```

## View QR Code in Browser

```javascript
const base64 = "PASTE_YOUR_BASE64_HERE";
const img = document.createElement('img');
img.src = 'data:image/png;base64,' + base64;
img.style.width = '300px';
document.body.appendChild(img);
```
