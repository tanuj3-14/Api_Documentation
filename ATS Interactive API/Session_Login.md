# Session Login

## Overview

The Session Login process allows you to establish a WebSocket connection to the ATS Execution Service and manage session login and logout requests.

## WebSocket Connection

To establish a WebSocket connection with the ATS Execution Service, use the following URL:

<div style="background-color:#f7f7f7; padding: 10px; border: 1px solid #ccc; border-radius: 5px; display: flex; align-items: center;">
  <input type="text" value="ws://execution-streaming-service-ip:port" id="link-to-copy" readonly style="border: none; background-color: #f7f7f7; flex-grow: 1;">
  <button onclick="copyLink()" style="padding: 5px 10px; background-color: #4CAF50; color: white; border: none; cursor: pointer;">Copy Link</button>
</div>

<script>
  function copyLink() {
    const input = document.getElementById('link-to-copy');
    input.select();
    document.execCommand('copy');
    alert('Link copied to clipboard!');
  }
</script>

## Body of Request and Response:

### Session Login Request (1001 - Login Request)

```json
{
    "RequestHeader": {
        "userId": "<user-id>",
        "apiKey": "<api-key>",
        "requestType": 1001
    }
}
