# Sample
Example use of SDK to create self subscriber form with PushPushGo SDK

# Preparing demo
1. Setup account on https://app.pushpushgo.com
2. Create project
3. Create API KEY with access to this project
4. Modify sw.js and replace value PROJECT_ID_HERE with real ProjectId
5. Modify index.html and replace value PROJECT_ID_HERE with real ProjectId

# Run
For python 3.x
`$ python -m http.server 8080`

For python 2.x
`$ python -m SimpleHTTPServer 8080`

# How to send message?
If you fetch correct subscriber id, you can send this via curl like:
```
curl --request POST \
  --url https://api.pushpushgo.com/project/PROJECT_ID_HERE/send/push \
  --header 'accept: application/json' \
  --header 'x-token: xxxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx' \
  --header 'content-type: application/json' \
  -d '{"to": "SUBSCRIBER_ID_HERE", "message": {"title": "sample title", "body": "message conent", "icon": "https://via.placeholder.com/150/150", "redirectLink": "https://samplewebsite.pl"}}'
`````